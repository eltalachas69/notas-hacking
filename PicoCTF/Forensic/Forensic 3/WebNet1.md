## Descripción
We found this [packet capture](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/webnet1-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/picopico.key). Recover the flag.
## Solución
Como en [[WebNet0]] lo que yo hice fue modificar el .key y tambien del protocolo le puse tls, entonces hice un follow al numero 91 en http, ahi salio texto cifrado pero en una parte salio la bandera, ahi arriba hay una bandera que no es la bandera, pero usando el find me salio la bandera que es `academy{honey.roasted.peanuts}`
## Notas Adicionales 
## Referencias
