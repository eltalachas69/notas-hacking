## Descripción
Find the flag in the Python script!

[Download Python script](https://artifacts.picoctf.net/c/37/serpentine.py)
## Solución
No fue tan complicado, solo puse la funcion `print_flag()` cuando se escogia 'b' y ya me daba la bandera
```
┌──(kali㉿kali)-[~/Projects/picoCTF/General_Skills3]
└─$ python3 serpentine.py
/home/kali/Projects/picoCTF/General_Skills3/serpentine.py:41: SyntaxWarning: invalid escape sequence '\ '
  /     \      .- ~ ~ -.

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}

```
## Notas Adicionales 
## Referencias