# 5.Postion yet elsewhere

hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var/log directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /var/log/challenge/run
bash: cd: /var/log/challenge/run: No such file or directory
hacker@paths~position-yet-elsewhere:~$ cd /var/log
hacker@paths~position-yet-elsewhere:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!

-This time i just tried to do the entire thing in 1 line. Then i understood that /challenge/run is a program in log, just another directory.

 ## Answer:
**Flag:** pwn.college{EiVLw5puutgTiRbUNQ1_eJUw_lo.QX4QTN0wCO1kjNzEzW}
