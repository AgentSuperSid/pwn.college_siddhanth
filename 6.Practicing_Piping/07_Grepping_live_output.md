# Grepping live output
- We should find the flag using `grep` by redirecting output of */challenge/run* without using any file.

## My solve
**Flag:** `pwn.college{Uw-8Y8c2yxGken-B7y29X7Hj5qq.QX5EDO0wCO1kjNzEzW}`

- As mentioned, by following the example provided by them initially, we can directly redirect teh output of */challenge/run* and access the flag using `grep` by using `|`.
- This can be done by `/challenge/run | grep pwn.college`
```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{Uw-8Y8c2yxGken-B7y29X7Hj5qq.QX5EDO0wCO1kjNzEzW}
```

## What I learned 
- We can directly use `grep` and search for the required text as the output is redirected by using `|`.
