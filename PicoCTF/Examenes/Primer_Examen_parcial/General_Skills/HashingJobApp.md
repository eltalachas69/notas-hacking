## Descripción
If you want to hash with the best, beat this test! `nc xebec.cylabacademy.net 17508`
## Solución
En esta hay varias maneras de resolverlo, yo use cyberchef y de ahi mismo le hice un hash md5 cada vez que me lo pedia aunque tambien se podia hacer un script de python para poder hacerlo y eso lo hacia mas rapido pero lo hice de esta manera porque el limite de tiempo no era mucho como en otra actividad, la bandera es `academy{4ppl1c4710n_r3c31v3d_467e06bf}`
```
┌──(kali㉿kali)-[~]
└─$ nc xebec.cylabacademy.net 17508
Please md5 hash the text between quotes, excluding the quotes: 'the sunrise'
Answer: 
3652f115c238da1f79187d39b64e3fa2
3652f115c238da1f79187d39b64e3fa2
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Confucius'
Answer: 
286bd9ea520691c9f2018dc96db3ce31
286bd9ea520691c9f2018dc96db3ce31
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'apples'
Answer: 
daeccf0ad3c1fc8c8015205c332f5b42
daeccf0ad3c1fc8c8015205c332f5b42
Correct.
academy{4ppl1c4710n_r3c31v3d_467e06bf}

```
## Notas Adicionales 
## Referencias
[Cyberchef](https://gchq.github.io/CyberChef/#recipe=MD5()&input=YXBwbGVz)
