## Descripción
 This file contains more than it seems. Get the flag from [garden.jpg](https://challenge-files.cylabacademy.net/library/0b84012e7d505751ee79c0407057962df7324463d7f8495cb79f5fb2dd998d7d/garden.jpg).
## Solución
En este caso use primero el comando `xxd` pero cuando lo use se tardo un poco, si me dio la bandera pero me acorde que podiamos usar strings entonces lo use junto con un grep para buscar la bandera la cual es `academy{more_than_m33ts_the_3y36c4fc727}`
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Forensics_1/Glory_of_the_Garden]
└─$ xxd garden.jpg                   
00000000: ffd8 ffe0 0010 4a46 4946 0001 0101 0048  ......JFIF.....H
00000010: 0048 0000 ffe2 0c58 4943 435f 5052 4f46  .H.....XICC_PROF
00000020: 494c 4500 0101 0000 0c48 4c69 6e6f 0210  ILE......HLino..
00000030: 0000 6d6e 7472 5247 4220 5859 5a20 07ce  ..mntrRGB XYZ ..
00000040: 0002 0009 0006 0031 0000 6163 7370 4d53  .......1..acspMS
00000050: 4654 0000 0000 4945 4320 7352 4742 0000  FT....IEC sRGB..
00000060: 0000 0000 0000 0000 0000 0000 f6d6 0001  ................
00000070: 0000 0000 d32d 4850 2020 0000 0000 0000  .....-HP  ......
00000080: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00000090: 0000 0000 0000 0000 0000 0000 0000 0000  ................
...
┌──(kali㉿kali)-[~/Projects/picoCTF/Forensics_1/Glory_of_the_Garden]
└─$ strings garden.jpg | grep "academy"       
Here is a flag: academy{more_than_m33ts_the_3y36c4fc727}

```
## Notas Adicionales 
## Referencias