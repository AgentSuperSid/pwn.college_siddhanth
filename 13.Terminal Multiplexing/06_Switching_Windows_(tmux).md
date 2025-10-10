# Switching Windows (tmux)
In this challenge we are supposed to reattach a session and switch to window 0 to get the flag.

## My solve
**Flag:** `pwn.college{wrtM6HIHyS-2MS6a94E6W_XTwKo.0FM5IDOxwCO1kjNzEzW}`

- First I had to to reattach to a session with `tmux a`.
- Then Follow as they instructed- switch to window 0 using `Ctrl+B 0`.
- This will take us to window 0 which has the flag.
- In the beginning I was a bit confused if I had to create a new session and then continue or just reattach.
- Then I thought since the widows are already present there must be a pre-existing session so I directly reattached.

```bash
 cat <<MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!
MSG
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Welcome to the tmux window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-B 0 to switch to window 0!
> MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows-tmux:~$
```

```bash
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{wrtM6HIHyS-2MS6a94E6W_XTwKo.0FM5IDOxwCO1kjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{wrtM6HIHyS-2MS6a94E6W_XTwKo.0FM5IDOxwCO1kjNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$
```
