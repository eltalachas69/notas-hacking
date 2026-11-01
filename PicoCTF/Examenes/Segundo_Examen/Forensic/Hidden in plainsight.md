## Descripción
You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. Your task is to discover the hidden payload and extract the flag. Download the jpg image [here](https://challenge-files.cylabacademy.net/library/9ec77a1b83f3b582954d97ec39f7926d4dc45f98cd1ef7a24b3172ca385e02b2/img.jpg).
## Solución
Para resolver esto en use exiftool para ver lo que habia y dentro de ahi habia un texto en base64, uno decia steghide y otro pAzzword, luego de eso no sabia que hacer o que debia de continuar despues, entonces vi que steghide era un comando en linux, no me habia cordado y entonces lo use para extraer lo que tenia la imagen que tenia un archivo de texto que era flag.txt, despues de extraerlo me dio la bandera que es `academy{h1dd3n_1n_1m4g3_71ae1957}`
```
┌──(kali㉿kali)-[~/…/Examenes/SegundoExamen/Forensic/HiddenInPlainsish]
└─$ exiftool img.jpg                                                          
ExifTool Version Number         : 13.55
File Name                       : img.jpg
Directory                       : .
File Size                       : 73 kB
File Modification Date/Time     : 2026:09:23 01:38:52-04:00
File Access Date/Time           : 2026:10:31 16:27:38-04:00
File Inode Change Date/Time     : 2026:10:31 16:27:24-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Comment                         : c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9
Image Width                     : 640
Image Height                    : 640
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 640x640
Megapixels                      : 0.410
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Examenes/SegundoExamen/Forensic/HiddenInPlainsish]
└─$ steghide --info img.jpg        
"img.jpg":
  format: jpeg
  capacity: 4.0 KB
Try to get information about embedded data ? (y/n) y
Enter passphrase: 
steghide: could not extract any data with that passphrase!
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Examenes/SegundoExamen/Forensic/HiddenInPlainsish]
└─$ steghide --info img.jpg -p pAzzword
"img.jpg":
  format: jpeg
  capacity: 4.0 KB
  embedded file "flag.txt":
    size: 34.0 Byte
    encrypted: rijndael-128, cbc
    compressed: yes
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Examenes/SegundoExamen/Forensic/HiddenInPlainsish]
└─$ steghide extract -sf  img.jpg -p pAzzword
wrote extracted data to "flag.txt".

```
## Notas Adicionales 
## Referencias
[PrimerBase64](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YzNSbFoyaHBaR1U2WTBWR05tVnVaSFpqYlZFOQ)
[SegundoBase64](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0VGNmVuZHZjbVE9)