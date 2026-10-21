## Descripción
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://challenge-files.cylabacademy.net/library/f3895827512c6fab64095a69942e62ba9e367bb32d70ff69dc0e8fd9a826936a/message.txt).

Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.

Wrap your decrypted message in the academy flag format (i.e. `academy{decrypted_message}`)
## Solución
Esto basicamente se podria resolver haciendo un codigo en python, basicamente nos pedian sacar el residuo con 37, ahi mismo nos decia que el 0 equivalia la a, el 1 el b y asi, ,esto se podia sacar en codigo pero la verdad solo saque los numeros y ya los estaba viendo uno por uno en el bloc de notas, no es optimo pero pues como no eran muchos numeros me di el tiempo de hacerlo asi
Codigo:
```
┌──(kali㉿kali)-[~/…/picoCTF/cripto/cripto4/basicmod1]
└─$ python
}Python 3.14.7 (main, Sep  5 2026, 05:55:41) [GCC 16.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> lista = [313, 396, 353, 161, 336, 73, 198, 406, 202, 285, 57, 346, 151, 332, 328, 216, 214, 70, 286, 360, 72, 21
>>> for numero in lista:
...     print(numero%37)
...     
17
26
20
13
3
36
13
36
17
26
20
13
3
36
32
31
29
33
27
27
35
31

```

Bloc de notas:
```
0=a
1=b
2=c
3=d
4=e
5=f
6=g
7=h
8=i
9=j
10=k
11=l
12=m
13=n
14=o
15=p
16=q
17=r
18=s
19=t
20=u
21=v
22=w
23=x
24=y
25=z
26=0
27=1
28=2
29=3
30=4
31=5
32=6
33=7
34=8
35=9
36=_

academy{r0und_n_r0und_65371195}
```
## Notas Adicionales 
## Referencias
