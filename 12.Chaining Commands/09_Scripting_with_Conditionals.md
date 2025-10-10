# Scripting with Conditionals
In this challenge we have to output *college* for *pwn* input, else nothing in script.

## My solve
**Flag:** `pwn.college{YGxdrQkgjVBFwa0caT_J3bhT-x0.0lNzMDOxwCO1kjNzEzW}`

- In my first attempt I checked if the space between `"$1"`,`==` and `pwn` needed.
- Then I understood that if the space is not given, for any input it will give the output *college*.
- Then everything was done in the format shown in the examples.
- This gave me the flag.

```bash
  GNU nano 8.4                                                         solve.sh                                                                   
#!/bin/bash

if [ "$1" == "pwn" ]
then
 echo college
fi
```
```bash
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{YGxdrQkgjVBFwa0caT_J3bhT-x0.0lNzMDOxwCO1kjNzEzW}
hacker@chaining~scripting-with-conditionals:~$ 
```

## What I learned 
using `if` logic in script.
