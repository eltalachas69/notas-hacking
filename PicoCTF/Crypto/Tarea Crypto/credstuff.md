## Descripción
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://challenge-files.cylabacademy.net/library/7f760cee144ac7237469fd6bfab7c748d6f1d101ca47c101187ca7d8f5c721f0/leak.tar).

The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.
## Solución
No use comandos de linux esta vez, lo unico que hice fue checarlo en el bloc de notas y pues ya ahi me salia a la izquierda los numeros de su posicion de linea, entonces lo primero que hice fue buscar al usuario y ya con ese numero de la posicion lo busque en el de passwords y con eso me salio la bandera pero esta en rot13, pues ya fui con el cyberchef y pues ya le mande eso de rot13   `npnqrzl{P7e1S_54I35_71Z3}` y ya me salio, la bandera que es `academy{C7r1F_54V35_71M3}`

## Notas Adicionales 
## Referencias
[CyberChef](https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=bnBucXJ6bHtQN2UxU181NEkzNV83MVozfQ)
