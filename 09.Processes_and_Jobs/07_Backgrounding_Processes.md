# Background Processes
In this challenge we are supposed to run */challenge/run* in the background an rerun it.
## My solve
**Flag:** `pwn.college{QQNLhGdEU6fgc7o8hUeu3Dv4DEn.QX3QDO0wCO1kjNzEzW}`

- Just run */challenge/run*, suspend it with Ctrl+Z, run it in background using `bg` and rerun the program.
```bash 
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         147 S+   bash /challenge/run
root         149 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         147 S    bash /challenge/run
root         157 S    sleep 6h
root         158 S+   bash /challenge/run
root         160 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{QQNLhGdEU6fgc7o8hUeu3Dv4DEn.QX3QDO0wCO1kjNzEzW}
```
