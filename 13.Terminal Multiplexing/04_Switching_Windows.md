# Switching Windows
In this challenge we are suppose dto open a window containing the flag.

## My solve
**Flag:** `pwn.college{csCwABD1_gI_mqxwsJDzjd76UmH.0FO4IDOxwCO1kjNzEzW}`

- First I checked which screen was detached, reattached it.
- Then opened the window 0 by typing `Ctrl-A` and `0`.
- This opened the window which had the flag.

```bash
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{csCwABD1_gI_mqxwsJDzjd76UmH.0FO4IDOxwCO1kjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{csCwABD1_gI_mqxwsJDzjd76UmH.0FO4IDOxwCO1kjNzEzW}
hacker@terminal-multiplexing~switching-windows:~$
```
