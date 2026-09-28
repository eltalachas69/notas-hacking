## Descripción
BookShelf Pico, my premium online book-reading service.

I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book! Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/42628968e19dda614759290450f9ab06e4c37183b6a07886784d4e8341e69aab/bookshelf-pico.zip).

Website can be accessed [here!](http://xebec.cylabacademy.net:35897/).
## Solución
Para esto checamos la cookie del almacenamiento local con esto usamos `jwt.io` para poder cambiarle sus valores, esto lo vemos que es en el codigo de java que es secretgenerator que ahi nos da la clave que es '1234', una vez eso cambiaos sus propiedades a las siguientes
```
{
  "role": "Admin",
  "iss": "bookshelf",
  "exp": 1791164086,
  "iat": 1790559286,
  "userId": 2,
  "email": "user"
}
```
Con eso volvemos y cambiamos la propiedad de almacenamiento local y nos da la bandera que es `academy{w34k_jwt_n0t_g00d_d3a1bea8}`

## Notas Adicionales 
## Referencias