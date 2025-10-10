# Scripting with Arguments
In this challenge we are supposed to write a `solve.sh` script to output the reverse of its agrument.

## My solve
**Flag:** `pwn.college{0d9EQL6gq8xulBbXPDDCynOtUtR.0VNzMDOxwCO1kjNzEzW}`

- Fist I wrote the script as shown below. Since they said to output to reverse the words I just used `echo ` and did `$2 $1`.
- Then run `/challenge/run`, it checked then gave the flag.
```bash
hacker@chaining~scripting-with-arguments:~$ ls -l
total 56
-rw-r--r-- 1 hacker hacker   4 Sep 29 17:55  COLLEGE
drwxr-xr-x 1 hacker hacker   0 Sep 21 08:30  Desktop
-rw-r--r-- 1 hacker hacker   8 Sep 30 14:07  PWN
-rw-r--r-- 1 root   hacker  77 Sep 30 17:09  cmd1_out
-rw-r--r-- 1 hacker hacker 829 Sep 30 13:55  instructions
-rw-r--r-- 1 hacker hacker   0 Oct  1 07:04  mkfifo
-rw-r--r-- 1 hacker hacker  95 Sep 30 13:55  myflag
lrwxrwxrwx 1 hacker hacker   5 Sep 25 17:15  not-the-flag -> /flag
-rwxr--r-- 1 hacker hacker  17 Oct  9 14:36  script.sh
-rwxr--r-- 1 hacker hacker  35 Oct 10 09:49  solve.sh
-rw------- 1 hacker hacker 696 Oct 10 09:44  solve.sh.save
-rw-r--r-- 1 hacker hacker 437 Sep 30 13:02  stdout
-rw-r--r-- 1 hacker hacker 437 Sep 30 12:59  the-flag
-rw-r--r-- 1 hacker hacker   9 Oct 10 05:39  win.sh
-rw-r--r-- 1 hacker hacker   0 Oct  9 11:37  x
-rw-r--r-- 1 hacker hacker 150 Oct  9 15:02  x.sh
-rw-r--r-- 1 root   hacker  60 Sep 23 15:58 '~'
hacker@chaining~scripting-with-arguments:~$ nano solve.sh
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{0d9EQL6gq8xulBbXPDDCynOtUtR.0VNzMDOxwCO1kjNzEzW}
```
```bash
  GNU nano 8.4                                                         solve.sh                                                                   
#!/bin/bash

echo $2 $1
```
## What I learned
- How to use the read argument of a script and manipulate them.
