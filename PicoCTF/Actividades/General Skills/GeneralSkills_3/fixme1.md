## Descripción

Fix the syntax error in this Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)

Hints

1

Indentation is very meaningful in Python

2

To view the file in the webshell, do: `$ nano fixme1.py`

3

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

4

The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
Solo hay que acomodar el codigo que descargamos, nos dice que el error esta en la linea 20 del codigo
```
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3/fixme1]
└─$ python3 fixme1.py
  File "/home/kali/Projects/picoCTF/General_Skills3/fixme1/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent

```
Cuando abrimos abrimos el codigo vemos esto
```
import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) +>

  
flag = str_xor(flag_enc, 'enkidu')
     print('That is correct! Here\'s your flag: ' + flag)



```
El error que nos dice es en la parte del print, este debe de estar mas a la izquierda
```

  
flag = str_xor(flag_enc, 'enkidu')
print('That is correct! Here\'s your flag: ' + flag)

```
Con esto ya nos va a dar la bandera
```
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3/fixme1]
└─$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}

```
## Notas Adicionales 
## Referencias
