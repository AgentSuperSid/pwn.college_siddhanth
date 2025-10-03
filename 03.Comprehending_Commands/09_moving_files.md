# Removing files
- The challenge just gives us a basic introduction of the command **mv** and its importance.

## My Solve
```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet  
Correct! Performing 'mv /flag /tmp/hack-the-planet'.  
hacker@commands~moving-files:~$ /challenge/check  
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:  
pwn.college{8a4eLvBshk0qBvPwj37U8Nf_xdS.0VOxEzNxwCO1kjNzEzW}  
```
## Answer
**Flag:** pwn.college{8a4eLvBshk0qBvPwj37U8Nf_xdS.0VOxEzNxwCO1kjNzEzW}

- Here we should move the *flag* file to *hack-the-planet* file with **mv**. Then execute the *check* program from *challenge* directory.


## What I learned

- What **mv** basically does is that it renames the file(in a way).

