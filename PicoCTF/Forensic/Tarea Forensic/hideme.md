## Descripción
Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://challenge-files.cylabacademy.net/library/072ab2768814bc12f4cc180b5e7bf48e8501774bfb741ff9263792824887fd04/flag.png).
## Solución
Para esto lo primero que hice fue usar binwalk y que me extrayera la bandera, dentro de ella habia una carpeta secret ahi mismo habia otra imagen y cuando la abri ahi estaba la bandera que es `academy{Hiddinng_An_imag3_within_@n_ima9e_ba7f84d1}`
```
──(kali㉿kali)-[~/…/picoCTF/forensics/Tarea/hideme]
└─$ binwalk flag.png -e

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
75            0x4B            Zlib compressed data, default compression
15929         0x3E39          Zip archive data, at least v1.0 to extract, name: secret/
15994         0x3E7A          Zip archive data, at least v1.0 to extract, compressed size: 5805, uncompressed size: 5805, name: secret/flag.png

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

```
## Notas Adicionales 
## Referencias
