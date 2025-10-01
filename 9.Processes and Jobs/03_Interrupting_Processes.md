# interrupting Processes
- In this challenge we should run */challenge/run* and interrupt it.

## My solve
**Flag:** `pwn.college{YgPxFdNNioGcL61BMulHd7Si6Bs.QXzQDO0wCO1kjNzEzW}`

- Things were pretty much straight forward, just run `/challenge/run` and interrupt using `Ctrl+C`.
- This will give the flag

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{YgPxFdNNioGcL61BMulHd7Si6Bs.QXzQDO0wCO1kjNzEzW}
```
