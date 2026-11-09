## Descripción
What does asm3(0xc682a0b0,0xf2b059d1,0xccc1df85) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://challenge-files.cylabacademy.net/library/9c1d403a72b67a2f8ea1eaec314c81ec2ee7b35b74e25a9d48718b9f5dfdc8a2/test.S)
## Solución
En este caso use una pagina que nos dio el profe, esto porque aunque sea corto el programa nos ibamos a tomar tiempo en analizarlo uno por uno, al final me dio la bandera que es `0x1DCF`

```
start:
	push 0xccc1df85
	push 0xf2b059d1
	push 0xc682a0b0
	call asm3
	
asm3:
	push   ebp
    mov    ebp,esp
    xor    eax,eax
    mov    ah,BYTE PTR [ebp+0xa]
    shl    ax,0x10
    sub    al,BYTE PTR [ebp+0xf]
    add    ah,BYTE PTR [ebp+0xc]
    xor    ax,WORD PTR [ebp+0x12]
    nop
    pop    ebp
    ret

```
## Notas Adicionales 
## Referencias
[Pagina](https://carlosrafaelgn.com.br/Asm86/)
