# Deleting newlines
- In this challenge we are supposed to delete all the newlines from the flag using `tr`.

## My solve
**Flag:** `pwn.college{0vshj051gQeaWxgfON5Z9kdhIHC.0VNxEzNxwCO1kjNzEzW}`

- In this challenge we have to use the same method we used for deleting charecters in the previous challenge but with newline `"\n"`.
- This is done by `/challenge/run | tr -d "\n"`

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{0vshj051gQeaWxgfON5Z9kdhIHC.0VNxEzNxwCO1kjNzEzW}
```
