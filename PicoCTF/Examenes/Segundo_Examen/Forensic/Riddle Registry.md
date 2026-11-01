## Descripción
Hi, intrepid investigator! 📄🔍 You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense. But beware! Not everything is as it appears. Amidst the chaos lies a hidden treasure—an elusive flag waiting to be uncovered. Find the PDF file here [Hidden Confidential Document](https://challenge-files.cylabacademy.net/library/b32f1f1945481591df61d328d02995fe3521d16b70928fbe44e3bd90c4ccb113/confidential.pdf) and uncover the flag within the metadata.
## Solución
La bandera estaba codificada en base64, usando strings se vio que en donde decia author estaba el texto de base64 `YWNhZGVteXtwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV85ZDNjYzY2OX0` usando base64 -d lo pude decodificar y la bandera que me dio es `academy{puzzl3d_m3tadata_f0und!_9d3cc669}`
```
┌──(kali㉿kali)-[~/…/Examenes/SegundoExamen/Forensic/RiddleRegistry]
└─$ echo "YWNhZGVteXtwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV85ZDNjYzY2OX0" | base64 -d
academy{puzzl3d_m3tadata_f0und!_9d3cc669}                                  
```
## Notas Adicionales 
## Referencias
