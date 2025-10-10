# Adding Commands
In this challenge we are supposed to create a shell script called `win`, add its location to `PATH` and run `/challenge/run`.

## My solve
**Flag:** `pwn.college{8JdtAIYsxbeI23LYQdveP6qzIrp.QX2cjM1wCO1kjNzEzW}`

- First we should create a shell script `win` and type the given below block.
- The `cat` path is found using `which`.
- `read` is used so that teh flag can be read.
- All permissions were given to `/flag` just in case.
- Then `/challenge/run` was run. 

```bash
  GNU nano 8.4                                                           win                                                                      

/run/dojo/bin/cat /flag

```
- If it was for win.sh
```bash
  GNU nano 8.4                                                          win.sh                                                                    
#!/bin/bash
read var < /flag
/run/dojo/bin/cat /flag

```
```bash
hacker@path~adding-commands:~$ touch win
hacker@path~adding-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ chmod ugo+rwx win
hacker@path~adding-commands:~$ PATH=/home/hacker
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
/home/hacker/win: line 1: GNU: command not found
pwn.college{8JdtAIYsxbeI23LYQdveP6qzIrp.QX2cjM1wCO1kjNzEzW}
hacker@path~adding-commands:~$ 
```
- If used `win.sh` then just substitute `win` with that in the above method.

## Incorrect Tangents
- I was doing in `win.sh` as they mentioned earlier but we were supposed to create file `win` and then do the same, due to which `/challenge/run` couldnt find the file.
- If I needed to use `win.sh`, I should have written `read var < /flag` inside it as `read` would work even after the contents of `PATH` changed ( read is a builtin functionality of bash).
