# Finding Commands
In this challenge we should find the path of `win` command, where the flag file is and `cat` that file.

## My solve
**Flag:** `pwn.college{IVOZi9e1M_QdGXoX1Gk_fHJvCB-.01NzEzNxwCO1kjNzEzW}`

- First I checked the path of `win` commandusing `which`.
- Then I `cd` to that directory where `win` is present(and so is the flag).
- Then I read the falg file using `cat`.
- I could have directly read it without `cd` but I still went with it.

```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/20528/win
hacker@path~finding-commands:~$ cd /challenge/paths/20528
hacker@path~finding-commands:/challenge/paths/20528$ ls
flag  win
hacker@path~finding-commands:/challenge/paths/20528$ cat flag
pwn.college{IVOZi9e1M_QdGXoX1Gk_fHJvCB-.01NzEzNxwCO1kjNzEzW}
hacker@path~finding-commands:/challenge/paths/20528$
```

## What I learned 
- Using `which` command
