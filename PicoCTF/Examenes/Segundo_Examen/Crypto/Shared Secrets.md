## Descripción
A message was encrypted using a shared secret... but it looks like one side of the exchange leaked something. Can you piece together the secret and get the flag? Download the [message](https://challenge-files.cylabacademy.net/library/696a330c92491df25f02f3f20e552a2b8b1b8fd8c5ffc3b3902b972c24638f19/message.txt). And source [code](https://challenge-files.cylabacademy.net/library/696a330c92491df25f02f3f20e552a2b8b1b8fd8c5ffc3b3902b972c24638f19/encryption.py)
## Solución
Usando los datos que se nos dio se puede sacar la bandera mediante a los datos que se nos dio, por ejemplo la llave usa una encriptacion XOR, el codigo que nos da es que hace un calculo para darnos el valor de cada letra en un archivo .txt, la llave se puede sacando el compartido que es una potencia entre la A, b y p, y sacar su residuo con 256, al tener esto ya me dio la bandera que es `academy{dh_s3cr3t_441eb9ee}`
```
──(kali㉿kali)-[~/…/Examenes/SegundoExamen/Crypto/SharedSecrets]
└─$ python
Python 3.14.7 (main, Sep  5 2026, 05:55:41) [GCC 16.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> g = 2
>>> p = 2927273144810939766701580090813587829846998218139050366191650895496341639672151115600622801622875986429173669666450605563086095565809406776099318149676703864803530494465478726922189453273460829331935414785533102652757649572940\
785971419755291375295328412738229475603220295990344218551730029944293124696567146516090193
>>> A = 5730648581087755877964010315061578770183482884262264702855242056791360759710727535672973557631636158704029916911878507463361690422626926104834258598309708035638242850740335972227693455565336663449797474865713811745091404553985\
67155637545070339870299749606406694126580709457390475875189904723414950764573551900114879
>>> b = 3104809848458447823504699294889571034040656729676817217944339685980786066784575741159488933426580163888503009515486893903625862850819231582509128619289546066839713739596522872466594108078046030533754921042351147826983359622927\
73627028417650732575398422905666599383548621368163602765974099546321049636858616564366046
>>> enc = "43414346474f5b59464a7d5111415011567d16161347401b47475f"
>>> compartido = pow(A,b,p)
>>> llave = compartido % 256
>>> key
Traceback (most recent call last):
  File "<python-input-7>", line 1, in <module>
    key
NameError: name 'key' is not defined
>>> llave
34
>>> cifrado = bytes.fromhex(enc)
>>> bandera = bytes([byte ^ for byte in cifrado])
  File "<python-input-10>", line 1
    bandera = bytes([byte ^ for byte in cifrado])
                            ^^^
SyntaxError: invalid syntax
>>> bandera = bytes([byte ^llave for byte in cifrado])
>>> bandera
b'academy{dh_s3cr3t_441eb9ee}'

```
## Notas Adicionales 
## Referencias
