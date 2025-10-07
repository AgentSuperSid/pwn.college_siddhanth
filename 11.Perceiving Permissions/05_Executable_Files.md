# Executable Files

## My solve
**Flag:** `pwn.college{AWo5yif7UK1wV-JKxa6v65FY_tJ.QXyEjN0wCO1kjNzEzW}`

- I checked the owner and the group and the permissions they had to decide if I had to use `o` or `a` in the argument of `chmod`.
- The group that had reading permission was `hacker` so I had to use `a` and not `o`.
- I was still not so familiar with all the other arguments I could give specifically for a group etc.
- After making the changes by running `/challenge/run` you will get the flag.

```bash
hacker@permissions~executable-files:~$ ls -l
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
hacker@permissions~executable-files:~$ chmod a+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{AWo5yif7UK1wV-JKxa6v65FY_tJ.QXyEjN0wCO1kjNzEzW}
```

## Incorrect Tangents
- I didnt check initially wether teh group that had access to this file was `hacker` or not and used `o` in the argument part.
- This excluded the `hacker` group to which we belonged to and thus didnt get the permission.
- Then after checking by listing it I understood this,
