## Descripción
Can you look at the data in this binary? The bash script might help!

[static](https://challenge-files.picoctf.net/c_wily_courier/b06384f5fdb3a6e3f0f254d1064d203e7df4bf7e9a5780a95622523367d82bc0/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/b06384f5fdb3a6e3f0f254d1064d203e7df4bf7e9a5780a95622523367d82bc0/ltdis.sh)
## Solución
Esto es lo mismo que con el chmod +x nomas que ahora son dos archivos, cuando ejecutamos los dos nos sale esto

```
┌──(kali㉿kali)-[~/Projects/picoCTF/Static-aint-always-noise]
└─$ ./static         
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
┌──(kali㉿kali)-[~/Projects/picoCTF/Static-aint-always-noise]
└─$ ./ltdis.sh       
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!

```
Lo que tenemos que hacer es juntar el ltdis.sh junto con el static
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Static-aint-always-noise]
└─$ ./ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset

┌──(kali㉿kali)-[~/Projects/picoCTF/Static-aint-always-noise]
└─$ ls             
ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt

```
Abrimos el .strings.txt con un grep porque nos va a salir mucho texto
```
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/Static-aint-always-noise]
└─$ cat static.ltdis.strings.txt | grep pico
   3020 picoCTF{d15a5m_t34s3r_20335e41}
```

## Notas Adicionales 
## Referencias