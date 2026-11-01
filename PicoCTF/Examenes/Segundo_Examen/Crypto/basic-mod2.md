## Descripción
A new modular challenge! Download the message [here](https://challenge-files.cylabacademy.net/library/79ab2df83c3efdaa68f8d1d7b4ce3e478bd49e8193ca7002a30ea460743c412c/message.txt).

Take each number mod 41 and find the modular inverse for the result. Then map to the following character set: 1-26 are the alphabet, 27-36 are the decimal digits, and 37 is an underscore.

Wrap your decrypted message in the academy flag format (i.e. `academy{decrypted_message}`)
## Solución
Para resolverlo simplemente nos pidieron aplicar la formula, osea encontrar el residuo y en base de eso sacarle la inversa, mas facil era en python hacer la formula para cada numero y pues si ya uno queria podia convertir las letras uno por uno o hacer un script, pero como me la quiero complicar preferi hacer lo primero y me dio el contenido de la bandera la cual es `academy{1NV3R53LY_H4RD_FED0A735}`

```
>>> lista = [309, 44, 274, 149, 57, 378, 313, 311, 64, 420, 405, 86, 98, 195, 256, 48, 238, 277, 448, 411, 240, 436, 214]
>>> import math
>>> for numero in lista:
...     numeromod = numero%41
...     inverso = pow(numeromod,-1,41)
...     print(inverso)
...     
28
14
22
30
18
32
30
12
25
37
8
31
18
4
37
6
5
4
27
1
34
30
32

```
## Notas Adicionales 
## Referencias
