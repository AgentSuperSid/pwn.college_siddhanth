# Split piping stderr and stdout
In this challenge your supposed to apply the concepts you learnt in this module till now.

## My solve
**Flag:** `pwn.college{k-mNWeuU5mEacTe3e1urbYh7XLK.QXxQDM2wCO1kjNzEzW}`

- We have to do both the stderr for `/challenge/the` and stdout for `/challenge/planet` .
- So for stderr we can do `/challenge/hack 2> >(/challenge/the)` which will store the errors and for stdout we can do normal `>` usage with `>()`.
- So the command will come as `/challenge/hack 2> >(/challenge/the) > >(/challenge/planet)`.
- 
```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) > >(/challenge/planet)
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{k-mNWeuU5mEacTe3e1urbYh7XLK.QXxQDM2wCO1kjNzEzW}
```

## What I learned 
- In standard error rather than using `cmd_1 2>&1 | cmd_2` u can do `cmd_1 2> >(cmd_2)`.

## Incorrect tangents
- I was messing up in the error part in the usage of `2> &1 |` and `2> `
