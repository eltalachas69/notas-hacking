## Descripción
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg)
## Solución
Para resolverlo tuve que usar exiftool y en licencia ahi estaba la bandera solo que estaba en base64, entonces use base64 y ya con eso me dio la bandera que es `academy{the_m3tadata_1s_modified}`
```
                                                                                                                
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Tarea/information]
└─$ exiftool cat.jpg
ExifTool Version Number         : 13.55
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2026:09:22 22:44:41-04:00
File Access Date/Time           : 2026:10:17 13:56:03-04:00
File Inode Change Date/Time     : 2026:10:17 13:56:03-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 13.25
License                         : YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
                                                                                                                
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Tarea/information]
└─$ echo "YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d
academy{the_m3tadata_1s_modified}  
```
## Notas Adicionales 
## Referencias
