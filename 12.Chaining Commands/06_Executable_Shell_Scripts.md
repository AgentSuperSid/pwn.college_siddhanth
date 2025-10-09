# Executable Shell Scripts
In this challenge we are supposed to explicitly call the script file after inputing the commands into it without using `bash`.

## My solve
**Flag:** `pwn.college{AzAFKe-I073t6Ce_SvYmprPS3Zm.QX0cjM1wCO1kjNzEzW}`

- While calling script it saif permission denied.
- Then I understood that when they said make it executable they meant to give the user (us) the permission to execute using `chod`.
- I did the same and then ran it to get the flag.

```bash
hacker@chaining~executable-shell-scripts:~$ echo /challenge/solve > script.sh
hacker@chaining~executable-shell-scripts:~$ ~/script.sh
bash: /home/hacker/script.sh: Permission denied
hacker@chaining~executable-shell-scripts:~$ ls -l
total 44
-rw-r--r-- 1 hacker hacker   4 Sep 29 17:55  COLLEGE
drwxr-xr-x 1 hacker hacker   0 Sep 21 08:30  Desktop
-rw-r--r-- 1 hacker hacker   8 Sep 30 14:07  PWN
-rw-r--r-- 1 root   hacker  77 Sep 30 17:09  cmd1_out
-rw-r--r-- 1 hacker hacker 829 Sep 30 13:55  instructions
-rw-r--r-- 1 hacker hacker   0 Oct  1 07:04  mkfifo
-rw-r--r-- 1 hacker hacker  95 Sep 30 13:55  myflag
lrwxrwxrwx 1 hacker hacker   5 Sep 25 17:15  not-the-flag -> /flag
-rw-r--r-- 1 hacker hacker  17 Oct  9 14:36  script.sh
-rw-r--r-- 1 hacker hacker 437 Sep 30 13:02  stdout
-rw-r--r-- 1 hacker hacker 437 Sep 30 12:59  the-flag
-rw-r--r-- 1 hacker hacker   0 Oct  9 11:37  x
-rw-r--r-- 1 hacker hacker 106 Oct  9 14:22  x.sh
-rw-r--r-- 1 root   hacker  60 Sep 23 15:58 '~'
hacker@chaining~executable-shell-scripts:~$ chmod u+x script.sh
hacker@chaining~executable-shell-scripts:~$ ./script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{AzAFKe-I073t6Ce_SvYmprPS3Zm.QX0cjM1wCO1kjNzEzW}
```
