# Finding files
- This challenge gives us the introduction to the **find** command.

## My Solve
```
find / -name flag  
/usr/local/lib/python3.8/dist-packages/prompt_toolkit/key_binding/__pycache__/flag  
/usr/local/lib/python3.8/dist-packages/pwnlib/flag  
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag  
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/prompt_toolkit/key_binding/__pycache__/flag  
pwn.college{gHERk-9D2Ib8Z6kkKWiHucdWL2B.QXyMDO0wCO1kjNzEzW}  
```
- While using **find** we should specify the directory where we need to search to */* so that we can get all the possible files with the name *flag*.
- It takes time for the files which we can access to appear after running the command. Then access one by one each file using **cat** to get a flag value an keep trying till you get the correct one.

## Answer

**Flag:** pwn.college{gHERk-9D2Ib8Z6kkKWiHucdWL2B.QXyMDO0wCO1kjNzEzW}

## What I learned
- The working and usage of **find** command with which we can find any directory's or file's path or of all the files or directories with the same name.
