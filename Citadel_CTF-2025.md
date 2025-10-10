# Citadel CTF challenges
- This includes some challenges which I had solved or assisted to solve

# track 8
Bypassing the second chamber leads to an empty floor except for a single artifact in the center: an old MP3 player, scratched and worn. On its surface, a cipher is etched, a message left behind for anyone who can decode it:

`twj eys zpr ukm 'viamnwqw' bx lzgo: esmqqui{yyr_oshwwcm_bwupa}`
When you power it on, the sound fills the chamber. The tracks play like whispers from a lost world, and you recognize it as a song from Panchiko’s latest studio album, particularly track no. 8. Its title feels familiar, hinting at a famous cipher. Decrypt it by using the album name as your key and continue your ascent.

## Solve
- First I did a little research about the **Panchiko** rock band and found out that the Album they were referring to was named *Vinegar*.
- Since this was a decryption quetion which means with had to decipher it using some method, it closely resembled to the word *Vigenère* which is a ciphering method.
- Once it was deciphered we get the answer as `citadel{add_vinegar_twice}`.
- **Flag:** `citadel{add_vinegar_twice}`

# The Ripper
The guardian of this floor steps from the shadows. Known only as Jack the Ripper, he watches you carefully. He proclaims himself merciful and hands you a word list to help. He asks you to find the passcode hidden in this hash $2a$04$RNoyoWAcW0StwSri4YN1Eeb2j1gBNKutDOMxsLzfyfSvB/ghMHToa. The word list is your only aid. Only by combining the two correctly can you uncover the key and move on to the next floor.

## Solve
- The name and the format gave the clue that we had to use `John the ripper` program to find the correct flag.
- We redirected the output of  `$2a$04$RNoyoWAcW0StwSri4YN1Eeb2j1gBNKutDOMxsLzfyfSvB/ghMHToa` to a text file called `hash`.
- The normal method was used, `john --wordlist="/mnt/c/Users/Anvitha/OneDrive/Desktop/wordlist.txt" --format=bcrypt "/mnt/c/Users/Anvitha/OneDrive/Desktop/hash.txt"` for the program to access the file.
- Then `john --show "/mnt/c/Users/Anvitha/OneDrive/Desktop/hash.txt"` to show us the flag.
- It showed the password of a user something like `fake_flag_4_fake_pl4y3rs` which was supposed to be the part inside `{}` of the flag.
- **Flag:** `citadel{fake_flag_4_fake_pl4y3rs}`

## What I learned
- I saw the vast world of CTF and there were so many things to learn and use to solve these interesting and unique challenges.
- Learnt to use many new tools like `Burp`, `IDA`, `John the Ripper` etc.
