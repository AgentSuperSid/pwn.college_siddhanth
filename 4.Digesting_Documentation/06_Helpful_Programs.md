# Helpful Programs
- This challenge give us an introduction to use the **--help** argument to any argument to understand its usage.

## My solve
**Flag:** `pwn.college{IvsyxQ6S2szmL1VBgwQqZuabJTC.QX3IDO0wCO1kjNzEzW}`

- First type `/challenge/challenge --help` to get the list of legal arguments for **challenge/challenge**.
- The arguments were `-p` to print the value needed (621) to get the flag and `-g 621` to get the flag.
```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
  hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 621
hacker@man~helpful-programs:~$ /challenge/challenge -g 621
Correct usage! Your flag: pwn.college{IvsyxQ6S2szmL1VBgwQqZuabJTC.QX3IDO0wCO1kjNzEzW}
```

## What I learned
- Usage of **--help** argument and find the required argument to a given program to get the expected result.

## Incorrect Tangents
- I was doing a small typing error by missing the initial **/** in */challenge/challenge --help*.
