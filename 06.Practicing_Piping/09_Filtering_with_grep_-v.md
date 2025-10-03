# Filtering with grep -v
This challenge expects us to find the real flag form the text output redirected by */challenge/run*.


## My solve
**Flag:** `pwn.college{Embi-Tqb76UsOJ4NJfTBjwgY_AF.0FOxEzNxwCO1kjNzEzW}`

- The command is pretty much the same as previous challenges but the difference is that `grep` has to be used with `-v` with argument **DECOY**.
- This searches for the lines not having **DECOY**.
- This can be done by `/challenge/run | grep -v DECOY`. This will directly give the flag.
```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{Embi-Tqb76UsOJ4NJfTBjwgY_AF.0FOxEzNxwCO1kjNzEzW}
```

## What I learned 
Usage of `-v` in `grep` command.
