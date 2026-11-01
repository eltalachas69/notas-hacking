## Descripción
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

Connect with nc fickle-tempest.picoctf.net 57147.
## Solución
Hay varias soluciones para resolver esto, en mi caso fue un codigo de python
```
import socket
import re

host = 'fickle-tempest.picoctf.net'
port = 49687

conectarse = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
conectarse.connect((host, port))
def recibir_mensajes(sock):
    datos = conectarse.recv(1024)
    datos_texto = datos.decode('utf-8')
    return datos_texto

def decodificar_dato(texto):
    if re.search(r"\bo([0-7]{3})\b", texto):
        octanal = re.findall(r"\bo([0-7]{3})\b", texto)
        texto_octanal = "".join([chr(int(o, 8)) for o in octanal])
        return texto_octanal

    elif re.search(r"[01]+", texto):
        binario = re.findall(r"[01]+", texto)
        texto_binario = "".join([chr(int(b,2)) for b in binario])
        return texto_binario

    else:
       hexadecimal = re.findall(r'\b[0-9a-fA-F]{2,}\b',texto)
       texto_hexo = "".join(hexadecimal)
       texto_hexadecimal = bytes.fromhex(texto_hexo).decode('utf-8')
       return texto_hexadecimal

def mandar_mensaje(mensaje):
    enviar_mensaje = mensaje+"\n"
    conectarse.sendall(enviar_mensaje.encode('utf-8'))

while True:
     texto=recibir_mensajes(conectarse)
     if not texto:
         break
     else:
       print(texto)
       mensaje = decodificar_dato(texto)
       mandar_mensaje(mensaje)




```
Utilice 2 imports, el socket y el re, socket es para conectarse con el host y port, re es para buscar en los textos que recibia del netcat.
Donde me complique mas fue en la hexadecimal porque no sabia como tomarlo pero al final se pudo aunque en esa al final es prueba y error.
```
┌──(kali㉿kali)-[~]
└─$ python3 hoal.py
Let us see how data is stored
test
Please give the 01110100 01100101 01110011 01110100 as a word.
...
you have 45 seconds.....

Input:

Please give me the  o146 o141 o154 o143 o157 o156 as a word.
Input:

Please give me the 636f6c6f7261646f as a word.
Input:

WRONG!

                                                                                                                                                            
┌──(kali㉿kali)-[~]
└─$ python3 hoal.py
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:

Please give me the  o154 o151 o172 o141 o162 o144 as a word.
Input:

Please give me the 6c696d65 as a word.
Input:

You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_acdCcfCa}

```

## Notas Adicionales 
## Referencias
