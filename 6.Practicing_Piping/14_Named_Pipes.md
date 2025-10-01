# Named Pipes
- This challenge wants us to create a named pipe, redirect output of */challenge/run* into it and read it to get the flag.
## My solve
**Flag:** `pwn.college{A63hpjURa_71XnvPNJ_D0VJQMWd.01MzMDOxwCO1kjNzEzW}`

- First, create the named pipe using `mkfifo`- `mkfifo /tmp/flag_fifo`.
- Then, as mentioned, run */challenge/run* and redirect output into */tmp/flag_fifo*: `/challenge/run > /tmp/flag_fifo`.
- Now the current terminal will be blocked by the named pipe till an stdout is made for */tmp/flag_fifo*.
- So we should do that in a new terminal: `cat /tmp/flag_fifo`.
- This will give the flag.
- 
Terminal 1 
```bash
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!
```
Terminal 2
```bash
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{A63hpjURa_71XnvPNJ_D0VJQMWd.01MzMDOxwCO1kjNzEzW}
```

## What I learned 
- Creating, accessing and printing named pipes and its contents
