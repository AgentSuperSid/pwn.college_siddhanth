# Grepping stored results
In this challenge we should redirect the output of */challenge/run* to */tmp/data.txt* and search for the flag using `grep`.

## My solve
**Flag:** `pwn.college{U3gmepLk8f1Nk_-ujRgPaBWg4WS.QX4EDO0wCO1kjNzEzW}`

- First redirect output of */challenge/run* into */tmp/data.txt* by `/challenge/run > /tmp/data.txt`.
- Then there will be thousands of lines of text. One of them is the required flag.
- So we should find that using grep, that is by `grep pwn.college /tmp/data.txt`.
- This will give the flag.

```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn /tmp/data.txt
pwns
pwning
pwn.college{U3gmepLk8f1Nk_-ujRgPaBWg4WS.QX4EDO0wCO1kjNzEzW}
pwn
pwned
```

