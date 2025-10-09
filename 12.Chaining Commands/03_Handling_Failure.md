# Handling Failure
In this challenge we should run two commands using `||`.

## My solve
**Flag:** `pwn.college{sC2LHxBdjpf2TC7NMjpturDQ-gK.01M0MDOxwCO1kjNzEzW}`

- Here the first command does not work but the second command works so by using `||` it still runs 2nd command even if 1st one fails.

```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{sC2LHxBdjpf2TC7NMjpturDQ-gK.01M0MDOxwCO1kjNzEzW}
hacker@chaining~handling-failure:~$ 
```

## What I learned 
- The `||` operator either runs first command or the second command depending on which one works, doesn't run both even if both works.
