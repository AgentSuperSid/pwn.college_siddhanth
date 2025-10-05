# Changing File Ownership
In this challenge we should set the owner for `not-the-flag` as `hacker`.

## My solve
**Flag:** `pwn.college{4R0OiYHNA2jBD-2upnT_wFluEkk.QXxEjN0wCO1kjNzEzW}`

- I tried in unprivileged mode, turns out that for this level it worked even for unprivileged mode.
- First I thought it was `/flag` itself that I should access. When I used `chown` it didnt give any error, only when I `cat` the file it said no such file.
- Then I did `ls` and then then found the flag-file name and continued.

```bash
hacker@permissions~changing-file-ownership:~$ ls
 COLLEGE   Desktop   PWN   cmd1_out   instructions   mkfifo   myflag   not-the-flag   stdout   the-flag  '~'
hacker@permissions~changing-file-ownership:~$ chown hacker not-the-flag
hacker@permissions~changing-file-ownership:~$ cat not-the-flag
pwn.college{4R0OiYHNA2jBD-2upnT_wFluEkk.QXxEjN0wCO1kjNzEzW}
```
## What I learned
- `chown` when used doesnt give error even if the file you typed doesnt exist.
