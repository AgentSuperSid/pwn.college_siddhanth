# Redirecting errors
In this challenge we are supposed to redirect */challenge/run*'s output to *myflag* and the error(instructions) to *instructions* file.

## My solve
**Flag:** `pwn.college{85yZNyk2c9FwHp4PkmyQOWkf-FX.QX3YTN0wCO1kjNzEzW}`

- All we have to do is type `/challenge/run > myflag 2>instructions` which will redirect */challenge/run*'s output to *myflag* and the error(instructions) to *instructions* file.
- Then read the flag from *myflag* using `cat`.
```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2>instructions
hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{85yZNyk2c9FwHp4PkmyQOWkf-FX.QX3YTN0wCO1kjNzEzW}
```

## What I learned 
- I learnt that `>` or `1>` redirects output to file and `2>` redirects the std. error into a file.
