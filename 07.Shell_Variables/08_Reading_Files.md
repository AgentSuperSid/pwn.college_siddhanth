# Reading Files
- In this challenge we should read */challenge/read_me* right into the *PWN* variable with one command.
## My solve
**Flag:** `pwn.college{YTA5uu4y_zXDgyKu7FL-Yz_7j2U.QXwIDO0wCO1kjNzEzW}`

- We can solve by using `read` command by redirecting input of */challenge/read_me* into *PWN* in the same line using `<`.
- This is done as `read PWN < /challenge/read_me`.
- This will give us the flag.

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{YTA5uu4y_zXDgyKu7FL-Yz_7j2U.QXwIDO0wCO1kjNzEzW}
```

