## Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure!
## Solución
Para este reto debemos de usar varias herramientas, esto para hacer un ataque de fuerza bruta, para eso usamos flask--unsign con las palabras de cookies que tenemos, en mi caso me salio 'snowball'. Esto ya le hacemos sign con el secret ya sabido que es 'snowball' entonces solo pegamos la cookie que hicimos en el navegador y obtenemos la bandera que es `picoCTF{cO0ki3s_yum_b8a89e75}`
## Notas Adicionales 
## Referencias