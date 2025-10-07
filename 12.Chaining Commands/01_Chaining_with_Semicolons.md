# Chaining with Semicolons
In this challenge we should execute 2 commands in a single prompt.

## My solve
**Flag:** `pwn.college{ILp6EQuti0N1li_T0PTfMhRJmB_.QX1UDO0wCO1kjNzEzW}`

- Here we just had to seperate the 2 commands with a `;` to execute both of them in  single prompt.
- I checked if the spaces before or after `;` mattered in the execution by leavind space before and not leaving space after `;` (opposite to what was shown in the example).
- Then I understood that it doesnt matter.

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn ;/challenge/college 
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{ILp6EQuti0N1li_T0PTfMhRJmB_.QX1UDO0wCO1kjNzEzW}
```
