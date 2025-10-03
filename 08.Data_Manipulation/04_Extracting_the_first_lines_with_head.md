# Extracting the first lines with head
- In this challenge we are supposed to redirect the first 7 lines of the output of */challenge/pwn* into */challenge/college*.

## My solve
**Flag:** `pwn.college{suaddzFKQVRclREvze4TsE-Qjm1.0lNxEzNxwCO1kjNzEzW}`

- To access only the first 7 lines of the output of */challenge/pwn* we should use `head` with argument `-n 7`.
- Then by using `|` as we did on previous challenges, we will get the flag.
- This can be done using `/challenge/pwn | head -n 7 | /challenge/college`
```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{suaddzFKQVRclREvze4TsE-Qjm1.0lNxEzNxwCO1kjNzEzW}
```
