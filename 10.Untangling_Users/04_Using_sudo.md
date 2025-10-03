# Using sudo
In this challenge we are supposed to read the flag file with **sudo** access.

## My solve
**Flag:** `pwn.college{oOy5QzR0CxoqQ21L2lezbt69oy9.QX4UDN1wCO1kjNzEzW}`

- I just checked initially if I could access it directly, in the sense if i was by default the root user and could access it.
- Then I used the code `sudo` to read the flag file.
- From previous experience i knew it would be in the `not-the-flag` file.

```bash
hacker@users~using-sudo:~$ ls
 COLLEGE   Desktop   PWN   cmd1_out   instructions   mkfifo   myflag   not-the-flag   stdout   the-flag  '~'
hacker@users~using-sudo:~$ cat not-the-flag
cat: not-the-flag: Permission denied
hacker@users~using-sudo:~$ sudo cat not-the-flag
pwn.college{oOy5QzR0CxoqQ21L2lezbt69oy9.QX4UDN1wCO1kjNzEzW}
```
