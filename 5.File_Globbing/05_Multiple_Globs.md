# Multiple Globs
- This challenge expects us to access all the files in the *challenge/files* dir. having **p** in their names.

## My solve
**Flag:** `pwn.college{460zBPYTHE5d9MhmR2UIHSpQNy1.0lM3kjNxwCO1kjNzEzW}`

- As they mentioned, first we should go to */challenge/files* dir.
- Then write the command `/challenge/run *p*`.
-  The argument `*p*` will cover all the files which has the letter **p** in their names.
```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ ls
amazing    challenging  educational  great  incredible  kind      magical  optimistic  queenly  splendid   uplifting   wonderful  youthful
beautiful  delightful   fantastic    happy  jovial      laughing  nice     pwning      radiant  thrilling  victorious  xenial     zesty
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{460zBPYTHE5d9MhmR2UIHSpQNy1.0lM3kjNxwCO1kjNzEzW}
```

