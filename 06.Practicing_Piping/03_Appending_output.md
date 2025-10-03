# Appending output
- Thic challenge expects us to first append the */challenge/run* output into */home/hacker/the-flag* and then the `cat` output of that should be appended to *stdout*.

## My solve
**Flag:** `pwn.college{cTY11TRSEWkGb76nRoTmUED_ZX9.QX3ATO0wCO1kjNzEzW}`

- First we should redirect the output of */challenge/run* into */home/hacker/the-flag* file.
- Then redirect the output of `cat /home/hacker/the-flag` into **stdout**.
- What actually happens is that when the second command is given **stdout** file is created and programed in such a way that after appending properly, the second half appends to the first half.
- Else it would just contain the second half.
```bash
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
the first write directly to the file, and the second write, I'll do to stdout 
(if it's pointing at the file). If you redirect the output in append mode, the 
second write will append to (rather than overwrite) the first write, and you'll 
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag >>stdout
hacker@piping~appending-output:~$ cat stdout
 | 
\|/ This is the first half:
 v 
pwn.college{cTY11TRSEWkGb76nRoTmUED_ZX9.QX3ATO0wCO1kjNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
```

## Incorrect tangents 
- I tried to redirect the output of **stdout** to **/home/hacker/the-flag**. Then this error came:
```bash
hacker@piping~appending-output:~$ cat stdout >> /home/hacker/t
he-flag
cat: stdout: No such file or directory
```
- Then I realised that it should be the other way around.

## References
The explanation given by chatGPT on the concept of appending and how it works in linux.
