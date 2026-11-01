## Descripción
Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://challenge-files.cylabacademy.net/library/764d21f0248d7c1df55583eb1ad863dad241f86f90dd2717e8aa5b9fc3a7e26e/anthem.flag.txt).
## Solución
Para resolverlo primero use el comando strings junto al grep porque vi que era mucho texto y me salio la bandera que es `academy{gr3p_15_@w3s0m3_c16b6693}`
```
┌──(kali㉿kali)-[~/…/Examenes/SegundoExamen/Forensic/LookeyHere]
└─$ strings anthem.flag.txt | grep "academy{"
      we think that the men of academy{gr3p_15_@w3s0m3_c16b6693}

```
## Notas Adicionales 
## Referencias
