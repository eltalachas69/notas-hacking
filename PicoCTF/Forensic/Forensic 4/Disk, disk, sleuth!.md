## Descripción
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.cylabacademy.net/library/cb4d1ac86836c86e1ea16a4be1d8cf72c0465c6edcc0ab886728040a28dd7966/dds1-alpine.flag.img.gz)
## Solución
Nada dificil, solo use el comando que me dijeron y le puse un grep, ahi me salio la bandera `academy{f0r3ns1c4t0r_n30phyt3_6502313d}`
```
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Forensics4/diskdisk]
└─$ srch_strings dds1-alpine.flag.img | grep "academy{"
  SAY academy{f0r3ns1c4t0r_n30phyt3_6502313d}
                                                           
```
## Notas Adicionales 
## Referencias
