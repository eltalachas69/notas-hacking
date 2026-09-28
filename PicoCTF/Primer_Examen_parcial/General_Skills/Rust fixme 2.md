## Descripción
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?

Download the Rust code [here](https://challenge-files.cylabacademy.net/library/048c73621a97b98cde18eae5a9495279f2396cb64c65235bb310e7ad26d726ac/fixme2.tar.gz).
## Solución
Solo se tenia que añadir "mut" en los que estaba con `&` para asi tener la bandera la cual es `academy{4r3_y0u_h4v1n5_fun_y31?}`
```
┌──(kali㉿kali)-[~/…/General_Skills/Rust_fixme_2/fixme2/src]
└─$ cargo run
   Compiling rust_proj v0.1.0 (/home/kali/Projects/picoCTF/Primer_Examen_parcial/General_Skills/Rust_fixme_2/fixme2)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.53s
     Running `/home/kali/Projects/picoCTF/Primer_Examen_parcial/General_Skills/Rust_fixme_2/fixme2/target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: academy{4r3_y0u_h4v1n5_fun_y31?}
                                                                                                                    
┌──(kali㉿kali)-[~/…/General_Skills/Rust_fixme_2/fixme2/src]
└─$ 

```
## Notas Adicionales 
## Referencias