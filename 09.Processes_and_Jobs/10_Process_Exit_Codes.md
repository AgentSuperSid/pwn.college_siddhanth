# Process Exit Codes
In this challenge we should run *challenge/get-code* to get an error code and give it as argument to */challenge/submit-code* to get the flag
## My solve
**Flag:** `pwn.college{YK6j7Y23oA-GhHy6K6XMqAKJQJO.QX5YDO1wCO1kjNzEzW}`

- At first I thought that `$?` was a command and wondere what would happen if we run it directly rather than using `echo` as shown in the example.
- When I tried it came that `*error code* command not found`.
- Then I understood that `$?` is a pre-defined shell variable that holds the error code of the recently executed command.
- When you run it directly the shell will run the contained code as a command.

```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
35
hacker@processes~process-exit-codes:~$ /challenge/submit-code 35
CORRECT! Here is your flag:
pwn.college{YK6j7Y23oA-GhHy6K6XMqAKJQJO.QX5YDO1wCO1kjNzEzW}
```

## What I learned 
- While using `echo $?` commands that succeed typically return 0 and commands that fail typically return a non-zero value, most commonly 1 but sometimes an error code that identifies a specific failure mode.
- `$?` is just a shell variable that holds the exit code of the most recent command.
- If we just type `$?` in the terminal without `echo`, the shell will try to execute the value inside (like running a command with that number as its name).
