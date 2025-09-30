# Redirecting more output
In this challenge we should print the output of */challenge/run* into *myflag* file using `>`.

## My solve
**Flag:** `pwn.college{c64fwik29JWdCG1ZhP5tBXbwMRH.QX1YTN0wCO1kjNzEzW}`

- Since they said to redirect output of */challenge/run* into *myflag* the command will be /challenge/run > myflag.
-  This will redirect output flag into the *myflag* file which can be read using **cat**.
 
```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{c64fwik29JWdCG1ZhP5tBXbwMRH.QX1YTN0wCO1kjNzEzW}
```



