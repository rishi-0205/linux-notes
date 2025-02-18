## Tmux (Terminal Multiplexer)

tmux is a terminal multiplexer that allows you to manage multiple terminal sessions inside a single window.
You split windows, detach sessions, and keep processes running even after closing your terminal.
It is useful for remote SSH sessions, as it prevents loss of work if the connection drops.

### Installing tmux

> sudo apt install tmux

to check if tmux is installed

> tmux -V

### Starting and Exiting tmux

Start a new session

> tmux

Exit

1. Exit a session normally: exit
2. Detach without closing: Press Ctrl+B, then D

Reattach a detached session

> tmux attach-session -t 0

If you have multiple sessions, replace 0 with the session ID.

### Understanding tmux Terminology

1. Session: A collection of windows and panes.
2. Window: A full-screen terminal inside a session.
3. Pane: A split section inside a window.
4. Detach: Leave tmux running in the background.
5. Reattach: Reconnect to a detached tmux session.

### Basic tmux Shortcuts

tmux uses Ctrl+B as a prefix key before commands.

1. Detach session: ctrl+B, then D
2. Create a new window: ctrl+B, then C
3. Switch windows: ctrl+B, then N(next)/P(previous)
4. List all windows: ctrl+B, then W
5. Split window horizontally: ctrl+B, then %
6. Split window vertically: ctrl+B, then "
7. Navigate panes: ctrl+B, then arrow keys
8. Kill a pane: ctrl+B, then X

### Managing Sessions
