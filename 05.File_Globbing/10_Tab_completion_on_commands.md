# Tab completion on commands
- In this challenge we are supposed to autocomplete commands using **tab**.

## My solve
**Flag:** `pwn.college{IwpiV4LkGswRd4kGTew8zLbCMwD.0VN0EzNxwCO1kjNzEzW}`

- Typed "pwn.co" and pressed **tab**.It got autocompleted to `pwncollege-4003`. Then pressed it again to see if there are other options.
- Saw that there were extra argument options. `not-the-flag` arument caught my eye and the name made me curious to try it first.
- Turns out that it gave the correct flag.
```bash
acker@globbing~tab-completion-on-commands:~$ pwncollege-4003 
.ICEauthority  .cache/        .dbus/         .lesshst       Desktop/       ~/             
.bash_history  .config/       .idapro/       .local/        not-the-flag   
hacker@globbing~tab-completion-on-commands:~$ pwncollege-4003 not-the-flag 
Correct! Here is your flag:
pwn.college{IwpiV4LkGswRd4kGTew8zLbCMwD.0VN0EzNxwCO1kjNzEzW}
```

