## Descripción
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.

There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
En este caso al mero final nos dice en una lista que en uno de esos textos esta la contraseña correcta, tomamos de esa lista uno por uno y la transformamos a hash, esto lo comparamos con el hash que tenemos y si es correcta tenemos la contraseña
```
def level_3_pw_check():
    pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]
    for i in range(0, len(pos_pw_list)):
        user_pw = pos_pw_list[i]
        user_pw_hash = hash_pw(user_pw)
        if user_pw_hash != correct_pw_hash:
            i++


```
```
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3/PW-Crack-3]
└─$ python3 level3.py
87ab
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}

```
## Notas Adicionales 
## Referencias