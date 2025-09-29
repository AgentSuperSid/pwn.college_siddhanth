# Mixing Globs
- This challenge expects us to use multiple globbing techniques to access the desired files in just one argument within 6 charecters length.

## My solve
**Flag:** `pwn.college{cvQvs279I9piSS_lFC_O2Y3raXv.QX1IDO0wCO1kjNzEzW}`

- First, as mentioned we should *cd* to */challenge/files*.
- Then run the program */challenge/run* with an argument such that only **challenging,educational,pwning** files are accessed.
- This is done by giving it the argument `[cep]*`.
- This would then give us the flag.
```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{cvQvs279I9piSS_lFC_O2Y3raXv.QX1IDO0wCO1kjNzEzW}
```


## Incorrect Tangents
- Instead of giving argument `[cep]*` i was giving `*[cep]` due to which the following error came
```bash
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *[cep]
Your expansion did not expand to the requested files (challenging, educational, 
pwning). Instead, it expanded to:
fantastic incredible nice optimistic
```
- These 3 words had **c** or **e** at the end.
- This made me realize that `*` was supposed to be used after `[cep]` to show that the initial letters of the required files are either **c,e or p** and then followed by any charecter(s).

## What I learned
- This challenge gave me a better understanding on the globbing concept and also made me better understand the `[]` usage.
