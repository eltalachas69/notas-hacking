## Descripción
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.cylabacademy.net/library/4a463561643f2cc25e74665dadd7ca654a9b828dc7a5b9239a8000ab4179c57e/whitepages.txt) is all blank!
## Solución
Viendo en una pagina me dice que esta codificado en UTF-8, entonces con un script en python podemos saber que dice la bandera
```
def convertSpacesToBinary():
    with open('whitepages.txt', 'rb') as f:
        result = f.read()
    result = result.replace(b'\xe2\x80\x83', b'0')  # Unicode EM SPACE -> 0
    result = result.replace(b'\x20', b'1')  # ASCII Space -> 1
    result = result.decode()
    return result

def convertFromBinaryToASCII(binaryValues):
    binary_int = int(binaryValues, 2)
    byte_number = (binary_int.bit_length() + 7) // 8
    binary_array = binary_int.to_bytes(byte_number, "big")
    ascii_text = binary_array.decode('ascii')
    print(ascii_text)

convertFromBinaryToASCII(convertSpacesToBinary())

```
Al ejecutarlo nos da la bandera que es `academy{not_all_spaces_are_created_equal_743510e5f5459071ed7d4109b7832a8e}`
## Notas Adicionales 
## Referencias
[Tipo de codigo](https://flipperfile.com/text-tools/txt-encoding-detector/)