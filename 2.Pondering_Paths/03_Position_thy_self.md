# 3.Position thy self
-In this challenge i learnt more in depth of how these directory paths work.

hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /doc
bash: cd: /doc: No such file or directory
hacker@paths~position-thy-self:~$ cd doc
bash: cd: doc: No such file or directory
hacker@paths~position-thy-self:~$ cd /usr/share/doc
hacker@paths~position-thy-self:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!


## Answer:
**Flag:** pwn.college{YeV9JetyXgphh3YUuhVawNak95A.QX2QTN0wCO1kjNzEzW}

##Incorrect Tangents
-I struggled initially to understand what they were telling in initially(that the directory they are showing is where we should go and then execute *challenge/run*)
-I was confused about the difference between *Relative* and *absolute* path cuz to try in relative path i typed directly doc and it was just saying that "*doc is a directory*". Then i understood that u should write **cd** for any changes in the directory and the **/** makes the difference in *absolute* and *relative* path.

##References
-Tutorial video of "The file system"
