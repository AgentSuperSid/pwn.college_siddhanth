# Translating characters
In this challenge we should invert the output of */challenge/run* to get the correct flag using `tr`.

## My solve
**Flag:** `pwn.college{YebVXO6AqNhNqlFZ70W8_yE6gD2.01MxEzNxwCO1kjNzEzW}`

- To inverse the case of the letters of the flag present in */challenge/run* should use `tr` with the argument `'A-Za-z' 'a-zA-Z'`. This is written as `/challenge/run | tr 'A-Za-z' 'a-zA-Z'`.
- This will directly give the output of */challenge/run* but the case of all the letters in its output will be inverted.
```bash
hacker@data~translating-characters:~$ /challenge/run | tr 'A-Za-z' 'a-zA-Z'
yOUR CASE-SWAPPED FLAG:
pwn.college{YebVXO6AqNhNqlFZ70W8_yE6gD2.01MxEzNxwCO1kjNzEzW}
```

## What I learned 
- We can use argument `'A-Za-z' 'a-zA-Z'` to `tr` to invert case of all the charecters in a text or comand output.

## References
https://www.shellscript.sh/examples/case/
