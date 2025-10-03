# Help for Builtins
- This challenge expects us to use the **help** builtin to find the usage for the required command.

## My solve
**Flag:** `pwn.college{s5sj8s3jA7OST4D7kO-W-e6S0oI.QX0ETO0wCO1kjNzEzW}`

- Run the **help** builtin and give the argument **challenge**.
- Here you dont need **/** before challenge because in this challenge **challenge** itself is also a builtin.
- This will give the list of required arguments.
- The required aregument is **--secret VALUE** where *VALUE* is "s5sj8s3j" which is given in the **help** list.
- Run `challenge --secret s5sj8s3j` to get the flag.
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "s5sj8s3j".
hacker@man~help-for-builtins:~$ challenge --secret s5sj8s3j
Correct! Here is your flag!
pwn.college{s5sj8s3jA7OST4D7kO-W-e6S0oI.QX0ETO0wCO1kjNzEzW}
```

