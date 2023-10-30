# LFTS - Comments

## 52. Write the Markup for a Post Comment
    Creamos la vista para los commentarios, de la misma manera de la que lo hemos venido haciendo, utilizando blade

![Visual Studio Code](./images/comments%2052.PNGG "Creacion de la vista para commentarios")

![Visual Studio Code](./images/show%2052.PNG "Modificacion de la vista de de los post para que muestre la seccion de de los comentarios")


## 53. Table Consistency and Foreign Key Constraints
    Ahora que creamos la vista para los comentarios tenemos que agregar la tabla y darle consistencia para poder usarla igual que las otras tablas que hemos creado

#### Para crear todo esto a la vez utilzamos el php artisan

```
php artisan make:model -cfm
```

![Visual Studio Code](./images/comment-model%20%2053.PNG "Creacion del modelo para los comentarios")

![Visual Studio Code](./images/comment-controller%20%2053.PNG "Creacion del controlador para los comentarios")

![Visual Studio Code](./images/comment-factory%20%2053.PNG "Creacion del factory para los comentarios")

![Visual Studio Code](./images/comment-table%2053.PNG "Creacion de la migracion para la tabla de los comentarios")

![Visual Studio Code](./images/post-migrate%2053.PNG "Modificacion de la de la base de datos de los post para que tenga sentido con los cambios que acabamos de hacer")



## 54. 
## 55. 
## 56. 
## 57. 
