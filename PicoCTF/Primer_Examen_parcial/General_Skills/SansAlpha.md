## Descripción
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols. `ssh -p 23600 ctf-player@xebec.cylabacademy.net`

Use password: `fa1a82ad`
## Solución
En este reto se tenia que usar el uso de las wildcard para poder ver la bandera, la cual estaba encriptada en base64 y luego de decodificarla salio que era `academy{7h15_mu171v3r53_15_m4dn355_9b767f07}`
```
SansAlpha$ ./*/*
\x1b[?2004l
bash: ./blargh/flag.txt: Permission denied
\x1b[?2004h
SansAlpha$ /???/??????
\x1b[?2004l
/bin/base32: extra operand ‘/bin/basenc’
Try '/bin/base32 --help' for more information.
\x1b[?2004h
SansAlpha$ /???/???[!_]64 /????/??????????/??????/????????
\x1b[?2004l
cmV0dXJuIDAgYWNhZGVteXs3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV85Yjc2N2YwN30=
\x1b[?2004h
SansAlpha$ 
Traceback (most recent call last):
  File "/usr/local/sansalpha.py", line 11, in <module>
    user_in = input("SansAlpha$ ")
              ^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pwnlib/term/readline.py", line 453, in str_input
    return readline(-1, prompt, float).decode().rstrip(os.linesep)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pwnlib/term/readline.py", line 399, in readline
    keymap.handle_input()
  File "/usr/local/lib/python3.12/dist-packages/pwnlib/term/keymap.py", line 24, in handle_input
    self.send(key.get())
              ^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pwnlib/term/key.py", line 180, in get
    _read(timeout)
  File "/usr/local/lib/python3.12/dist-packages/pwnlib/term/key.py", line 168, in _read
    _cbuf.extend(getraw(timeout))
                 ^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pwnlib/term/key.py", line 45, in getraw
    c = getch(timeout)
        ^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/dist-packages/pwnlib/term/key.py", line 28, in getch
    rfds, _wfds, _xfds = select.select([_fd], [], [], timeout)
                         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
KeyboardInterrupt
Connection to xebec.cylabacademy.net closed.
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ echo "cmV0dXJuIDAgYWNhZGVteXs3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV85Yjc2N2YwN30=" | base64 -d
return 0 academy{7h15_mu171v3r53_15_m4dn355_9b767f07}    
```
## Notas Adicionales 
## Referencias