# Detaching and Attaching
In this challenge we should open screen, detach, run a command and then reattach to get the flag.

## My solve
**Flag:** `pwn.college{E5CwrHRNVabznKC2xUvwkcrHfAj.0lN4IDOxwCO1kjNzEzW}`

- In this challenge we will just have to follow as they say.
- First open screen by `screen`.
- Then detach using `Ctrl+A` and `d`.
- Then run `/challenge/run` to print the flag in the detached screen as it runs in the background.
- Then reattach to it using `screen -r` to reopen the same screen and read the flag.

```bash
Yes! Flag is: pwn.college{E5CwrHRNVabznKC2xUvwkcrHfAj.0lN4IDOxwCO1kjNzEzW}
```
