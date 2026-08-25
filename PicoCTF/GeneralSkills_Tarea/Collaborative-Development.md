## Descripción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/70/challenge.zip)

## Solución
Consiste en moverse con los comandos de git para ver el repositorio, nos dieron 3 ramas para checar, la primera rama fue esta y hay un archivo `.py`
```
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ git checkout feature/part-1
Switched to branch 'feature/part-1'
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ la -la
total 16
drwxr-xr-x 3 kali ElCuilango 4096 Aug 25 00:23 .
drwxr-xr-x 3 kali ElCuilango 4096 Aug 25 00:19 ..
-rw-r--r-- 1 kali ElCuilango   64 Aug 25 00:23 flag.py
drwxr-xr-x 8 kali ElCuilango 4096 Aug 25 00:23 .git
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ cat flag.py     
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')    
```
En la segunda rama fue esto
```
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ git checkout feature/part-2
Switched to branch 'feature/part-2'
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ ls -la
total 16
drwxr-xr-x 3 kali ElCuilango 4096 Aug 25 00:25 .
drwxr-xr-x 3 kali ElCuilango 4096 Aug 25 00:19 ..
-rw-r--r-- 1 kali ElCuilango   64 Aug 25 00:25 flag.py
drwxr-xr-x 8 kali ElCuilango 4096 Aug 25 00:25 .git
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')            
```
La tercera rama fue esto
```
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ git checkout feature/part-3
Switched to branch 'feature/part-3'
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ ls    
flag.py
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Collaborative-Development/drop-in]
└─$ cat flag.py 
print("Printing the flag...")

print("w0rk_7ffa0077}")

```
La bandera es esta `picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ffa0077}`


## Notas Adicionales 
## Referencias