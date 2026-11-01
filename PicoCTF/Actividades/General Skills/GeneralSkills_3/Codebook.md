## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)
## Solución
Lo que trata es correr el programa de python, pero esto lo debemos de hacer en la misma carpeta ya que si tenemos el `code.py` en otro lado sin el `codebook.txt` este nos marcara un error, si tenemos esos dos archivos en la misma carpeta nos dara la bandera
``` 
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3/Codebook]
└─$ ls
codebook.txt  code.py
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3/Codebook]
└─$ python3 code.py               
picoCTF{c0d3b00k_455157_197a982c}
                                                                                                                                                           
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3/Codebook]
└─$ python3 code.py
Couldn't find codebook.txt. Did you download that file into the same directory as this script?

```
## Notas Adicionales 
## Referencias
