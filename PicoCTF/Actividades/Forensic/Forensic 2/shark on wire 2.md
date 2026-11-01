## Descripción
We found this [packet capture](https://challenge-files.cylabacademy.net/library/f76620763560ca0683be36e0ed4648743f969ab4d852fda0d8fb4d3ae21a173d/shark-on-wire-2-capture.pcap). Recover the flag that was pilfered from the network.
## Solución
Para obtener la bandera estaba buscando en wireshark y en un udp hay un puerto especial, bueno la informacion que tiene, mas que nada por el puerto 22 ahi marca 'start' y habia un '{end' algo diferente a los demas que son letras con numeros, entonces buscando en el puerto 22 y ordenandolo, lo curioso es que en todos empezaban en 5 y 3 digitos, y se ve que hace una "ace" en los siguientes digitos, entonces tome esos 3 digitos y los puse en cyberchef y ahi me salio la bandera que es `academy{p1LLf3r3d_data_v1a_st3g0}`
## Notas Adicionales 
## Referencias
[cyberchef](https://cyberchef.io/#recipe=From_Decimal('Space',false)&input=MDk3IDA5OSAwOTcgMTAwIDEwMSAxMDkgMTIxIDEyMyAxMTIgNDkgNzYgNzYgMTAyIDUxIDExNCA1MSAxMDAgOTUgMTAwIDk3IDExNiA5NyA5NSAxMTggNDkgOTcgOTUgMTE1IDExNiA1MSAxMDMgNDggMTI1Cg)
