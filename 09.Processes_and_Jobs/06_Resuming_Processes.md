# Resuming Processes
In this challenge we should suspend and continue */challenge/run*'s process.

## My solve
**Flag:** `pwn.college{c3RHlgNJpQ94lrwJ2P4fZ5gD7xi.QX2QDO0wCO1kjNzEzW}`

- I had to just as they instructed, run */challenge/run*, suspend eith Ctrl+Z, then continue it with `fg`

```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{c3RHlgNJpQ94lrwJ2P4fZ5gD7xi.QX2QDO0wCO1kjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```
