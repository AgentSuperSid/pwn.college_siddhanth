# Reading Input
- In this challenge we should give the value to *PWN* as college manually.
## My solve
**Flag:** `pwn.college{8Z2tN_7s0GZQ5x1MmouiuiIdGT4.QX4cTN0wCO1kjNzEzW}`

- First we should type `read PWN`.
- This will give a prompt to input a value, where we should type `COLLEGE`.
- This will give us the flag.
  
```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8Z2tN_7s0GZQ5x1MmouiuiIdGT4.QX4cTN0wCO1kjNzEzW}
```

## What I learned 
- How to use `read` and the usage of `-p` within `read`.
