## Descripción
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)
## Solución
Lo que hacemos es descomprimir el archivo, simplemento usamos grep -r , esto lo hacemos para buscar en todas las carpetas donde diga pico el archivo para tener la bandera
```
┌──(kali㉿kali)-[~/Projects/picoCTF/repetitions/Big-zip]
└─$ grep -r "pico"
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/repetitions/Big-zip]
└─$ 

```
## Notas Adicionales 
## Referencias