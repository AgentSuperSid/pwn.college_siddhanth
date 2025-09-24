# Hidden files
-The challenge just gives us information on the usage of *ls -a* command to access the hidden files

## My Solve

hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ cat .flag-223813006523155
pwn.college{cJ4q2RLioNlcm5GGcUx2_UicJFV.QXwUDO0wCO1kjNzEzW}

## Answer
**Flag:** pwn.college{cJ4q2RLioNlcm5GGcUx2_UicJFV.QXwUDO0wCO1kjNzEzW}

-Here we should go to **/** directory, then search for the hidden flag file *.flag-223813006523155* using *ls -a* command, cat the file and get the flag.
-I was thinking that the flag file would be somewhere in the *~* directory itself.



## What I learned
- Some files(.filename files) are not visible to us directly when we use *ls* and we should use *ls -a* to view them.

## Incorrect tangents
-I tried almost all the files and found all possible fake flags in the *~* directory rather than going for */* directory and searching for the flag file.
-I was supposed to go to */* directory and then search for the flag file