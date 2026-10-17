## Descripción
How about some hide and seek?

Download this file [here](https://challenge-files.cylabacademy.net/library/11fdb597bbb1d536206281294ff4deaab719218f36d44e69c4eafde5926144a6/unknown.zip).
## Solución
Con hexeditor vi que habia un texto en Base64, entonces lo tome y le hice un base64 -d para que me diera el texto y ya ahi salio la bandera que es `academy{ME74D47A_HIDD3N_b65fe5f7}`
```
┌──(kali㉿kali)-[~/…/picoCTF/forensics/Tarea/CanYouSee]
└─$ echo "YWNhZGVteXtNRTc0RDQ3QV9ISUREM05fYjY1ZmU1Zjd9Cg" | base64 -d
academy{ME74D47A_HIDD3N_b65fe5f7}

```
## Notas Adicionales 
## Referencias
