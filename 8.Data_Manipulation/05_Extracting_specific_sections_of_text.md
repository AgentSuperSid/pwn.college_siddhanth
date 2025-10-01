# Extracting specific sections of text
- In this challenge we should format the output of */challenge/run* in such a way that we get the flag only as output.

## My solve
**Flag:** `pwn.college{M8pReWtYcw2ZkAwKbMitUytb6yF.01NxEzNxwCO1kjNzEzW}`

- First we have to remove the first column of the output containing random numbers. Then we should make the entire flag come in 1 line by removing all the unnecessary newlines.
- This can be done by `/challenge/run | cut -d " " -f 2 | tr -d "\n"`.
- This will give us the formated flag.
- Here first `cut -d " " -f 2` will only transfer the 2nd column of the output to the next command through piping, then `tr -d "\n"` removes all the newlines. 
```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{M8pReWtYcw2ZkAwKbMitUytb6yF.01NxEzNxwCO1kjNzEzW}
```
