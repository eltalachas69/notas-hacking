## Descripción
Download this image and find the flag.

- [Download image](https://challenge-files.cylabacademy.net/library/01f9976b25d3f083166b941c63be9d195b9a4289a2351dcceb0ea944a30bcf83/academy.flag.png)
## Solución
Para solucionarlo se tenia que hacer una esteganografía esto para encontrar la bandera la cual es `academy{7h3r3_15_n0_5p00n_6c8e74e0}`  esto usando zsteg para sacar la bandera
```
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Tarea/st3o]
└─$ zsteg academy.flag.png          
b1,r,lsb,xy         .. text: "~__B?+c_G@"
b1,rgb,lsb,xy       .. text: "academy{7h3r3_15_n0_5p00n_6c8e74e0}$t3g0"
b1,rgba,msb,xy      .. text: "2TAF0RU6r"
b1,abgr,lsb,xy      .. text: "E2A5q4E%uSA"
b2,b,lsb,xy         .. text: "AAAPAAQTAAA"
b3,r,msb,xy         .. file: Applesoft BASIC program data, first line number 18
b4,r,lsb,xy         .. file: Targa image data - Map (16-257) 65536 x 4097 x 1 +257 +4369 - 1-bit alpha - right
b4,b,lsb,xy         .. file: Targa image data 272 x 17 x 16 +272 +272 - 1-bit alpha "\020\001\021\001\021\020\020\001\020\001\020\001"       
```
## Notas Adicionales 
## Referencias
