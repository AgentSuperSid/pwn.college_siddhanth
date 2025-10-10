# Scripting with Default Cases
In this challenge we should do the same as previous challenge but with a default case.

## My solve
**Flag:** `pwn.college{gNVIncQ0j9SOh99HyCXX-bWAn5n.01NzMDOxwCO1kjNzEzW}`

- Here we are supposed to give `else` case to cover default cases.
- So we should just add the `else` statement with `echo nope`.
- This will give us the flag when we run `/challenge/run`.

```bash
  GNU nano 8.4                                                         solve.sh                                                                   
#!/bin/bash

if [ "$1" == "pwn" ]
then
 echo college
else
echo nope
fi
```
```bash
hacker@chaining~scripting-with-default-cases:~$ nano solve.sh
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{gNVIncQ0j9SOh99HyCXX-bWAn5n.01NzMDOxwCO1kjNzEzW}
```

## What I learned 
Using `else` for default cases
