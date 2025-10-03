# Exclusionary Globbing
- Usage of `^` and `!` in `[]` to access specific files not having the charecters specified inside `[]` glob.

## My solve
**Flag:** `pwn.college{s8eXFpMu7AwmhHkH4Go7rtM1dGV.QX2IDO0wCO1kjNzEzW}`

- `cd` to */challenge/files*.
- Run */challenge/run* with the argument `[!pwn]*`.
- This will help us access all files not having their starting charecter **p** or **w** or **n**.
- Then we will get our flag.
```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{s8eXFpMu7AwmhHkH4Go7rtM1dGV.QX2IDO0wCO1kjNzEzW}
```

## What I learned 
- The usage of **!** and **^** in the `[]` globbing, which can be used to forbid accessing the files having those charecters in their name.

## Incorrect Tangents
- In the argument i was forgetting `*` in `[!pwn]*` which would prevent accessing even the files which we needed.
- It was restricting to only accessing files having names only **p** or **w** or **n**.
