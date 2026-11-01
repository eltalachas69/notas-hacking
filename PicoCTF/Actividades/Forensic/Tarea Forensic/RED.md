## Descripción
RED, RED, RED, RED Download the image: [red.png](https://challenge-files.cylabacademy.net/library/fefcf06050d98347e1585e5cb9f2940967f82e0b89c591966473c752de9f3aba/red.png)
## Solución
Usando zsteg salio un texto en base64 ya de ahi mismo lo decodifique para ver lo que tenia y ahi me dio la bandera que es `academy{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}`
```
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Tarea/RED]
└─$ zsteg red.png  
meta Poem           .. text: "Crimson heart, vibrant and bold,\nHearts flutter at your sight.\nEvenings glow softly red,\nCherries burst with sweet life.\nKisses linger with your warmth.\nLove deep as merlot.\nScarlet leaves falling softly,\nBold in every stroke."
chunk:0:IHDR        .. file: Adobe Photoshop Color swatch, version 0, 128 colors; 1st RGB space (0), w 0x80, x 0x806, y 0, z 0; 2nd HSB space (1), w 0, x 0xff, y 0xff01, z 0x1
b1,rgba,lsb,xy      .. text: "YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="
b1,rgba,msb,xy      .. file: OpenPGP Public Key
b1,abgr,msb,xy      .. file: OpenPGP Secret Key
b2,g,lsb,xy         .. text: "ETEUTTPETUUT@TUUTD@PDUDDDPE"
b2,rgba,msb,xy      .. text: "CIkiiiII"
b2,abgr,lsb,xy      .. file: OpenPGP Public Key
b2,abgr,msb,xy      .. text: "akcikaicc"
b3,a,lsb,xy         .. file: MPEG ADTS, layer II, v1, 224 kbps, 48 kHz, Monaural
b3,bgr,lsb,xy       .. file: PDP-11 executable not stripped - version 56
b3,rgba,msb,xy      .. text: "#vr#w`#~p#6"
b3,abgr,msb,xy      .. text: "7r'7p#wp"
b4,b,lsb,xy         .. file: raw G3 (Group 3) FAX, byte-padded
                                                                                                                   
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Tarea/RED]
└─$ echo "YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==YWNhZGVteXtyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ" | base64 -d
academy{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}academy{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}academy{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}academy{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}                                                                                                                   

```
## Notas Adicionales 
## Referencias
