## Descripción
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://challenge-files.cylabacademy.net/library/b21cf2891dc0aa8e13e806fc64fbf0a6f01d47760f7905540cf3a7139a3fc778/VaultDoor4.java)
## Solución
Pues simplemente andaba checando lo ultimo y pues ahi mismo me daba la bandera pero en ascii, otra en hexadecimal y ya la tercera estaba en octal, en la cuarta parte no era necesario hacer nada ya que pues ya esos caracteres debian de estar, entonces primero vi y cheque el ascii de los primeros, los otros dos use cyberchef para resolverlo, la bandera que me dio fue `academy{jU5t_4_bUnCh_0f_bYt3s_88a31dad6c}`

```
byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 070 , 070 ,
            'a' , '3' , '1' , 'd' , 'a' , 'd' , '6' , 'c' ,
        };
```
## Notas Adicionales 
## Referencias
[ASCII](https://elcodigoascii.com.ar/)
[Hexadecimal](https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=IDB4NTUsIDB4NmUsIDB4NDMsIDB4NjgsIDB4NWYsIDB4MzAsIDB4NjYsIDB4NWY)
[Octal](https://gchq.github.io/CyberChef/#recipe=From_Octal('Space')&input=MTQyIDEzMSAxNjQgNjMgMTYzIDEzNyA3MCA3MA)