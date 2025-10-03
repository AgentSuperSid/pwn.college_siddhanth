# Other users with su
In this challenge we are supposed to access */challenge/run* while logging in as **zardus** user.

## My solve
**Flag:** `pwn.college{sYGHwkOXdC-4YucPPoDEak44qVo.QX2UDN1wCO1kjNzEzW}`

- we had to do the same thing what we did last challenge but this time we should just give the username as an argument to `su`.

```bash
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{sYGHwkOXdC-4YucPPoDEak44qVo.QX2UDN1wCO1kjNzEzW}
```
