## Descripción
Decode this [message](https://challenge-files.cylabacademy.net/library/d825fde6581b1311eafdd403da1cc96f1f98fe3fe84cd71d850310ebb3908088/message.wav) from the moon.
## Solución
Para esto debemos de transformar el audio en una imagen y para transformalo tenemos que hacerlo con un programa, esto lo encontramos en github una vez hecho esto nos va a dar la bandera la cual es `picoCTF{beep_boop_im_in_space}`
El comando para transformar el audio en imagen es el siguiente
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Forensics_2]
└─$ sstv -d message.wav -o hola.png               
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [#################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!

``` 
## Notas Adicionales 
## Referencias
[sstv](https://github.com/colaclanth/sstv)
