# NewGenPass
For generating your password generator bookmarklet.

Many years ago I started using Chris Zarate's [GenPass](https://genpass.supergenpass.com/) bookmarklet. Supergenpass superceded it, but there were some [security concerns](https://akibjorklund.com/2009/supergenpass-is-not-that-secure) at the time because it is part of the DOM. The issue had been resolved, but I got used to GenPass and preferred its simplicity. All code is included in the bookmarklet. SuperGenPass pulls in external resources including scripts over insecure http and reports statistics. GenPass also has a weakness because you enter the master password in a plaintext [prompt()](https://www.w3schools.com/JSREF/met_win_prompt.asp), so just make sure nobody is watching your screen. Unfortunately that is just how the prompt() function works. There is no way around it except making the dialog part of the DOM.
GenPass has some limitations, for example generated passwords may not be accepted because they do not contain any special characters. Also, sometimes it fails to find the password box so you have to copy/paste it manually.

So I decided to write my own version, based on the simple but effective [Fowler-Noll-Vo hash function](https://en.wikipedia.org/wiki/Fowler–Noll–Vo_hash_function). I chose the 128-bit [FNV-1a](https://en.wikipedia.org/wiki/Fowler–Noll–Vo_hash_function#FNV-1a_hash) that gives enough bits to generate password hashes up to 21 characters.

Credits to Chris Zarate for the original GenPass script.
# Usage
Download the newgenpass.html to your pc and open it locally, or [just click here](https://ploink.github.io/NewGenPass/newgenpass.html).
