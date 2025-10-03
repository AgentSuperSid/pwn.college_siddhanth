# Becoming Root with su
In this challenge we should login as **root** user and read the flag file.

## My solve
**Flag:** `pwn.college{o1xegAjq5g8eWy5w_qjH_ZrBs0q.QX1UDN1wCO1kjNzEzW}`

- As they instructed, first is typed `su`, it gave a prompt for password, gave what was given and logged in as user.
- Then I wanted to know the flag name, so I `ls`-ed to check the files.
- Once I saw the file **not-the-flag** I knew that was the flag file and read it and go the flag.

```bash
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# ls
 COLLEGE   Desktop   PWN   cmd1_out   instructions   mkfifo   myflag   not-the-flag   stdout   the-flag  '~'
root@users~becoming-root-with-su:/home/hacker# cat not-the-flag
pwn.college{o1xegAjq5g8eWy5w_qjH_ZrBs0q.QX1UDN1wCO1kjNzEzW}
```

