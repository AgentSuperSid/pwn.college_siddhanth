# matching with []
- In this challenge we are supposed to access multiple files using `[]`.

## My solve
**Flag:** `pwn.college{Y73kRhN5E9H4iNeAwpkD-WIRM3n.QXzIDO0wCO1kjNzEzW}`

- First as they mentioned, we should change dir. to */challenge/files*.
- Then to access the files we should type `/challenge/run file_[bash]`.
- This will give us the flag.
```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{Y73kRhN5E9H4iNeAwpkD-WIRM3n.QXzIDO0wCO1kjNzEzW}
```

## What I learned
- The usage of `[]` in the file globbing concept.
