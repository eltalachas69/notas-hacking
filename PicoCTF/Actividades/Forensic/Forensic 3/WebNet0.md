## Descripción
We found this [packet capture](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key). Recover the flag.
## Solución
Para saber donde estaba la bandera analice el pcap y habia una parte que decia encriptado, tambien buscando en base al protocolo tls, ahi estaba la bandera pero no sabia cual era. Lo que hice fue usar wireshark y meterme en Edit e irme a los protocolos para buscar el TLS, meti una nueva RSA key que me dio el reto, de la configuracion puse la IP `any`, el puerto `443`, con el protocolo `http` y ya de ahi en key file puse el `.key` del reto, entonces ya use el tls stream y buscando encontre la bandera que es  `academy{nongshim.shrimp.crackers}`

## Notas Adicionales 
## Referencias
