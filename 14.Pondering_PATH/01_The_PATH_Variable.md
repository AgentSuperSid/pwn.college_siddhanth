# The PATH Variable
In this challenge we are supposed to clear `PATH` to disable `rm` when we run `/challenge/run`.
## My solve
**Flag:** `pwn.college{Uc_y28IxBtKIN3-8rReXlWRTvNW.QX2cDM1wCO1kjNzEzW}`
- What we did is that we deleted the path where the basics commands are present, including `rm` by `PATH=""`.
- So when we run `/challenge/run` the command will not be able to call `rm` and thus the flag will not be removed.

```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{Uc_y28IxBtKIN3-8rReXlWRTvNW.QX2cDM1wCO1kjNzEzW}
```

## What I learned 
`PATH` contains the basic commands we use.
