# Listing Processes
- In this challenge we should look for the program to run and get the flag by checking the running processes.

## My solve
**Flag:** `pwn.college{Az0lpxgUyup6_UvXk2XEMg62udy.QX4MDO0wCO1kjNzEzW}`

- I used `ps -ef` because I felt `ps aux` showed memory usage etc which I felt was unnecessary.
- After finding the programname under the *challenge* directory I ran it to get the flag.
- I didnt understand at first why did they say that process was sleeping and I also noticed that the terminal's command prompt was coming.
- After a bit of searching I understood that in order to maintain the process so that we can view it using `ps` it was put to sleep.
- Or else it would finish its process and exit. So it was put to sleep.
- Since the process didnt end, the cmd prmpt didnt come.

```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 17:46 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 17:46 ?        00:00:00 /run/dojo/bin/sleep 6h
root         131       1  0 17:46 ?        00:00:00 /challenge/15125-run-2331
root         134     131  0 17:46 ?        00:00:00 sleep 6h
hacker       136       0  0 17:47 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoin
hacker       142     136  0 17:47 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       153       0  0 18:05 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoin
hacker       159     153  0 18:05 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       168     159  0 18:05 pts/1    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/15125-run-2331
Yahaha, you found me! Here is your flag:
pwn.college{Az0lpxgUyup6_UvXk2XEMg62udy.QX4MDO0wCO1kjNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```
