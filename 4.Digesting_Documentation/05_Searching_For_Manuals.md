# Searching For Manuals
- This challenge expects us to find the hidden page of *challenge* by looking for the right command to display the *challenge* page and hence its right usage to print the flag.

## My solve
**Flag:** `pwn.college{k_yb5r4jdiZPjvn2lgKMl4mbT-H.QX2EDO0wCO1kjNzEzW}`

- First we have to look into the different arguments that can be used for *man* command using **man man**.
- Then try each of the initial arguments displayed in the page and give *challenge/challenge* as an argument to the argument.
- Here it was **man -k challenge/challenge**.
- Then it gave the argument to find the manual page for the **challenge** page which was **kybrjdijvn**.
- After opening the manual page we got to know the correct usage to get the flag-`/challenge/challenge --kybrjd 542`.
- This gave us the flag.
```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge/challenge
kybrjdijvn (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man kybrjdijvn
hacker@man~searching-for-manuals:~$ /challenge/challenge --kybrjd 542
Correct usage! Your flag: pwn.college{k_yb5r4jdiZPjvn2lgKMl4mbT-H.QX2EDO0wCO1kjNzEzW}
```

## What I learned 
- Usage of **man man** command and how to search for hidden pages of the manual.
