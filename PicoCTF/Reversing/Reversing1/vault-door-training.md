## Descripción
Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open. Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer! You will need to read the source code for each level to figure out what the password is for that vault door. As a warmup, we have created a replica vault in our training facility.

The source code for the training vault is here: [VaultDoorTraining.java](https://challenge-files.cylabacademy.net/library/78ec91618d4c4219c55fbe2c9fc67ec6e248664564e6b2f13a54534aaf1d1000/VaultDoorTraining.java)
## Solución
Para resolver la bandera en mi caso yo fui a checar el codigo y ahi estaba la bandera, pues el contenido que estaba dentro, ya eso lo puse para ver si esa era la bandera y pues si era, la bandera es `academy{w4rm1ng_Up_w1tH_jAv4_8352733cecd}`
```
public boolean checkPassword(String password) {
    return password.equals("w4rm1ng_Up_w1tH_jAv4_8352733cecd");
}

```
## Notas Adicionales 
## Referencias
