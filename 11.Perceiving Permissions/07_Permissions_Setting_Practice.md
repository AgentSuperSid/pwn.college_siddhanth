# Permissions Setting Practice
In this challenge we will have to do the same thing we did in the previous challenge but by using `=`,`,` and `-`.

## My solve
**Flag:** `pwn.college{sCjCYAp9l30FZHp-NpuZA18ijZB.QXzETO0wCO1kjNzEzW}`

- We had to do the same thing as we did the last time but using `=`,`,` and `-`.
- This time they made me the user so I used `u+r` to be able to read the flag file.

```bash
hacker@permissions~permissions-setting-practice:~$ chmod u+r /flag
hacker@permissions~permissions-setting-practice:~$ cat /flag
pwn.college{sCjCYAp9l30FZHp-NpuZA18ijZB.QXzETO0wCO1kjNzEzW}
```

## What I learned 
- U can add multiple arguments to `chmod` using `,`.
- U can also use `=` to rewrite all permissions rather than `+-` to change permissions.
- Typing `-` after `g/u/o=` will remove all permissions for the respective user/s.
