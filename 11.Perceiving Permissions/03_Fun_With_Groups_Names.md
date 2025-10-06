# Fun_With_Groups_Names
In this challenge we are supposed to find the group we are in and then with that group name we should change the accessibility to the flag file.

## My solve
**Flag:** `pwn.college{Mm5YLxlHJ7ISSwlCHfgA8duvaIa.QXycjM1wCO1kjNzEzW}`

- I just followed as they said, used `id` to see the group name Im in.
- Then did the same thing we did in the last challenge but this time the group name was `grp25737` and not `Hacker`.

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp25737) groups=1000(grp25737)
hacker@permissions~fun-with-groups-names:~$ chgrp grp25737 not-the-flag
hacker@permissions~fun-with-groups-names:~$ cat not-the-flag
pwn.college{Mm5YLxlHJ7ISSwlCHfgA8duvaIa.QXycjM1wCO1kjNzEzW}
```
