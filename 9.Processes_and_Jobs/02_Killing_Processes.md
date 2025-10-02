# Killing Processes
- In this challenge we are supposed to kill */challenge/dont_run* process in order too run the */challenge/run* process.

## My solve
**Flag:** `pwn.college{w9EgM_h3JbKnhYjTBTkHAdysA6E.QXyQDO0wCO1kjNzEzW}`

- First I had to search for the **PID** of */challenge/dont_run*, for which I used `ps -ef | grep dont_run`.
- I used `grep` because im more comfortable with it as it was used more in previous challenges, and because it was given in the example.
- Once I got the **PID** (136) just use the `kill` command, that is `kill 136`.

```bash
hacker@processes~killing-processes:~$ ps -ef | grep dont_run
hacker       136     135  0 18:42 ?        00:00:00 /challenge/dont_run
hacker       185     175  0 18:43 pts/2    00:00:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{w9EgM_h3JbKnhYjTBTkHAdysA6E.QXyQDO0wCO1kjNzEzW}
hacker@processes~killing-processes:~$
```

## What I learned 
- Yet another application of `grep`.
- `kill` only accepts **PID** of a program.
