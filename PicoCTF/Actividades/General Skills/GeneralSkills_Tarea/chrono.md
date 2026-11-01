## Descripción
How to automate tasks to run at intervals on linux servers?

Use ssh to connect to this server:

`Server: saturn.picoctf.net Port: 56071 Username: picoplayer Password: pYkku7iMsS`
## Solución
No se si asi sea la solucion pero igual use un `grep` y me salio la bandera aunque fueron muchos archivos despues de ahi
```
picoplayer@challenge:/$ grep -r "picoCTF{"
grep: etc/.pwd.lock: Permission denied
grep: etc/gshadow: Permission denied
grep: etc/security/opasswd: Permission denied
grep: etc/shadow: Permission denied
grep: etc/ssh/ssh_host_ecdsa_key: Permission denied
grep: etc/ssh/ssh_host_ed25519_key: Permission denied
grep: etc/ssh/ssh_host_rsa_key: Permission denied
grep: etc/ssh/ssh_host_dsa_key: Permission denied
etc/crontab:# picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}

```
## Notas Adicionales 
## Referencias