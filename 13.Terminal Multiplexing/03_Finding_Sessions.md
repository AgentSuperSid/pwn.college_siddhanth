# Finding Sessions
In this challenge we have to search for the screen having the flag.

## My solve
**Flag:** `pwn.college{ktsQeHOe63vYK4SqE2WdpOTnd3a.01N4IDOxwCO1kjNzEzW}`

- When I checked the screen names and PIDs using `screen -ls` there were 2 screens saying (remote or dead) so I ignored them.
- Then there were 3 of them remaining.
- I opend and closed the first one using `screen -r 144` and closed using `Ctrl+A` and d.
- Second one (PID 147) had the flag.

```bash
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{ktsQeHOe63vYK4SqE2WdpOTnd3a.01N4IDOxwCO1kjNzEzW}
pwn.college{ktsQeHOe63vYK4SqE2WdpOTnd3a.01N4IDOxwCO1kjNzEzW}
hacker@terminal-multiplexing~finding-sessions:~$
```
