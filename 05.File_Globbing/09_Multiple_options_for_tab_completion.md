# Multiple options for tab completion
- Use **tab** to check all the files present and autocomplete using the same.

## My solve
**Flag:** `pwn.college{IoXEDLuYFx7inwLi9waIEG2Ur8f.0lN0EzNxwCO1kjNzEzW}`

- First type `cat /challenge/files/p` and press **tab**. It will complete to pwn.
- Then from there you should check for all the files present to be readable by pressing **tab** again.
- Then by trial and error we get the flag for `cat /challenge/files/pwncollege-flag`.
```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{IoXEDLuYFx7inwLi9waIEG2Ur8f.0lN0EzNxwCO1kjNzEzW}
```

## What I learned 
- While autocompleting if there are multiple files with the same first charecters while u press **tab** it gives the list of all the files starting with those charecters.

## Incorrect tangents 
- I missed the **cat** command in the beginning, due to which I wasnt getting the flag for any of those files.
