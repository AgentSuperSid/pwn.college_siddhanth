# Linking files
- This challenge gives us the introduction to the **ln** command.

## My Solve

hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag  
hacker@commands~linking-files:~$ /challenge/catflag  
About to read out the /home/hacker/not-the-flag file!  
pwn.college{k-dKyP8JyxF390L1rFEINt-e9Hi.QX5ETN1wCO1kjNzEzW}  

- Since the */challenge/catflag* would read the *not-the-flag* file, I made a soft link to the flag file so that when the command is invoked, the contents of the *flag* file is given.

## Answer

**Flag:** pwn.college{k-dKyP8JyxF390L1rFEINt-e9Hi.QX5ETN1wCO1kjNzEzW}

## What I learned

- The logic and usage behind the soft link to access the contents of another file by linking them using *ln -s* command.
