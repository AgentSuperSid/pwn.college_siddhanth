# Writing to multiple programs
- in this challenge we should duplicate the output of `/challenge/hack` into `/challenge/the` and `/challenge/planet`. Using **process substitution** and **piping**.

## My solve
**Flag:** `pwn.college{IPEKr6uYa5eGF8GqWmsail2rDBc.QXwgDN1wCO1kjNzEzW}`

- `tee` was used to duplicate output of `/challenge/hack` as input to `/challenge/the` and `/challenge/planet`.
- This is done by `/challenge/hack | tee >(/challenge/the) >(/challenge/planet)`
```bash
/challenge/hack | tee >(/challenge/the) >(/challeng
e/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
22038275813232624077
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{IPEKr6uYa5eGF8GqWmsail2rDBc.QXwgDN1wCO1kjNzEzW}
```
## What I learned 
- Using *process substitution* even for writing to commands.
