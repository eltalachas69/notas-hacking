## Descripción
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?
Connect to fickle-tempest.picoctf.net 51486.
## Solución
```
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net 51486 
This is defintely not a flag
I don't think this is a flag either
This is defintely not a flag
Not a flag either
Not a flag either
This is defintely not a flag
Not a flag either
Again, I really don't think this is a flag
This is defintely not a flag
Again, I really don't think this is a flag
Not a flag either
Again, I really don't think this is a flag
This is defintely not a flag
I don't think this is a flag either
Not a flag either
Not a flag either
I don't think this is a flag either
Again, I really don't think this is a flag
Again, I really don't think this is a flag
I don't think this is a flag either
...
┌──(kali㉿kali)-[~]
└─$ nc fickle-tempest.picoctf.net 51486 | grep pico
picoCTF{digital_plumb3r_00da27CC}

```
## Notas Adicionales 
Lo que se hizo fue usar un pipe para encontrar la bandera
## Referencias