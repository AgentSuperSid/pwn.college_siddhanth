# Detaching and Attaching (tmux)
In this challenge we should open session, detach it, run a command and then reattach that session to get the flag.

## My solve
**Flag:** `pwn.college{sdcg9iRoMjkyt-eP7xiROKsJFAQ.0VO4IDOxwCO1kjNzEzW}`

- We had to follow as they instructed- `tmux` to open the session and `Ctrl+B d` to detach that session.
- Run `/challenge/run` to generate the flag in that session and then reattach that session using `tmux a` to get the flag.

```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{sdcg9iRoMjkyt-eP7xiROKsJFAQ.0VO4IDOxwCO1kjNzEzW}
Congratulations, here is your flag: pwn.college{sdcg9iRoMjkyt-eP7xiROKsJFAQ.0VO4IDOxwCO1kjNzEzW}
```
## What I learned
- Using the `tmux` command to open and use sessions.
