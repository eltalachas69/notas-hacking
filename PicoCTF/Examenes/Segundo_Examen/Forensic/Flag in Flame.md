## Descripción
The SOC team discovered a suspiciously large log file after a recent breach. When they opened it, they found an enormous block of encoded text instead of typical logs. Could there be something hidden within? Your mission is to inspect the resulting file and reveal the real purpose of it. The team is relying on your skills to uncover any concealed information within this unusual log. Download the encoded data here: [Logs Data](https://challenge-files.cylabacademy.net/library/8389f7eb8ae95fd4453f1e2d27498905b415efec5fc738bfd0983d56c09959bf/logs.txt). Be prepared—the file is large, and examining it thoroughly is crucial .
## Solución
Para solucionarlo cheque que tenia dentro los logs, era puro base64 entonces al principio pense que era un textote pero me salio que era una imagen en cyberchef cuando le subi el archivo, entonces descargue la imagen y ahi abajo hay un texto codificado en hex, entonces al decodificarlo me dio la bandera que es `academy{forensics_analysis_is_amazing_dfc2b4b9}`
## Notas Adicionales 
## Referencias
[Base64](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false))
[Hexadecimal](https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=NjE2MzYxNjQ2NTZENzk3QjY2NkY3MjY1NkU3MzY5NjM3MzVGNjE2RTYxNkM3OTczNjk3MzVGNjk3MzVGNjE2RDYxN0E2OTZFNjc1RjY0NjY2MzMyNjIzNDYyMzk3RA&oeol=FF)
