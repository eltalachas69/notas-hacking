## Descripción
Can you crack the password to get the flag? Download the password checker [here](https://challenge-files.cylabacademy.net/library/a2b32b2b4b000d12f209c65a2c414ede32d08a63774f7e150e3e30a3892a386d/level5.py) and you'll need the encrypted [flag](https://challenge-files.cylabacademy.net/library/a2b32b2b4b000d12f209c65a2c414ede32d08a63774f7e150e3e30a3892a386d/level5.flag.txt.enc) and the [hash](https://challenge-files.cylabacademy.net/library/a2b32b2b4b000d12f209c65a2c414ede32d08a63774f7e150e3e30a3892a386d/level5.hash.bin) in the same directory too. Here's a [dictionary](https://challenge-files.cylabacademy.net/library/a2b32b2b4b000d12f209c65a2c414ede32d08a63774f7e150e3e30a3892a386d/dictionary.txt) with all possible passwords based on the password conventions we've seen so far.
## Solución
Para esto se nos dio la lista de contraseñas en un txt pero pues simplemente se puso esas contraseñas en una lista y pues basicamente como los ejemplos anteriores se hizo un for y la que era correcta la devolvia y pues con eso ya me dio la bandera que es `academy{h45h_sl1ng1ng_27d64792}`

Codigo:
```
import hashlib

  

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################

def str_xor(secret, key):

#extend key to secret length

new_key = key

i = 0

while len(new_key) < len(secret):

new_key = new_key + key[i]

i = (i + 1) % len(key)

return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])

###############################################################################

  

flag_enc = open('level5.flag.txt.enc', 'rb').read()

correct_pw_hash = open('level5.hash.bin', 'rb').read()

lista_contraseña = open('dictionary.txt', 'r').read().splitlines()

  
  

def hash_pw(pw_str):

pw_bytes = bytearray()

pw_bytes.extend(pw_str.encode())

m = hashlib.md5()

m.update(pw_bytes)

return m.digest()

  
  

def level_5_pw_check():

for contraseña in lista_contraseña:

contraseñahash = hash_pw(contraseña)

if contraseñahash == correct_pw_hash:

print(contraseña)

user_pw = input("Please enter correct password for flag: ")

user_pw_hash = hash_pw(user_pw)

if( user_pw_hash == correct_pw_hash ):

print("Welcome back... your flag, user:")

decryption = str_xor(flag_enc.decode(), user_pw)

print(decryption)

return

print("That password is incorrect")

  
  
  

level_5_pw_check()
```

Terminal:
```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/general-skills/puton5]
└─$ python3 level5.py
eee0
Please enter correct password for flag: eee0
Welcome back... your flag, user:
academy{h45h_sl1ng1ng_27d64792}
```
## Notas Adicionales 
## Referencias
