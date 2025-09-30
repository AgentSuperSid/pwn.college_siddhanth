# Process substitution for input
In this challenge we are supposed to differenciate between the 2 given commands using `diff` and **process substitution**.

## My solve
**Flag:** `pwn.college{cKKR3r65byJdbhoL-juX7PQIUYx.0lNwMDOxwCO1kjNzEzW}`

- All we have to do is differenctiate between the given two commands using `diff` and by **process substitution**.
- This is done by `diff  <(/challenge/print_decoys)  <(/challenge/print_decoys_and_flag)`.
- The *process substitution* replaces the named pipe connected to the command's output, reading the standard output of the command.
```bash
hacker@piping~process-substitution-for-input:~$ diff  <(/challenge/print_decoys)  <(/ch
allenge/print_decoys_and_flag)
6a7
> pwn.college{cKKR3r65byJdbhoL-juX7PQIUYx.0lNwMDOxwCO1kjNzEzW}
```

## What I learned 
- I understood the usage of *process substitution* and its application.
