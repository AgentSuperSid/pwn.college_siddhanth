# Understanding Shebangs
In this challenge we should write a script file and after making it executable, run `/challenge/run`.

## My solve
**Flag:** `pwn.college{gzfNw3GWCCnmjv0aY2YhVe9Ty4l.0VOzMDOxwCO1kjNzEzW}`
- First I created a `solve.sh` script using `nano` command and gave the required input as shown below.
- It took me a while to understand how to create scripts using `nano`.
```bash
#!/bin/bash

echo hack the planet

```
- Then I checked if the script file was executable, which it wasnt so I made it executable.
- Then I ran `/challenge/run` to get the flag.

```bash
hacker@chaining~understanding-shebangs:~$ nano solve.sh
hacker@chaining~understanding-shebangs:~$ ls -l
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
-rw-r--r-- 1 hacker hacker  35 Oct 10 09:49  solve.sh
-rw------- 1 hacker hacker 696 Oct 10 09:44  solve.sh.save
-rw-r--r-- 1 hacker hacker 437 Sep 30 13:02  stdout
-rw-r--r-- 1 hacker hacker 437 Sep 30 12:59  the-flag
-rw-r--r-- 1 hacker hacker   9 Oct 10 05:39  win.sh
-rw-r--r-- 1 hacker hacker   0 Oct  9 11:37  x
-rw-r--r-- 1 hacker hacker 150 Oct  9 15:02  x.sh
-rw-r--r-- 1 root   hacker  60 Sep 23 15:58 '~'
hacker@chaining~understanding-shebangs:~$ chmod u+x solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{gzfNw3GWCCnmjv0aY2YhVe9Ty4l.0VOzMDOxwCO1kjNzEzW}
```

## What I learned 
- I learnt to make scripts using `nano`.
