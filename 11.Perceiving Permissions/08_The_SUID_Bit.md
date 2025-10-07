# The SUID Bit
In this challenge we have to give ourselves permission to run the */challenge/getroot* and read the flag as `root` user.

## My solve
**Flag:** `pwn.college{kqYQ0JUwUSfkwZgOZ4Za3SeJMCS.QXzEjN0wCO1kjNzEzW}`

- First I gave myself the `su` permissions to */challenge/getroot* and then read the `/flag` after running*/challenge/getroot*.

```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{kqYQ0JUwUSfkwZgOZ4Za3SeJMCS.QXzEjN0wCO1kjNzEzW}
```
