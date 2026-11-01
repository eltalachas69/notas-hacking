## Descripción
Download this disk image, find the key and log into the remote machine.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://challenge-files.cylabacademy.net/library/8af34b0fa863a6efa03d28278ca270b335291ad998f21c3696889bdc9c77ab72/disk.img.gz)
- Remote machine: `ssh -i key_file -p 13567 ctf-player@xebec.cylabacademy.net`
## Solución
De lo que trata es conectarnos a un puerto pero ahi nos dice que ocupamos un archivo key, pero para eso tenemos que checar un img y ya de ahi sacarlo,para este caso teniamos que checar una imagen con fls, a mi el que me interesaba era el root, entonces ahi salia un .ssh, entonces lo extraemos el privado para poder ingresarlo, pero antes que nada tenemos que cambiarle los permisos con el chmod porque no nos va a funcionar `academy{k3y_5l3u7h_0e000cd7}`
```
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ fls -o 206848  disk.img
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ fls -o 206848  disk.img 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ fls -o 2048 disk.img 25585 
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ fls -o 206848  disk.img    
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ fls -o 206848  disk.img 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ fls -o 206848  disk.img 3916
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ icat -o 206848 disk.img 2345 > unamamada
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ chmod +x unamamada 
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ ls -l
total 235524
-rw-r--r-- 1 kali ElCuilango 241172480 Sep 22 22:58 disk.img
-rwxr-xr-x 1 kali ElCuilango       411 Oct  7 23:26 unamamada
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ ssh -i unamamada  -p 13567 ctf-player@xebec.cylabacademy.net   
The authenticity of host '[xebec.cylabacademy.net]:13567 ([3.14.181.178]:13567)' can't be established.
ED25519 key fingerprint is: SHA256:ZzFWPkrkkhq4v3aMejPdeBM6CxOJEdDfCOqwc0eXgfY
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[xebec.cylabacademy.net]:13567' (ED25519) to the list of known hosts.
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0755 for 'unamamada' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
Load key "unamamada": bad permissions
ctf-player@xebec.cylabacademy.net's password: 

                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ chmod 600 unamamada 
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/OperationOni]
└─$ ssh -i unamamada  -p 13567 ctf-player@xebec.cylabacademy.net
Welcome to Ubuntu 24.04.4 LTS (GNU/Linux 7.0.0-1014-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt 
academy{k3y_5l3u7h_0e000cd7}ctf-player@challenge:~$ 

```
## Notas Adicionales 
## Referencias
