## Descripción
Fix the syntax error in the Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)
## Solución
El unico error era en la parte es en la de comparar si esta vacia, hasta en la terminal nos dice que puede que sea `==`
```
File "/home/kali/Projects/picoCTF/General_Skills3/fixme2/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?

```
Entonces hay varias maneras para corregir esa parte como de cambiar `=` a `==`, tambien esta ponerlo asi `if not flag:`, pero cualquiera es valida
```
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3/fixme2]
└─$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}

```
## Notas Adicionales 
## Referencias
