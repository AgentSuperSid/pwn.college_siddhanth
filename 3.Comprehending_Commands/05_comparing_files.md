# Comparing files
- The challenge just gives us a basic introduction of the command **diff** and its importance.

## My Solve
```
hacker@commands~comparing-files:$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt  
10a11  
> pwn.college{s2yFb9jV56qYERvqd0fL8sGS6_K.01MwMDOxwCO1kjNzEzW}  
```
## Answer
**Flag:** pwn.college{s2yFb9jV56qYERvqd0fL8sGS6_K.01MwMDOxwCO1kjNzEzW}

- All we had to do was type **diff** and the paths of both the files to get the difference between them, which basically was that the 2nd file had an extra line which was the correct flag.


## What I learned

- Usage of **diff** to easily find what was difference between two files or what was added/changed/removed in a file.

