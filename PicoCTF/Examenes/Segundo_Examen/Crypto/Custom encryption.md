## Descripción
Can you get sense of this code file and write the function that will decode the given encrypted file content.

Find the encrypted file here [flag_info](https://challenge-files.cylabacademy.net/library/168dfb66953daef3e9c494a5ee63a78f09370e1e39d8b1489d5f9c090acd2a8f/enc_flag) and [code file](https://challenge-files.cylabacademy.net/library/168dfb66953daef3e9c494a5ee63a78f09370e1e39d8b1489d5f9c090acd2a8f/custom_encryption.py) might be good to analyze and get the flag.
## Solución
Esto era una encriptacion de XOR, en el mismo codigo se agrego unos metodos para desencriptarlo para saber que es lo que decia el cipher, la cual era la bandera que es `academy{custom_d2cr0pt6d_200ccafe}`
```
def decrypt(cipher, key):
    plaintext = ""
    for encrypted_value in cipher:
        decrypted_value = encrypted_value // (key * 311)
        plaintext += chr(decrypted_value)
    return plaintext

def test2():
    p = 97
    g = 31
    a = 91
    b = 25

    u = generator(g, a, p)
    v = generator(g, b, p)
    key = generator(v, a, p)
    b_key = generator(u, b, p)
    shared_key = key
    cipher = [148347, 379109, 313177, 82415, 98898, 32966, 1137327, 1120844, 1054912, 692286, 0, 1368089, 346143, 82415, 1120844, 0, 362626, 1417538, 16483, 1021946, 395592, 445041, 98898, 98898, 280211, 98898, 428558, 197796, 412075, 379109, 280211, 82415, 98898, 0]

    semi_cipher = decrypt(cipher, shared_key)

    flag = dynamic_xor_decrypt(semi_cipher, "trudeau")

    print(flag)

```
## Notas Adicionales 
## Referencias

