## Descripción
How well can you perfom basic binary operations?
## Solución
En esta solucion tenia dos terminales abiertas, una para ejecutar un codigo de python y otra donde tenia `nc` para conectarme al puerto y host que me dieron, pude haberlo hecho de otra manera pero pues al final lo hice asi porque no era como otro que tenia limite de tiempo, el codigo de python es este:
```
numero_1 = int(input(),2)
numero_2 = int(input(),2)
caracter = input("Dame el caracter ")

if caracter == '+':
    resultado = bin(numero_1 + numero_2)[2:]
    print(resultado)
elif caracter == '-':
    resultado = bin(numero_1 - numero_2)[2:]
    print(resultado)
elif caracter == '*':
    resultado = bin(numero_1 * numero_2)[2:]
    print(resultado)
elif caracter == '&':
    resultado = bin(numero_1 & numero_2)[2:]
    print(resultado)
elif caracter == '|':
    resultado = bin(numero_1 | numero_2)[2:]
    print(resultado)
elif caracter == '<<':
    resultado = bin(numero_1 << 1)[2:]
    print(resultado)
else:
    resultado = bin(numero_2 >> 1)[2:]
    print(resultado)

binario = "11011010"
hexadecimal = hex(int(binario, 2))
print(hexadecimal)


```
Mientras que lo estaba ejecutando tenia la otra ventana para ingresar los datos
```
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ nc titan.picoctf.net 64583

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00111101
Binary Number 2: 10011101


Question 1/6:
Operation 1: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10010101101001
Correct!

Question 2/6:
Operation 2: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11101
Correct!

Question 3/6:
Operation 3: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 1111010
Correct!

Question 4/6:
Operation 4: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 11110 
Incorrect. Try again
Enter the binary result: 1001110
Correct!

Question 5/6:
Operation 5: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10111101
Correct!

Question 6/6:
Operation 6: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11011010
Correct!

Enter the results of the last operation in hexadecimal: 0xda

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}

```
Al final me pedia que convirtiera el ultimo binario en hexadecimal y pues lo guarde en una variable y ahi lo converti
```
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ vim programa.py    
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ vim programa.py
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
00111101
10011101
Dame el caracter *
10010101101001
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
00111101
10011101
Dame el caracter &
11101
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ vim programa.py
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
00111101
10011101
Dame el caracter <<
1111010
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
00111101
10011101
Dame el caracter >>
11110
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
>>
Traceback (most recent call last):
  File "/home/kali/Projects/picoCTF/General_Skills_Tarea/binhexa/programa.py", line 1, in <module>
    numero_1 = int(input(),2)
ValueError: invalid literal for int() with base 2: '>>'
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ vim programa.py    
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
00111101
10011101
Dame el caracter >>
1001110
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
00111101
10011101
Dame el caracter |
10111101
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
00111101
10011101
Dame el caracter +
11011010
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ vim programa.py
                                                                                                                                                            
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills_Tarea/binhexa]
└─$ python3 programa.py
00111101
10011101
Dame el caracter +
11011010
0xda

```
Se me olvido que en la de comparar tuve con `>>` o `<<` tuve que cambiarle las variables cuando no era el numero binario correcto
## Notas Adicionales 
## Referencias