## Descripción
Can you find the flag in this disk image? Wrap what you find in the academy{} flag format. Download the disk image [here](https://challenge-files.cylabacademy.net/library/bf9a20c350075c5863371e078daee1d570d4062902edc8a4a042e02a7cebf161/partition4.img.gz).
## Solución
Para allar la bandera se tenia que ver que tanto cambio o se modifico los archivos de la img, para eso se tenia que hacer un registro de toda la imagen, al hacer el registro de la imagen se uso el mactime para convertirlo en texto legible, hay un archivo curioso que habia ahi que tenia el año 1985, entonces lo extraje y estaba en base64, use cyberchef y me dio el contenido dentro de la bandera que es `academy{71m311n3_0u7113r_h3r_43a2e7af}`
## Notas Adicionales 
## Referencias
[Base64](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=TnpGdE16RXhiak5mTUhVM01URXpjbDlvTTNKZk5ETmhNbVUzWVdZSw)
