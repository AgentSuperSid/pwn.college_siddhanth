# foregrounding Processes
In this challenge we shoudl run */challenge/run*, run it in `bg` and then in `fg` without suspending it again.

## My solve
**Flag:** `pwn.college{EYDL4jDrxgH9xs-PUN6dUfMJoky.QX4QDO0wCO1kjNzEzW}`

- I realized that after running the program in the background even though the cmd prmpt of the shell doesnt appear it will still take commands.
- Only thing is that in `fg` and `bg` you will have to press **Enter** to get the desired output.

```bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.
fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{EYDL4jDrxgH9xs-PUN6dUfMJoky.QX4QDO0wCO1kjNzEzW}
```
 
