# Printing Exported Variables
- In this challenge all we have to do is see all the exported variables using `env`.
## My solve
**Flag:** `pwn.college{UHGqQVKzttmey0eeLAHSO21NZeO.QX4UTN0wCO1kjNzEzW}`

- Just type `env`, it will display all the exported variables.
- One of them is the flag.
```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=e13374e0062755d2820613ca1b6f480c9ba9e558e2f4158e18eda6378a38fdf8
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{UHGqQVKzttmey0eeLAHSO21NZeO.QX4UTN0wCO1kjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```
