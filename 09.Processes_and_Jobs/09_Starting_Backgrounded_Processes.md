# Starting Backgrounded Processes
In this challenge you are supposed to run */challenge/run* without suspending.

## My solve
**Flag:** `pwn.college{kLxYnEVMrZEmEPIMx3EdDoxo2PQ.QX5QDO0wCO1kjNzEzW}`

- You can run a the program without suspending using `&` as argument, that is by `/challenge/run & bg`.
```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run & bg
[1] 146
bash: bg: job 1 already in background
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{kLxYnEVMrZEmEPIMx3EdDoxo2PQ.QX5QDO0wCO1kjNzEzW}

## What I learned 
