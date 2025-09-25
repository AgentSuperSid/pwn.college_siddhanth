# An Epic Filesystem Quest
- This challenge tests all the commands we learnt in this module till now in the form of a fun and interesting quest.

## My Solve

hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
NOTE  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ cat flag
cat: flag: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cat NOTE
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/include/config/arch/has/ubsan/sanitize

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/include/config/arch/has/ubsan/sanitize
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/arch/has/ubsan/sanitize$ ls
TRACE  all.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/arch/has/ubsan/sanitize$ cat TRACE
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/arch/powerpc/mm

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/arch/has/ubsan/sanitize$ cd /
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/arch/powerpc/mm

Thacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/stdlib/2and3/ensurepip$ cat INFO
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/Documentation/devicetree/bindings/net

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/stdlib/2and3/ensurepip$ cat /opt/linux/linux-5.4/Documentation/devicetree/bindings/net
cat: /opt/linux/linux-5.4/Documentation/devicetree/bindings/net: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/stdlib/2and3/ensurepip$ ls /opt/linux/linux-5.4/Documentation/devicetree/bindings/net
SNIPPET-TRAPPED                 cavium-mix.txt               hisilicon-hns-dsaf.txt       mdio.yaml                renesas,ravb.txt
adi,adin.yaml                   cavium-pip.txt               hisilicon-hns-mdio.txt       mediatek,mt7620-gsw.txt  rockchip-dwmac.txt
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/jedi/third_party/typeshed/stdlib/2and3/ensurepip$ cat /opt/linux/linux-5.4/Documentation/devicetree/bindings/net/SNIPPET-TRAPPED
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/dma/ipu


## Answer
**Flag:** pwn.college{ATqpWeGJIUer0Yg9Ii2KF8Ny2gt.QX5IDO0wCO1kjNzEzW}


-Here I had to use all the commands and different cases that I had learnt till now in this module like finding hidden file, accessing files without changing to the file directory looking for clue after clue till I found the flag.
-Some files were **hidden**, so we had to first check the filename with *ls -a* and then access using *cat*.
-In case of **delayed** files, we had to *cd* to the file directory and then read it with *cat*.
-In one case, the file was **trapped**, that is, if we went to the file directory using *cd* the file would be destroyed, so we had to *ls* the files and *cat* the required file by accessing it from the root (*/*) directory itself.


## What I learned
- This challenge reinforced my knowledge of the different commands in this module and got a better idea in the application of all the commands in different scenarios.
- It also thought me a bit of patience and persistence.