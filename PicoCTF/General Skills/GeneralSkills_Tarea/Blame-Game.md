## Descripción
Someone's commits seems to be preventing the program from working. Who is it?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/159/challenge.zip)
## Solución
Use un `grep -r "pico"` al principio pero luego me salieron muchos archivos, entonces solo use `grep -r "picoCTF{"` y me salio la bandera
```
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Blame_Game/drop-in]
└─$ grep -r "picoCTF{" 
.git/logs/HEAD:3ce5c692e2f9682a866c59ac1aeae38d35d19771 23e9d4ce78b3cea725992a0ce6f5eea0bf0bcdd4 picoCTF{@sk_th3_1nt3rn_81e716ff} <ops@picoctf.com> 1710202035 +0000        commit: optimize file size of prod code
.git/logs/refs/heads/master:3ce5c692e2f9682a866c59ac1aeae38d35d19771 23e9d4ce78b3cea725992a0ce6f5eea0bf0bcdd4 picoCTF{@sk_th3_1nt3rn_81e716ff} <ops@picoctf.com> 1710202035 +0000   commit: optimize file size of prod code

```
## Notas Adicionales 
## Referencias