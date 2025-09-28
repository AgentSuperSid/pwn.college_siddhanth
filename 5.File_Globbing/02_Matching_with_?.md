# Matching with ?
- Usage of `?` to substitute **c** and **l** from */challenge* and then run the required program.

## My solve
**Flag:** `pwn.college{E-RhpDAJ5I8bRPLcLJaTp4LS21W.QXyIDO0wCO1kjNzEzW}`

- First substitute all **c** and **l** in challenge with `?` and then do **cd**, that is- `cd /?ha??enge`.
- Then run the program **/challenge/run** to get the flag.
```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{E-RhpDAJ5I8bRPLcLJaTp4LS21W.QXyIDO0wCO1kjNzEzW}
```

## What I learned
- We can use `?` as a substitution for only one charecter each while running a command.
