## Descripción
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.

The flag is in this [file](https://challenge-files.picoctf.net/c_fickle_tempest/92807684f3e52665caaf90d69e1e661f990b8731b2f8005e18631be23ff991bb/file).
## Solución

```
┌──(kali㉿kali)-[~/Downloads/picoCTF]
└─$ cat file | grep picoCTF
picoCTF{grep_is_good_to_find_things_eb80073D}
```
## Notas Adicionales 
De lo que se hizo fue ejecutar ese comando para buscar en la terminal 'picoCTF' y encontrar el contenido de las llaves.
## Referencias