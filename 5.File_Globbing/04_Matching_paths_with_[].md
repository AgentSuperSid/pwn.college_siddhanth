# Matching paths with []
- This challenge expects us to run the */challenge/run* command taking the whole paths of these files as arguments using `[]`.

## My solve
**Flag:** `pwn.college{AZ1j_mjGbw4KwTUc9NBgrKkzo_3.QX0IDO0wCO1kjNzEzW}`

- We should run the `/challenge/run` command with the argument`/challenge/files/file_[bash]`.
- Here we are taking entire paths of all the 3 files within a single line using bracket-globs.
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{AZ1j_mjGbw4KwTUc9NBgrKkzo_3.QX0IDO0wCO1kjNzEzW}
```

## What I learned
- We can expand entire paths with globbing using `[]` for multiple files in just one line.
