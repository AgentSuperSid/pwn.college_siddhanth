# Storing Command Output
- In this challenge we are supposed to store the output of */challenge/run* to *PWN* and get the flag by reading its value.
## My solve
**Flag:** `pwn.college{ocWccE0aZRruF3w1sO8cOyCcFID.QX1cDN1wCO1kjNzEzW}`

- By following the SYNTAX mentioned in the exapmles to assign the output of commands as value to variable, we can do the same by `PWN=$(/challenge/run)`.
- Then to print the flag value stored in *PWN* by `echo $PWN`.
```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{ocWccE0aZRruF3w1sO8cOyCcFID.QX1cDN1wCO1kjNzEzW}
```
