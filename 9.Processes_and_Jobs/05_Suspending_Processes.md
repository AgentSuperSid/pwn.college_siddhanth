# Suspending Processes
In this challenge we should run, suspend and run */challenge/run*.

## My solve
**Flag:** `pwn.college{Ifnhtx_RfPzlAHeqj9IM_0H2mq1.QX1QDO0wCO1kjNzEzW}`

- This challenge was pretty straight-forward, run */challenge/run*, suspend it using Ctr+Z, and rerun it, done.

```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         160     144  0 13:04 pts/1    00:00:00 bash /challenge/run
root         162     160  0 13:04 pts/1    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         160     144  0 13:04 pts/1    00:00:00 bash /challenge/run
root         167     144  0 13:04 pts/1    00:00:00 bash /challenge/run
root         169     167  0 13:04 pts/1    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{Ifnhtx_RfPzlAHeqj9IM_0H2mq1.QX1QDO0wCO1kjNzEzW}
```
