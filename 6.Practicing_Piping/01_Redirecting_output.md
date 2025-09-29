# Redirecting output
- This challenge expects us to redirect output into a file using `>`.

## My solve
**Flag:** `pwn.college{AYJnwYZPOXAqir7tAaphclFqX-4.QX0YTN0wCO1kjNzEzW}`

- - Type `echo PWN > COLLEGE`.
-  - `echo` prints **PWN** as the output which is needed to be redirected into **COLLEGE** file.
```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{AYJnwYZPOXAqir7tAaphclFqX-4.QX0YTN0wCO1kjNzEzW}
```

## What I learned 
- `>` can be used to redirect output of a program into another file which can be accessed uing **cat**.

