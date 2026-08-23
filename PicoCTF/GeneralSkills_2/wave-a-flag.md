## Descripción
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...

[warm](https://challenge-files.picoctf.net/c_wily_courier/1e14db3a752e16eae2b0e0d73d9779f9c4ddfd8942f60f3285a2986068480316/warm)
## Solución
Es cambiarle los permisos del archivo y ejecutarlo 
```
──(kali㉿kali)-[~/Projects/picoCTF/wave-a-flag]
└─$ ls -l       
total 20
-rw-r--r-- 1 kali ElCuilango 19312 Dec 12  2025 warm

```
En ese caso usamos chmod +x para que podamos ejecutar
```
┌──(kali㉿kali)-[~/Projects/picoCTF/wave-a-flag]
└─$ chmod +x warm          
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/wave-a-flag]
└─$ ls -l
total 20
-rwxr-xr-x 1 kali ElCuilango 19312 Dec 12  2025 warm

```
Cuando lo ejecutamos nos va a pedir que le mandemos una -h y ahi esta la bandera
```
┌──(kali㉿kali)-[~/Projects/picoCTF/wave-a-flag]
└─$ ./warm 
Hello user! Pass me a -h to learn what I can do!
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/wave-a-flag]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}

```
## Notas Adicionales 
## Referencias