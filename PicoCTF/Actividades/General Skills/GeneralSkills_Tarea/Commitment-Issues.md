## Descripción
I accidentally wrote the flag down. Good thing I deleted it!

You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/76/challenge.zip)
## Solución
Pues es checar los commits ya que ahi esta la bandera
```
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Commit/drop-in]
└─$ git log             
commit a6dca68e4310585eac3b5c9caf0f75967dfe972c (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:06 2024 +0000

    remove sensitive info

commit e720dc26a1a55405fbdf4d338d465335c439fb3e
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:06 2024 +0000

┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Commit/drop-in]
└─$ git reset --hard e720dc26a1a55405fbdf4d338d465335c439fb3e
HEAD is now at e720dc2 create flag
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Commit/drop-in]
└─$ ls
message.txt
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Commit/drop-in]
└─$ cat message.txt 
picoCTF{s@n1t1z3_7246792d}

```
## Notas Adicionales 
## Referencias