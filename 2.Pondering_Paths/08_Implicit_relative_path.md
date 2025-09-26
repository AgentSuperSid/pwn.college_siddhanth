# 8.Implicit relative path
- In this challenge we are supposed to learn the usage of **.** in paths.
## My Solve
```
hacker@pathsimplicit-relative-path:~$ cd /  
hacker@pathsimplicit-relative-path:/$ cd challenge/.  
hacker@pathsimplicit-relative-path:/challenge$ run  
bash: run: command not found  
hacker@pathsimplicit-relative-path:/challenge$ cd ./run  
bash: cd: ./run: Not a directory  
hacker@pathsimplicit-relative-path:/challenge$ run  
bash: run: command not found  
hacker@pathsimplicit-relative-path:/challenge$ ./run  
Correct!!!  
./run is a relative path, invoked from the right directory!  
```
## Answer:
**Flag:** pwn.college{ITiecgC8WU24RviGcFPxPwqNX1l.QXxUTN0wCO1kjNzEzW}

## What I learned
- Here I thought that we were just supposed to give **.** before */challenge* like last challenge to get the flag.
- Then I understood that you are supposed to run the *run* program with a **.** which acts as an assurance or clarity that we want to run the program **run** from the **challenge** directory itself and not from some parent directory.



