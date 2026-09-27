## Descripción
Find the flag in this [picture](https://challenge-files.cylabacademy.net/library/a3bb49a714b2015cbba62c5a2db7238a40609a2fbbd7fbe21af7a8f5068cc7b8/pico_img.png).
## Solución
Lo que hice fue lo mismo que hice en Glory of the Garden, fue hacer un strings junto con un grep y asi pude encontrar la bandera `academy{s0_m3ta_d5c3711a}`
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Forensics_1/So_Meta]
└─$ strings pico_img.png | grep "academy{"
academy{s0_m3ta_d5c3711a}6J;
```
## Notas Adicionales 
## Referencias