# Setting PATH
In this challenge we should input the path of `win` command in `PATH` and run it using `/challenge/run`.

## My solve
**Flag:** `pwn.college{EymdhCsPNJ-sG02OSlaJDtEbCGT.QX1cjM1wCO1kjNzEzW}`

- We have to input the path of `win` command into `PATH` by `PATH=/challenge/more_commands`.
- Then you can directly run the `/challenge/run` command which can directly access `win` without typing the path of the command.

```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{EymdhCsPNJ-sG02OSlaJDtEbCGT.QX1cjM1wCO1kjNzEzW}
```

