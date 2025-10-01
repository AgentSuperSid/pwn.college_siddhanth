# Deleting charecters
- In this challenge we are supposed to delete unwanted charecters using `tr`.

## My solve
**Flag:** `pwn.college{wQZc5RPYqM__4j5x77L0M0EFkAr.0FNxEzNxwCO1kjNzEzW}`

- As following the example for syntax and for argument of `-d` we should use `""` since there are 2 charecters.
- So the command as whole will come as `/challenge/run | tr -d "^ %"`.
```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d "^ %"
Yourcharacter-stuffedflag:
pwn.college{wQZc5RPYqM__4j5x77L0M0EFkAr.0FNxEzNxwCO1kjNzEzW}
```

## What I learned 
- Argument `-d` to `tr` is used to delete charecters.
