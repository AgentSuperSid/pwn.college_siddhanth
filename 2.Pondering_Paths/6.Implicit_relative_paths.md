# 6.Implicit relative paths, from /
-This is the application of the very thing i had doubts about initially.
-We should first come to **/** directory, then from there go to challenge directory and open run by relative path(not absolute path).
-Learnt the usage of **..** and also had a better understanding of this topic.

## My Solve:
hacker@paths~implicit-relative-paths-from-:~$ challenge/run
bash: challenge/run: No such file or directory
hacker@paths~implicit-relative-paths-from-:~$ cd ../..
hacker@paths~implicit-relative-paths-from-:/$  challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!

## Answer:
**Flag:** pwn.college{EBVfJLUSD8ufYmpImW5gnNUz0h-.QX5QTN0wCO1kjNzEzW}

## Incorrect Tangents

-Here **challenge** was a directory so in order to make it relative path i didn't have to type **/**. I thought it was a program.
