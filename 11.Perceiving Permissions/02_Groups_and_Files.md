# Groups and Files
In this challenge we should change the group who can access the flag file from `root` to `hacker`.

## My solve
**Flag:** `pwn.college{kQ7nSztZe065ufsmZ3NetfNmsQP.QXxcjM1wCO1kjNzEzW}`

- First I just looked for the flag file.
- Then I changed the group which can access the flag file to `hacker` using `chgrp`, that is `chgrp hacker not-the-flag`.


```bash
hacker@permissions~groups-and-files:~$ ls -l
total 36
-rw-r--r-- 1 hacker hacker   4 Sep 29 17:55  COLLEGE
drwxr-xr-x 1 hacker hacker   0 Sep 21 08:30  Desktop
-rw-r--r-- 1 hacker hacker   8 Sep 30 14:07  PWN
-rw-r--r-- 1 root   hacker  77 Sep 30 17:09  cmd1_out
-rw-r--r-- 1 hacker hacker 829 Sep 30 13:55  instructions
-rw-r--r-- 1 hacker hacker   0 Oct  1 07:04  mkfifo
-rw-r--r-- 1 hacker hacker  95 Sep 30 13:55  myflag
lrwxrwxrwx 1 hacker hacker   5 Sep 25 17:15  not-the-flag -> /flag
-rw-r--r-- 1 hacker hacker 437 Sep 30 13:02  stdout
-rw-r--r-- 1 hacker hacker 437 Sep 30 12:59  the-flag
-rw-r--r-- 1 root   hacker  60 Sep 23 15:58 '~'
hacker@permissions~groups-and-files:~$ chgrp hacker not-the-flag
hacker@permissions~groups-and-files:~$ cat not-the-flag
pwn.college{kQ7nSztZe065ufsmZ3NetfNmsQP.QXxcjM1wCO1kjNzEzW}
```
