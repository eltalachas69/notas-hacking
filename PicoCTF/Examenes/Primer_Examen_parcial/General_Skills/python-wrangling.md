## Descripción
Python scripts are invoked kind of like programs in the Terminal...

Can you run [ende.py](https://challenge-files.picoctf.net/c_wily_courier/0d4c2d3266a170a6b1cc9150c9a1cf489cd39be1968f82164aea44fb88e810b7/ende.py) using [password.txt](https://challenge-files.picoctf.net/c_wily_courier/0d4c2d3266a170a6b1cc9150c9a1cf489cd39be1968f82164aea44fb88e810b7/password.txt) to get [flag.txt.en](https://challenge-files.picoctf.net/c_wily_courier/0d4c2d3266a170a6b1cc9150c9a1cf489cd39be1968f82164aea44fb88e810b7/flag.txt.en)?
## Solución
Para esto corremos un programa de python y descarguemos 2 archivos, cuando ejecutamos el archivo py nos dice lo siguiente
```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/general-skills/convertme]
└─$ python3 ende.py     
Usage: ende.py (-e/-d) [file]

```
Lo que hace este programa es encriptar o desencriptar un archivo, usamos -d para desencriptar el la bandera
```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/general-skills/convertme]
└─$ python3 ende.py -d flag.txt.en      
Please enter the password:
```
Nos pide la contraseña, pero como descargamos el archivo password y ahi esta y se la pegamos y nos da la bandera
```
┌──(kali㉿kali)-[~/…/picoCTF/Personal/general-skills/convertme]
└─$ python3 ende.py -d flag.txt.en      
Please enter the password:720b6ad346f84cd483c60c7464dd95d4
picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}

```
## Notas Adicionales 
## Referencias