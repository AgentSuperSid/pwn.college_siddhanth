# Redirecting Input
- In this challenge we are supposed to redirect input from *PWN* to */challenge/college* and then again do the same but *PWN* should contain **COLLEGE** in it to get required output.

## My solve
**Flag:** `pwn.college{EUUEF8YY7UvsGkgzL9PCmSOuAtD.QXwcTN0wCO1kjNzEzW}`

- First type `/challenge/run > PWN`. This will create *PWN* and redirect some output.
- Then Change the contents in *PWN* to **COLLEGE** using `echo`. That is `echo COLLEGE > PWN`.
- After this redirect the file's input back to */challenge/run*. This will satisfy their condition and store the flag in *PWN*.
- Then the flag can be accesses by using `cat`.
```bash
hacker@piping~redirecting-input:~$ /challenge/run > PWN
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{EUUEF8YY7UvsGkgzL9PCmSOuAtD.QXwcTN0wCO1kjNzEzW}
```

