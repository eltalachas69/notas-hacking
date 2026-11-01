
## Descripcion
There is a nice program that you can talk to by using this command in a shell:
$ nc wily-courier.picoctf.net 65262, but it doesn't speak English...
## Solución
```
┌──(kali㉿kali)-[~/Projects/picoCTF/GlitchCat]
└─$  nc wily-courier.picoctf.net 65262 | xargs 
112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 97 57 52 101 55 125 10
┌──(kali㉿kali)-[~/Projects/picoCTF/GlitchCat]
└─$ python3
Python 3.13.14 (main, Jun 10 2026, 18:10:12) [GCC 15.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> datos = """112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 97 57 52 101 55 125 10
... """
>>> ''.join(chr(int(n))for n in datos.split())
'picoCTF{g00d_k1tty!_n1c3_k1tty!_a94e7}\n'
>>> 

```
## Notas Adicionales 
## Referencias
