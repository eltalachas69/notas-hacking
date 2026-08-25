## Descripción
Cryptography can be easy, do you know what ROT13 is?

[values.txt](https://challenge-files.picoctf.net/c_wily_courier/8b42cf1faceb5224789128447ae1c7682ae59c3e9810825a8fcef944e5687fdf/values.txt)
## Solución
En esta practica se uso cyberchef para desencriptar
```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/the-beginner/mod-26]
└─$ cat values.txt  
cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_45559noq}

```
Ahi esta la bandera pero esta encriptada en rot 13, entonces usamos cyberchef para desencriptarlo [bandera](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=Y3ZwYlBHU3thcmtnX2d2enJfVid5eV9nZWxfMl9lYmhhcWZfYnNfZWJnMTNfNDU1NTlub3F9Cg) 
## Notas Adicionales 
## Referencias
[Cyberchef](https://gchq.github.io/CyberChef/)

