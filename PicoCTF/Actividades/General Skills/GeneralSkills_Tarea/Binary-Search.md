## Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.

Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/20/challenge.zip)
## Solución
Es facil, ingresamos un numero del 1 al 1000, entonces simplemente lo dividimos de mitad a mitad hasta que lleguemos al numero que piensa
```
                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Binary_Search/home/ctf-player/drop-in]
└─$ ssh -p 56927 ctf-player@atlas.picoctf.net 
The authenticity of host '[atlas.picoctf.net]:56927 ([18.217.83.136]:56927)' can't be established.
ED25519 key fingerprint is: SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:56927' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 250
Lower! Try again.
Enter your guess: 125
Higher! Try again.
Enter your guess: 150
Higher! Try again.
Enter your guess: 180
Higher! Try again.
Enter your guess: 200
Lower! Try again.
Enter your guess: 195
Lower! Try again.
Enter your guess: 190
Higher! Try again.
Enter your guess: 192
Congratulations! You guessed the correct number: 192
Here's your flag: picoCTF{g00d_gu355_bee04a2a}
Connection to atlas.picoctf.net closed.

```
## Notas Adicionales 
## Referencias
