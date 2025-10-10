# Scripting with Multiple Conditions
In this challenge we should give input and output statements for multiple cases.

## My solve
**Flag:** `pwn.college{MEHhM7OrtWsSwfQ9GqLtj3elBkU.0FOzMDOxwCO1kjNzEzW}`

- I used the `elif` as they instructed
- For the last case (print "unknown" for foo) since it was last I felt it wasnt necessary to do `elif` so I just did `else`.
- Otherwise it is very similiar to the previous challenges but repeated `elif`s
```bash
  GNU nano 8.4                                                         solve.sh                                                                   
#!/bin/bash

if [ "$1" == "hack" ]
then
 echo the planet
elif [ "$1" == "pwn" ]
then
 echo college
elif [ "$1" == "learn" ]
then
 echo linux
else
echo unknown
fi

```
```bash
hacker@chaining~scripting-with-multiple-conditions:~$ nano solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{MEHhM7OrtWsSwfQ9GqLtj3elBkU.0FOzMDOxwCO1kjNzEzW}
```

## What I learned
using `elif` for multiple conditions
