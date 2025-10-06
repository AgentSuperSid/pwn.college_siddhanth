# Changing Permissions
In this challenge we are supposed to get reading permission to the flag file adn read the flag without changing the owner of the file.

## My solve
**Flag:** `pwn.college{o2oBt5pRzRyX5aoBTcGqzWKcpXt.QXzcjM1wCO1kjNzEzW}`

- At the beginning I was struggling a bit in giving the argument to `chmod` how to give the users access.
- Then after understanding its usage by reading from the `man` command I understood how to use it.
- TO prevent any kind of confusion I gave everyone the permission to read the flag file. Thus being `a+r`.

```bash
hacker@permissions~changing-permissions:~$ chmod a+r not-the-flag
hacker@permissions~changing-permissions:~$ cat not-the-flag
pwn.college{o2oBt5pRzRyX5aoBTcGqzWKcpXt.QXzcjM1wCO1kjNzEzW}
```

## What I learned 
- Better understanding of the way to give arguments to commands like `chmod` to get the necessary access to a file.
