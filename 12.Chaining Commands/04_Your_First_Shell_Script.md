# Your First Shell Script
In this challenge we should run /challenge/pwn and then /challenge/college, but this time in a shell script.

## My solve
**Flag:** `pwn.college{wZI3eScISVUmsjy51YNC4CiXVDo.QXxcDO0wCO1kjNzEzW}`

- First we have to redirect the outputs of `echo /challenge/pwn` and `echo /challenge/college` into `x.sh.
- `>>` was to prevent overwriting.
- First I tried directly redirecting output of the commands but it didnt work so after some tries it worked for `echo`.

```bash
hacker@chaining~your-first-shell-script:~$ echo /challenge/pwn > x.sh;
echo /challenge/college >> x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{wZI3eScISVUmsjy51YNC4CiXVDo.QXxcDO0wCO1kjNzEzW}
```

## Incorrect Tangents
- I was doing `/challenge/pwn; /challenge/college > x.sh`.
- This only redirected the output of the second command.
