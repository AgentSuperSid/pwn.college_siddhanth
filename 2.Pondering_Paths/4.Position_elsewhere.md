# 4.Position elsewhere
-The process was similiar to the previous challenge

hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /proc/138/fd directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /proc/138/fd
hacker@paths~position-elsewhere:/proc/138/fd$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!

## Answer:
**Flag:** pwn.college{MLqurO09LEcXuPtQGgNchzVNC_A.QX3QTN0wCO1kjNzEzW}
