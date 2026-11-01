## Descripción
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.

[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/ce53ef9432bf367be41e465224d721c1187c39debcd758efcd28e99a6b7ff7a4/Addadshashanammu.zip)
## Solución
Simplemente es usar el tabulador de nuestro teclado para ahorrarnos de escribir, pero para encontrar la bandera tenemos que descomprimir un archivo
```
──(kali㉿kali)-[~/Projects/picoCTF/Tab-Tab-Attack]
└─$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
 extracting: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet.c  
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/Tab-Tab-Attack]
└─$ ls
Addadshashanammu  Addadshashanammu.zip
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/Tab-Tab-Attack]
└─$ cd Addadshashanammu 

```
La manera mas facil de seguir es igual usando el tab hasta llegar a la ultima carpeta
```
┌──(kali㉿kali)-[~/Projects/picoCTF/Tab-Tab-Attack/Addadshashanammu]
└─$ cd Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku 
                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls -l
total 24
-rwxr-xr-x 1 kali ElCuilango 16712 Dec 12  2025 fang-of-haynekhtnamet
-rw-r--r-- 1 kali ElCuilango    96 Dec 12  2025 fang-of-haynekhtnamet.c

```
Tenemos un archivo ejecutable, lo abrimos y ahi esta nuestra bandera
```
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}

```
## Notas Adicionales 
## Referencias