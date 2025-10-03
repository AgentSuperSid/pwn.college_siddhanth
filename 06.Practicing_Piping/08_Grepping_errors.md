# Grepping errors
In this challenge we should redirect errors directly in a single line wihtout making a new file.

## My solve
**Flag:** `pwn.college{QcsLaHSUiJw8miEdmzGtjC_A5yr.QX1ATO0wCO1kjNzEzW}`

- As informed by them, for errors we should type `2>& 1` before `|` to be able to directly access text using grep in a single line.
- We can do this as `/challenge/run 2>& 1 | grep pwn.college`.
- This will give us the required output.
```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{QcsLaHSUiJw8miEdmzGtjC_A5yr.QX1ATO0wCO1kjNzEzW}
```

## What I learned 
- How to use `|` to redirect errors directly.
