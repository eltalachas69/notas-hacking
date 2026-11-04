## Descripción
This service can provide you with a random number, but can it do anything else? Connect to the program with netcat:

`$ nc xebec.cylabacademy.net 38990`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/0981ed1dcae182f5d272ebe49164d0dc2c09f043e1843e26dbebaa80317d3245/picker-I.py).
## Solución
Para solucionarlo tuve que checar el codigo que me proporcionaron, intente buscar academy en el programa y no me salio nada, pero cuando busque flag me salio que estaba dentro de una funcion que se llamaba win, entonces puse win y me dio la bandera en hexadecimal, pero ya despues use cyberchef para que me diera la bandera en texto y me la dio la cual la bandera fue `academy{4_d14m0nd_1n_7h3_r0ugh_c55fbef5}`
## Notas Adicionales 
## Referencias
[Hexadecimal](https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHg2MSAweDYzIDB4NjEgMHg2NCAweDY1IDB4NmQgMHg3OSAweDdiIDB4MzQgMHg1ZiAweDY0IDB4MzEgMHgzNCAweDZkIDB4MzAgMHg2ZSAweDY0IDB4NWYgMHgzMSAweDZlIDB4NWYgMHgzNyAweDY4IDB4MzMgMHg1ZiAweDcyIDB4MzAgMHg3NSAweDY3IDB4NjggMHg1ZiAweDYzIDB4MzUgMHgzNSAweDY2IDB4NjIgMHg2NSAweDY2IDB4MzUgMHg3ZA)
