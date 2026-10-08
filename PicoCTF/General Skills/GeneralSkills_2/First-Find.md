## Descripción
Unzip this archive and find the file named 'uber-secret.txt'
[Download zip file](https://artifacts.picoctf.net/c/502/files.zip)
## Solución
Lo que hacemos usar find para buscar el archivo en las carpetas
```
┌──(kali㉿kali)-[~/Projects/picoCTF/First-Find]
└─$ find . -name "uber-secret.txt"
./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/First-Find]
└─$ cat ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt

picoCTF{f1nd_15_f457_ab443fd1}

```
Copiamos la direccion que nos da y lo ejecutamos con cat, ahi nos da la bandera
## Notas Adicionales 
## Referencias