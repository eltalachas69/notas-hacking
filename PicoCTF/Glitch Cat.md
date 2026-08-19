## Descripción
`nc saturn.picoctf.net 49568`
## Solución
```
┌──(kali㉿kali)-[~/Projects/picoCTF/GlitchCat]
└─$ nc saturn.picoctf.net 49568                                                                                       
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/GlitchCat]
└─$ python3           
Python 3.13.14 (main, Jun 10 2026, 18:10:12) [GCC 15.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> >'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
  File "<python-input-0>", line 1
    >'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
    ^
SyntaxError: invalid syntax
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
'picoCTF{gl17ch_m3_n07_9c42a45d}'
>>> 

```
## Notas Adicionales 
## Referencias