## Descripción
Can you make sense of this file?

Download the file [here](https://artifacts.picoctf.net/c/471/enc_flag).
## Solución
En este caso se uso base64 multiples veces para encontrar la bandera
```
──(kali㉿kali)-[~/Projects/picoCTF/repetitions]
└─$ base64 enc_flag 
Vm1wR1UxRXlSWGxVV0d4VFlteEtWVll3WkZOV2JHeHlWMjFHVjFKdGVEQlViRnBQWVd4S2RGVnNh
RnBXVmxVeFdWWmFTMVpXV25WaApSbVJYWld0YWIxZFdXbXRTTWs1eVRsWldXQXBpVlZwVVZtMTBk
MVZXWkZkVmEyUnBZbFphV0ZadE5WZFZaM0JwVTBWS2VsZFdVa05rCk1sWlhWbGhvV0dKWVFrOVZi
RkpYVTBaa2NWUnVUbGRhTTBKWlZXcEdTMlZXV2tkYVNHUlhDazFzV25wV1YzaGhWbTFLUms1WE9W
VlcKVmtwRVZHeGFZVmRGTVZoU2JGcFNWMFZLV1ZaR1ZtdE5SVFZIVjJ0V1UySllVbFZEYlVwWFYy
NXNWV0pHY0haV2JHUkhaRWRXUmxacwphR2tLWWxScmVsWkVSbGRVTWtwelVXeFdUbEpZVGt4RFp6
MDlDZz09Cg==
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/repetitions]
└─$ cat enc_flag| base64 -d | base64 -d| base64 -d
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aUApWMGt4VDFkSmVrNVhUamxEWnowOUNnPT0K
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/repetitions]
└─$ cat enc_flag| base64 -d | base64 -d| base64 -d | base64 -d
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZP
V0kxT1dJek5XTjlDZz09Cg==
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/repetitions]
└─$ cat enc_flag| base64 -d | base64 -d| base64 -d | base64 -d |base64 -d
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfOWI1OWIzNWN9Cg==
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/repetitions]
└─$ cat enc_flag| base64 -d | base64 -d| base64 -d | base64 -d |base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}

```
## Notas Adicionales 
## Referencias