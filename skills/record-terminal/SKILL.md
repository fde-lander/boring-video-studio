---
name: record-terminal
description: Use when recording terminal command execution for a video; use ttyd to present a real local shell in Chrome for capture.
---

# Record terminal

Present a real local shell in Chrome with `ttyd`, then operate that browser terminal so commands and output appear in the recording.

## Prepare

1. Resolve the working directory, shell, command sequence, and target frame. Default to the current directory, login shell, and a 16:9 Chrome window.
2. Run `command -v ttyd`. When it is missing, tell the user that `ttyd` is required, show the relevant install command (`brew install ttyd` on macOS or the system package manager on Linux), and resume after it becomes available.
3. Choose an unused local port, normally `7681`, and the loopback interface (`lo0` on macOS, `lo` on Linux).

## Start the terminal

Keep `ttyd` in a managed long-running process so its output and lifecycle remain observable:

```bash
ttyd \
  -i lo0 \
  -p 7681 \
  -W -o -q \
  -w /absolute/working/directory \
  -t fontSize=20 \
  -t cursorBlink=true \
  -t 'theme={"background":"#0b0f14","foreground":"#e6edf3","cursor":"#7ee787"}' \
  /bin/zsh -l
```

Adapt the interface and shell to the host. The loopback bind keeps the writable shell local; one-client and exit-on-disconnect options give the recording session a bounded lifetime.

## Capture through Chrome

1. Open `http://127.0.0.1:<port>/` with the available Chrome browser-control tool and use a 16:9 viewport when it can set one.
2. Verify the visible path and round trip with `printf 'recording-ready\n'; pwd`.
3. Clear the terminal. When an agent-controlled screen recorder is available, start a Chrome-window capture and record its output path. When the user controls capture, hand off the ready window and wait for the start cue.
4. Enter every on-camera command through the browser terminal. Use deliberate typing and leave a short visual beat after meaningful output.
5. Read the rendered output before advancing. Preserve prompts, ANSI color, progress, and interactive TUI behavior as part of the shot.
6. Stop agent-controlled capture after the final visual beat and verify the video is playable. For user-controlled capture, leave the completed Chrome frame visible for handoff.
7. After capture is accepted, close the page and confirm the managed `ttyd` process has exited.

The session is complete when Chrome has run the requested commands at the intended video size and the recording is either verified or handed back to the user's recorder.
