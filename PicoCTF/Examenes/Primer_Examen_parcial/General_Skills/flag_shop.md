## Descripción
There's a flag shop selling stuff, can you buy a flag? [Source](https://challenge-files.cylabacademy.net/library/19e144508c6c4343acec333beb6bb22f4acb8a70c0b7143e7e3e64f1138de32a/store.c). Connect with `nc xebec.cylabacademy.net 34367`.
## Solución
Para este caso se tuvo que modificar nuestro dinero y para eso teniamos que comprar una bandera, como el total de costo es de 32 bits y este tienen un limite mayor, ponemos un numero mayor a de 2 mil millones obtendremos mucho dinero que podremos comprar la otra bandera y ahi mismo nos dice que la bandera es `academy{m0n3y_bag5_CAec77CC}`
```
Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1      
These knockoff Flags cost 900 each, enter desired quantity
2400000

The final cost is: -2134967296

Your current balance after transaction: 2134968396

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: academy{m0n3y_bag5_CAec77CC}

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
                                                                                                                    
┌──(kali㉿kali)-[~/…/picoCTF/Primer_Examen_parcial/General_Skills/flag_shop]
└─$ 

```
## Notas Adicionales 
## Referencias