## Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [dolls.jpg](https://challenge-files.cylabacademy.net/library/2eb277d09563812ad880fdd564d0fb59c084a64f514f6e12998534c8f7997405/dolls.jpg)
## Solución
De lo que trata el reto es extraer la imagen, pero para saberlo vi en una pista que decia que puede que el archivo puede ser diferente, osea que si puede haber otro tipo de identificador, buscando si habia un comando kali para que supiera si la imagen podia ser otro tipo de archivo encontre que si, era con el comando binwalk, de lo que me salio es que era un archivo .zip
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Forensics3/matryoshka]
└─$ binwalk dolls.jpg  

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378929, uncompressed size: 383919, name: base_images/2_c.jpg
651587        0x9F143         End of Zip archive, footer length: 22

```
Entonces en binwalk hay un comando para extraerlo y me salio esto
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Forensics3/matryoshka]
└─$ binwalk -e dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378929, uncompressed size: 383919, name: base_images/2_c.jpg

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

```
Una vez entrando habia otra imagen que basicamente era lo mismo con el comando anterior, esto es como las muñecas rusas hasta llegar a la ultima que es la cuarta, una vez que llegamos a la cuarta usando `strings` no sale la bandera que es `academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}`
```
──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ strings 4_c.jpg | grep "academy{" 
academy{ZNTyvSDXRNO1d0xCkBRMhAoiafpCTvgW}

```
## Notas Adicionales 
## Referencias
