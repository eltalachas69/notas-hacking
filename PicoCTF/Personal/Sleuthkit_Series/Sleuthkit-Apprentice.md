## Descripción
Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)
## Solución
Para encontrar la bandera tenemos que descargar el archivo que nos dan, igual es una imagen de un disco y tenemos que buscarlo, nos da 3 posibles particiones en donde esta, pero para adelantarnos es la ultima
```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/sleuthkit-Series/Sleuthkit-Apprentice]
└─$ mmls disk.flag.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)

```
usamos el comando fls para explorar la particion con un pipe grep para buscar la bandera
```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/sleuthkit-Series/Sleuthkit-Apprentice]
└─$ fls -r -o 360448 disk.flag.img| grep flag
++ r/r * 2082(realloc): flag.txt
++ r/r 2371:    flag.uni.txt

```
esos numeros a la izquierda son los nodos, con eso podemos saber cual es su contenido mediante a ese nodo, para ver el contenido de un archivo en una particion usamos icat
```
                                                                                                                                                          
┌──(kali㉿kali)-[~/…/picoCTF/Personal/sleuthkit-Series/Sleuthkit-Apprentice]
└─$ icat -o 360448 disk.flag.img 2371       
picoCTF{by73_5urf3r_2f22df38}

```
## Notas Adicionales 
## Referencias