# Searching Manuals
- This challenge teaches us to find the required argument for the program *challenge* using the manual when there are too many argument options.

## My solve
- First, as done in previous challenge, using **man** command we checked all the arguments of *challenge* program.
- Then we should use **/** to search for anything related to **flag** in the manual to get all the **flag** words in the manual.
- Then use **n** to go to the next **flag** till you get the necessary argument.
- Then press **q** to exit manual and then execute the program

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --wcbmdmm
Initializing...
Correct usage! Your flag: pwn.college{4WQ2LFEsJeptS21foGZbnh5wmvz.QX1EDO0wCO1kjNzEzW}
```

## Answer
**Flag:** `pwn.college{4WQ2LFEsJeptS21foGZbnh5wmvz.QX1EDO0wCO1kjNzEzW}`

## What I learned (optional)
- i learnt the usage of **/**,**n** and **N** in the manual.

