## Descripción
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.

Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `56092`.

## Solución
Vi que hay dos soluciones pero con la que nos da es explorar y movernos con cd y ver que hay en ls
```
ctf-player@pico-chall$ ls 
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1
cat: 1: No such file or directory
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ 

```
En instructions nos da lo siguiente y nos dice que nos movamos en "/"
```
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  challenge  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_//4t3r_

```
Ahi mismo esta las otras instrucciones y esta la ultima bandera
```
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
0b24fc4f}ctf-player@pico-chall$ 

```
Aunque otra forma es que ahi hay una carpeta que dice challenge, dentro de ella hay un archivo json con los datos de la bandera
```
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  challenge  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cd challenge/
ctf-player@pico-chall$ ls
metadata.json
ctf-player@pico-chall$ cat metadata.json 
{"flag": "picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}", "password": "8c606eb1"}ctf-player@pico-chall$ 

```
## Notas Adicionales 
## Referencias