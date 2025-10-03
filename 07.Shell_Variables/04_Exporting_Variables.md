# Exporting Variables
- In this challenge we are supposed to set the variables for *PWN* and *COLLEGE* while only exporting *PWN*.
## My solve
**Flag:** `pwn.college{wPYQuJKd1pnrpwynH3iqtRc8hsC.QXyYTN0wCO1kjNzEzW}`

- First we are supposed to initialize value *COLLEGE* to *PWN* and export it.
- This is done by `export PWN=COLLEGE`.
- Then we initialize value *PWN* to *COLLEGE* without exporting it.
- This is done by `COLLEGE=PWN`.
- Then by runnung */challenge/run* we will get the flag.
```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{wPYQuJKd1pnrpwynH3iqtRc8hsC.QXyYTN0wCO1kjNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

## What I learned 
- I learnt how `export` can be used to transfer the values of variables from main shell to its subshells.
