## Descripción
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.

The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden. The website is running [picoCTF News](http://chatelaine.cylabacademy.net:20839/).
## Solución
Descargando la diagnosis y haciendo un grep del heapdump nos da la bandera que es `academy{Pat!3nt_15_Th3_K3y_b3a35ec3}` 
```
┌──(kali㉿kali)-[~/Downloads]
└─$ cat  heapdump-1790556818321.heapsnapshot | grep "academy"
academy{Pat!3nt_15_Th3_K3y_b3a35ec3}
"strings":["<dummy>","","(GC roots)","(Bootstrapper)","(Builtins)","(Client heap)","(Code flusher)","(Compilation cache)","(Debugger)","(Extensions)","(Eternal handles)","(External strings)","(Global handles)","(Handle scope)","(Micro tasks)","(Read-only roots)","(Relocatable)","(Retain maps)","(Shareable object cache)","(SharedStruct type registry)","(Smi roots)","(Stack roots)","(Startup object cache)","(Internalized strings)","(Strong root list)","(Strong roots)","(Thread manager)","(Traced handles)","...
```
## Notas Adicionales 
## Referencias
