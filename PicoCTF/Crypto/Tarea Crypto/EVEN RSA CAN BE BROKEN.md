## Descripción
This service provides you an encrypted flag. Can you decrypt it with just N & e?
## Solución
Para solucionarlo teniamos que sacar los p y q de la n, esto se saca sabiendo si n es par, ya que si se multiplica p puede ser a 2 y la q es la mitad de N, entonces como si hay ya tenemos para p y q, esto nos sirve para sacar el phi y hacer la decodificacion para sacar la m, la bandera que nos dio es `academy{tw0_1$_pr!m3cfb893a9}`
```
┌──(kali㉿kali)-[~/Projects/picoCTF/cripto/tarea]
└─$ python
Python 3.14.7 (main, Sep  5 2026, 05:55:41) [GCC 16.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> n = 25368176226342670336132381198339079247845719545854659605191237772908652322002544387027373019534522511233765101591902956295915303335535644380323427716279066
>>> e = 65537
>>> c = 24882702401390495593917839789694850381209280596666182198890812425331757767180745487564918297862803365629234121180908453969797285282665825411681092199587459
>>> p = 2
>>> q = n//2
>>> phi = q-1
>>> d = pow(e,-1,phi)
>>> m = pow(c,d,n)
>>> hex_testo = hex(m)[2:]
>>> if len(hex_testo)%2!=0:
...     hex_testo = '0' + hex_testo
...     
>>> mensaje = bytes.fromhex(hex_testo).decode('utf-8', errors='ignore')
>>> mensaje
'academy{tw0_1$_pr!m3cfb893a9}'
>>> 

```
## Notas Adicionales 
## Referencias
