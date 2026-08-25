## Descripción
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
## Solución
Lo que hice en este caso fue denuevo checar el codigo con `nano` y vi que la contraseña era caracteres hexadecimales, entonces lo que hice fue que en el mismo codigo los decodifique y me los imprima para saber cual es la contraseña
```
def level_2_pw_check():
    hexadecimal = "64653736"
    texto = bytes.fromhex(hexadecimal).decode('utf-8')
    print(texto)
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):

```
Me dio la contraseña y asi pude saber la bandera
```
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3/PW-Crack-2]
└─$ python3 level2.py
de76
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}

```
## Notas Adicionales 
## Referencias
