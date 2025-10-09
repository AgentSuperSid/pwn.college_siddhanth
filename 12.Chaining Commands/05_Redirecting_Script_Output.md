# Redirecting Script Output
In this challenge we are supposed to input the commands into a shell script, pipe its output to another command which prints the flag.

## My solve
**Flag:** `pwn.college{gcwYjzblbSzslo2JgZgYZor_jHa.QX4ETO0wCO1kjNzEzW}`

- I had to do all in 1 line.
- Since both the commands had to run (inputting commands and piping output) so I used `&&`. Also used `()` for similar purpose.
- Took a while but at the end got the right command.
- Since the shell ran the commands at the end there are 2 error messages.
- These error messages are by default redirected to `stderr` so it was not a worry.

```bash
hacker@chaining~redirecting-script-output:~$ (echo /challenge/pwn; echo /challenge/college) >> x.sh && bash x.sh | /challenge/solve  
x.sh: line 1: cb048a2db8b834eff587fee2c5381da9: command not found
x.sh: line 2: 3857dfd5d1417d87a9d97d791dd6dfc8: command not found
Correct! Here is your flag:
pwn.college{gcwYjzblbSzslo2JgZgYZor_jHa.QX4ETO0wCO1kjNzEzW}
```

## Incorrect tangents
- I forgot to use `>>` initially due to which I was getting error.

## What I learned
- I learned why `echo` was needed in this and previous challenge, which is because by using `echo` the `x.sh` would take the commands as input but if it wasnt there then the output of those commands would be taken as input and then there would be a messup.
