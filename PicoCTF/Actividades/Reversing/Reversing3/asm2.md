## Descripción
What does asm2(0x8,0x18) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.cylabacademy.net/library/1024eb8bc7b4a17cb4796a34bd749e374a626680a3b3f66c8179ee2ccfcfeb77/test.S)
## Solución
En este caso se resuelve igual que la anterior solo que en este caso es algo corto pero nos esta dando dos valores, lo que trata es un ciclo, basicamente es una suma de uno en uno, para no complicarnos con la explicacion del profe nos dijo que dividieramos el numero hexadecimal del `cmp` con el del `add`, entonces en mi caso hace un ciclo de 175 vueltas, entonces sumamos ese 175 + 1 ya que en la comparacion nos esta pidiendo que si el segundo numero de entrada es menor o igual, entonces el resultado fue 200, convertido en hexadecimal fue `0xc8` y esa es nuestra bandera
## Notas Adicionales 
## Referencias
