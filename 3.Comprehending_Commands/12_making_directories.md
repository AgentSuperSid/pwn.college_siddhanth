# Making directories
- This challenge gives us the introduction to the **mkdir** command.

## My Solve
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn  
hacker@commands~making-directories:~$ cd /tmp/pwn  
hacker@commands~making-directories:/tmp/pwn$ touch college  
hacker@commands~making-directories:/tmp/pwn$ /challenge/run  
Success! Here is your flag:  
pwn.college{cZCZJcjkUCasj2LBgppU6IWJlSB.QXxMDO0wCO1kjNzEzW}  
hacker@commands~making-directories:/tmp/pwn$  
```
- First we should create a directory */tmp/pwn* using **mkdir** and then create file *college* using **touch** file.

## Answer

**Flag:** pwn.college{cZCZJcjkUCasj2LBgppU6IWJlSB.QXxMDO0wCO1kjNzEzW}

## What I learned
- The usage of **mkdir** command, which is to create new directories.
