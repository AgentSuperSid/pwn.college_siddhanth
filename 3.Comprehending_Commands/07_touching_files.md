# Touching files
- The challenge just gives us a basic introduction of the command **touch** and its importance.

## My Solve

hacker@commands~touching-files:~$ touch /tmp/pwn /tmp/college  
hacker@commands~touching-files:~$ /challenge/run  
Success! Here is your flag:  
pwn.college{UoojaTjaJ4RSgQDemY8oNAT78yY.QXwMDO0wCO1kjNzEzW}  
  
## Answer
**Flag:** pwn.college{UoojaTjaJ4RSgQDemY8oNAT78yY.QXwMDO0wCO1kjNzEzW}

- Here we were supposed to create the two files *pwn* and *college* in the *tmp* directory. Then execute the *run* program from *challenge* directory.
- I was curious to see if we could create 2 files at the same time(in a single line) rather than writing the line for each file. It worked.


## What I learned

- Usage of **touch** that is, with the help of it we can create a new file in that directory.
