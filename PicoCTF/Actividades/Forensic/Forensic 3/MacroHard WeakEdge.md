## Descripción
I've hidden a flag in this file. Can you find it? [Forensics_is_fun.pptm](https://challenge-files.cylabacademy.net/library/ef35dfe613527d28fe872d94179b53bc1a0497ddecf57e51d160c910be3a8e8a/Forensics_is_fun.pptm)
## Solución
Para extraerlo use el mismo comando `binwalk` y me salio `.zip` en el archivo, entonces lo extraje y buscando uno por uno en la carpeta ppt, en slidemasters hay un archivo que se llama hidden, mandando ese archivo al cyberchef me sale la bandera que es `academy{D1d_u_kn0w_ppts_r_z1p5}`

## Notas Adicionales
De lo que trata el reto es que por ejemplo un archivo ppt es solo un zip con varios archivos, osea es un zip pero con otro nombre en otras palabras
## Referencias
[Cyberchef](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=WiBtIHggaCBaIHogbyBnIFkgVyBOIGggWiBHIFYgdCBlIFggdCBFIE0gVyBSIGYgZCBWIDkgciBiIGogQiAzIFggMyBCIHcgZCBIIE4gZiBjIGwgOSA2IE0gWCBBIDEgZiBR)
