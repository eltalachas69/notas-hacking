## Descripción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)
## Solución
Esta imagen esta comprimida entonces la tenemos que descomprimir para poder usar mmls

```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/sleuthkit-Series/sleuthkit-intro]
└─$ file disk.img.gz              
disk.img.gz: gzip compressed data, was "disk.img", last modified: Tue Sep 21 19:34:53 2021, from Unix, original size modulo 2^32 104857600
                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/Personal/sleuthkit-Series/sleuthkit-intro]
└─$ mmls disk.img.gz   
                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/Personal/sleuthkit-Series/sleuthkit-intro]
└─$ gunzip disk.img.gz 

```
Tambien nos pide conectarnos en `nc saturn.picoctf.net 52598` y nos pide lo siguiente
```
┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 52598        
What is the size of the Linux partition in the given disk image?
Length in sectors:
```
Quiere saber el tamaño de la particion de linux que nos dio, para eso ahora usamos ya mmls a nuestra imagen descomprimida e insertamos el valor para que nos den la bandera
```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/sleuthkit-Series/sleuthkit-intro]
└─$ mmls disk.img   
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)

┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 52598        
What is the size of the Linux partition in the given disk image?
Length in sectors: 0000202752
0000202752
Great work!
picoCTF{mm15_f7w!}

```
## Notas Adicionales 
## Referencias