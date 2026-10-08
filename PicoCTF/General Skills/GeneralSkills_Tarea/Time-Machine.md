## Descripción
What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/160/challenge.zip)
## Solución
Aqui es muy facil, es solo ver el historial de los commits para encontrar la bandera
```
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/Time-Machine]
└─$ cd drop-in 
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Time-Machine/drop-in]
└─$ ls
message.txt
                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Time-Machine/drop-in]
└─$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...                                                                                                                                                            
┌──(kali㉿kali)-[~/…/picoCTF/General_Skills_Tarea/Time-Machine/drop-in]
└─$ git log --oneline                                        
89d296e (HEAD -> master) picoCTF{t1m3m@ch1n3_186cd7d7}
                                                                          
```
## Notas Adicionales 
## Referencias
