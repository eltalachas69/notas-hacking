## Descripción
How about some hide and seek heh? Look at this image [here](https://challenge-files.cylabacademy.net/library/4430e164c62a6474394efb666c3b2c24511a0823a3408e5e7a19a37940f0e592/atbash.jpg)
## Solución
Para esto tuve que ver que herramienta podriamos utilizar y buscando vi que teniamos steghide, esto porque binwalk no me servia y me decia que era una imagen cualquiera, entonces habia dentro un archivo oculto, estaba encriptado pero pues en la misma imagen nos da el tipo de cifrado, simplemente fui a cyberchef y ya con eso me dio la bandera que es `academy{atbash_crack_6167bd8e}`

```
┌──(kali㉿kali)-[~/…/picoCTF/cripto/cripto4/HideToSee]
└─$ steghide info atbash.jpg   
"atbash.jpg":
  format: jpeg
  capacity: 2.4 KB
Try to get information about embedded data ? (y/n) y
Enter passphrase: 
  embedded file "encrypted.txt":
    size: 31.0 Byte
    encrypted: rijndael-128, cbc
    compressed: yes
┌──(kali㉿kali)-[~/…/picoCTF/cripto/cripto4/HideToSee]
└─$ steghide extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".
```
## Notas Adicionales 
## Referencias
[CyberChef](https://cyberchef.io/#recipe=Atbash_Cipher()&input=enh6d3ZuYnt6Z3l6aHNfeGl6eHBfNjE2N3l3OHZ9Cg)
