# Multi-word Variables
- In this challenge we should store the value **COLLEGE YEAH** in *PWN*.
## My solve
**Flag:** `pwn.college{ME_3Pu-Qllodstxp7PiI_1Qzw6P.QXwYTN0wCO1kjNzEzW}`

- We should do the same thing as last challenge but here for the value we should write `"COLLEGE YEAH"`.
- This can be written as PWN="COLLEGE YEAH".
- This wasy the shell will consider `COLLEGE YEAH` as one unit.
```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{ME_3Pu-Qllodstxp7PiI_1Qzw6P.QXwYTN0wCO1kjNzEzW}
```

## What I learned 
- Usage of `""` to be able to store multi-word values to variables.
