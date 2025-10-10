# Reading Shell Scripts
In this challenge we are supposed to find the password to `/challenge/run` to get the flag.

## My solve
**Flag:** `pwn.college{0R-d8vbooOT1a2t4WNnVvS2ful6.0lMwgDOxwCO1kjNzEzW}`

- We can find what is the expected password by reading the file, that is by `cat`.
- After reading the logic of the script we got to know that the password is `hack the PLANET`.
- Then by giving this as argument to `/challenge/run` after running it we will get the flag.
- First what I was doing was that I was giving the password as argument.
- Because while reading `/challenge/run` it had `$GUESS` and usually `$` meant it had contained the argument as I had seen in the previous challenges.
- Due to this I wasnt getting the flag for a long time.

```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{0R-d8vbooOT1a2t4WNnVvS2ful6.0lMwgDOxwCO1kjNzEzW}
```
