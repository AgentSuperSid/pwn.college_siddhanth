# 8.Implicit relative path

## My Solve

hacker@paths~implicit-relative-path:~$ cd /
hacker@paths~implicit-relative-path:/$ cd challenge/.
hacker@paths~implicit-relative-path:/challenge$ run
bash: run: command not found
hacker@paths~implicit-relative-path:/challenge$ cd ./run
bash: cd: ./run: Not a directory
hacker@paths~implicit-relative-path:/challenge$ run
bash: run: command not found
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!

## Answer:
**Flag:** pwn.college{ITiecgC8WU24RviGcFPxPwqNX1l.QXxUTN0wCO1kjNzEzW}

-Here i thought that we were just supposed to give **.** before */challenge* like last challenge to get the flag.
-Then i understood that you are supposed to run the *run* program with a **.** which acts as an assurance or clarity that we want to run the program **run** from the **challenge** directory itself and not from some parent directory.

