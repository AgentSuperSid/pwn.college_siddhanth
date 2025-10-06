# Citadel CTF challenges
- This includes some challenges which I had solved or assisted to solve

## track 8
twj eys zpr ukm 'viamnwqw' bx lzgo: esmqqui{yyr_oshwwcm_bwupa} 
The tracks play like whispers from a lost world, and you recognize it as a song from Panchiko’s latest studio album, particularly track no. 8. 
Its title feels familiar, hinting at a famous cipher. Decrypt it by using the album name as your key and continue your ascent.

- First I did a little research about the **Panchiko** rock band and found out that the Album they were referring to was named *Vinegar*.
- Since this was a decryption quetion which means with had to decipher it using some method, it closely resembled to the word *Vigenère* which is a ciphering method.
- Once it was deciphered we get the answer as `citadel{add_vinegar_twice}`.

## The Ripper
It was a challenge where there was a gaurdian named **John** and he gave us 2 files, a word list and `$2a$04$RNoyoWAcW0StwSri4YN1Eeb2j1gBNKutDOMxsLzfyfSvB/ghMHToa` with which we had to find the flag.

- The name and the format gave the clue that we had to use `John the ripper` program to find the correct flag.
- We redirected the output of  `$2a$04$RNoyoWAcW0StwSri4YN1Eeb2j1gBNKutDOMxsLzfyfSvB/ghMHToa` to a text file called `hash`.
- The normal method was used, `john --wordlist="/mnt/c/Users/Anvitha/OneDrive/Desktop/wordlist.txt" --format=bcrypt "/mnt/c/Users/Anvitha/OneDrive/Desktop/hash.txt"` for the program to access the file.
- Then `john --show "/mnt/c/Users/Anvitha/OneDrive/Desktop/hash.txt"` to show us the flag.
- It showed the password of a user something like `fake_flag_4_f4ke_players` which was supposed to be the part inside `{}` of the flag.

## What I learnered
- I saw the vast world of CTF and there were so many things to learn and use to solve these interesting and unique challenges.
- How teeamwork plays an important role in these challenges.
- Learnt to use many new tools like `Burp`, `IDA` etc.
