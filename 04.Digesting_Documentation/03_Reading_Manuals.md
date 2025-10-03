# Reading Manuals
- This challenge gives us the introduction to the **man** command.

## My Solve
```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --rirctu 000
Correct usage! Your flag: pwn.college{ArirRZIctuYlSaL0nXFbzWPaSXc.QX0EDO0wCO1kjNzEzW}
```
- We had to find what are the arguments we could give to the *challenge* command using **man** command taking *challenge* as argument.
- Then refering to the manual we executed the program */challenge/challenge --rirctu 000* to get the flag.

## Answer

**Flag:** `pwn.college{ArirRZIctuYlSaL0nXFbzWPaSXc.QX0EDO0wCO1kjNzEzW}`

## What I learned

- How to use the manual using the **man** command to learn the usage of different commands and the arguments that can be applied to them.
