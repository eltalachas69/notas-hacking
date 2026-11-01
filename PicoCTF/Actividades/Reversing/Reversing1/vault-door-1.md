## Descripción
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://challenge-files.cylabacademy.net/library/60e8fbcf22f4bfa0e9856c1ebbd5506050d5f0ab9fb013f9e3e175021205869b/VaultDoor1.java)
## Solución
Para resolverlo me meti al codigo y vi que estaba ordenado del menor al mayor hasta mero abajo entonces lo que primero fue pegarlo y usar un comando de linux para ordenarlo numericamente que era el sort, pero no me lo ordeno bien al principio y era mas que nada por los numeros porque primero representaba del 0,1,2...10,11,12... Pero me los ordeno de una forma que no queria porque era 0,10,11,12 esto yo pienso que fue porque como eran dos digitos los tomaba como prioridad entonces lo que hice fue ponerles un cero al principio los que eran de un solo digito y ya me lo ordeno como debia de ser y la bandera es `academy{d35cr4mbl3_tH3_cH4r4cT3r5_45ebc3}`
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Reversing/vaultdoor1]
└─$ sort -n lista.txt 
password.charAt(0)  == 'd' &&
               password.charAt(10) == '_' &&
               password.charAt(11) == 't' &&
               password.charAt(12) == 'H' &&
               password.charAt(1)  == '3' &&
               password.charAt(13) == '3' &&
               password.charAt(14) == '_' &&
               password.charAt(15) == 'c' &&
               password.charAt(16) == 'H' &&
               password.charAt(17) == '4' &&
               password.charAt(18) == 'r' &&
               password.charAt(19) == '4' &&
               password.charAt(20) == 'c' &&
               password.charAt(21) == 'T' &&
               password.charAt(22) == '3' &&
               password.charAt(23) == 'r' &&
               password.charAt(24) == '5' &&
               password.charAt(2)  == '5' &&
               password.charAt(25) == '_' &&
               password.charAt(26) == '4' &&
               password.charAt(27) == '5' &&
               password.charAt(28) == 'e' &&
               password.charAt(29) == 'b' &&
               password.charAt(30) == 'c' &&
               password.charAt(31) == '3';
               password.charAt(3)  == 'c' &&
               password.charAt(4)  == 'r' &&
               password.charAt(5)  == '4' &&
               password.charAt(6)  == 'm' &&
               password.charAt(7)  == 'b' &&
               password.charAt(8)  == 'l' &&
               password.charAt(9)  == '3' &&

┌──(kali㉿kali)-[~/Projects/picoCTF/Reversing/vaultdoor1]
└─$ sort -n lista.txt
password.charAt(00)  == 'd' &&
               password.charAt(01)  == '3' &&
               password.charAt(02)  == '5' &&
               password.charAt(03)  == 'c' &&
               password.charAt(04)  == 'r' &&
               password.charAt(05)  == '4' &&
               password.charAt(06)  == 'm' &&
               password.charAt(07)  == 'b' &&
               password.charAt(08)  == 'l' &&
               password.charAt(09)  == '3' &&
               password.charAt(10) == '_' &&
               password.charAt(11) == 't' &&
               password.charAt(12) == 'H' &&
               password.charAt(13) == '3' &&
               password.charAt(14) == '_' &&
               password.charAt(15) == 'c' &&
               password.charAt(16) == 'H' &&
               password.charAt(17) == '4' &&
               password.charAt(18) == 'r' &&
               password.charAt(19) == '4' &&
               password.charAt(20) == 'c' &&
               password.charAt(21) == 'T' &&
               password.charAt(22) == '3' &&
               password.charAt(23) == 'r' &&
               password.charAt(24) == '5' &&
               password.charAt(25) == '_' &&
               password.charAt(26) == '4' &&
               password.charAt(27) == '5' &&
               password.charAt(28) == 'e' &&
               password.charAt(29) == 'b' &&
               password.charAt(30) == 'c' &&
               password.charAt(31) == '3';
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/Reversing/vaultdoor1]
└─$ echo "academy{d35cr4mbl3_tH3_cH4r4cTr5_45ebc3}" > bandera.txt 
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/Reversing/vaultdoor1]
└─$ echo "academy{d35cr4mbl3_tH3_cH4r4cT3r5_45ebc3}" > bandera.txt
                                                                    
```
## Notas Adicionales 
## Referencias
