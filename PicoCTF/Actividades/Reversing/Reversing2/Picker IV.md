## Descripción
Can you figure out how this program works to get the flag? Connect to the program with netcat:

`$ nc chatelaine.cylabacademy.net 25877`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/29304f03408a71abe2959b78d93cf0ad4b599550b0dfc4ee3211c8376731d344/picker-IV.c). The binary can be downloaded [here](https://challenge-files.cylabacademy.net/library/29304f03408a71abe2959b78d93cf0ad4b599550b0dfc4ee3211c8376731d344/picker-IV).
## Solución
Para resolverlo tuve que descargar un depurador para ver como funcionaba un programa, entonces solo queria ver las funciones y me las dio y ahi estaba el win, el programa solo consistia escribir un hex despues del `0x` y pues puse el de win y me dio la bandera que es `academy{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_cccc13c1}`
## Notas Adicionales 
## Referencias
