# Matching with *
- This challenge wants us to use the `*` to reduce the code and run the required command.

## My solve
**Flag:** `pwn.college{YCKxaz6nUz11fImND7X0jNlHmkg.QXxIDO0wCO1kjNzEzW}`

- First we should *cd* to */challenge* directory using `*` with less than 4 charecters in total.
- Then run the **/challenge/run** program to get the flag.
```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{YCKxaz6nUz11fImND7X0jNlHmkg.QXxIDO0wCO1kjNzEzW}
```
