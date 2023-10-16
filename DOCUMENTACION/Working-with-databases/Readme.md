# LFTS - Working With Database


## 17. Environment Files and Database Connections
    este paso es basicamente lo ultimo que hicimos en la ultima clase, configuracion de la basede datos y migracion tablas

### Configuracion de .env 
Configuramos el espacio que tiene preasignado el .env con los datos de nuestra base de datos

![Terminal bash]( ./Images/configuracion%20de%20la%20conexion%20a%20la%20base%20de%20datos.PNG "Configuramos el espacio que tiene preasignado el .env con los datos de nuestra base de datos")

### creamos el esquema la base de datos

![Terminal bash]( ./Images/confirmacion%20de%20creacion%20de%20tabla%20en%20base%20de%20datos.PNG "Confirmacion de la creacion de la base de datos lfts")

###  Migracion de la tablas de artisan

![Terminal bash]( ./Images/confirmacion%20de%20la%20migracion%20db.PNG "Creacion de tablas")



## 18. Migrations: The Absolute Basics
    Nos enseñan conceptos basicos de las migraciones la mayoria de ellos en torno al:

    ´´´
    php artisan migrate:fresh
    ´´´
    Esto basicamente no importa los cambias que podamos hacer ya sea en el archivo de complilacion de laravel o desde el administrador de base de datos siempre restablece todo a la migracion oiginal
    Tambien nos muestra un pequeño detalle pero que me parecio muy conveniente que es que basicamente si nos encontramos en el ambiente de produccion antes de correr este codigo nos muestra una alerta, avisandonos que estamos en el entorno de produccion.
    tambien nos enseña cosas como

    ´´´
    php artisan migrate:rollback
    ´´´
![Terminal bash]( ./Images/phpartisan%20comandos.PNG "Comandos disponibles con artisan")



## 19. Eloquent and the Active Record Pattern
    Utilizando el php artisan tinker creamos y visualizamos usuarios

### Creacion de usuario
   Utilizando tinker es posible crear usuarios en la base de datos
![Terminal bash]( ./Images/Creacion%20de%20usuario%20phptinker.PNG "Creacion de usuario")

### Visualizar usuarios
    Tambien es posible ver los usuarios que hemos creado
![Terminal bash]( ./Images/Usuarios%20phptinker.PNG "Ver Usuarios creados")

Y obiviamente estos usuarios no son exclusivos del php artisan tinker, esto afecta la base de datos y por ende los podemos ver desde nuestro administrador de base de datos
![MySQL Workbench]( ./Images/UsuariosWorkbench.PNG "Ver Usuarios creados")



## 20. Make a Post Model and Migration
    Ahora vamos a crear la tabla y el modelo post para almacenar post

### Creacion de tabla y modelo
    vamos a crear la tabla y el modelo de post para esto vamos a utilizar el siguente comando
```
    php artisan make:migration create_posts_table
    php artisan make:model Post
```

### Asignar columnas a la tabla
Vamos a asignar unas columnas a la tabla que acabamos de crear

![Visual Studio Code]( ./Images/UsuariosWorkbench.PNG "Creacion de columnas")

despues de esto ocupamos migrar estas columnas con el comando
 ```
 php artisan migrate
 ```

### Creacion de datos para Posts
    De la misma manera en la que creamos los usuarios en el ep. 19 vamos a crear datos para Post, esto lo hacemos 2 veces, simplemente para tener 2 datos de prueba

![Terminal bash]( ./Images/Creacion%20de%20post%20phptinker.PNG "Creacion de Post")

#### Resultado

![Terminal bash]( ./Images/verposttinker.PNG "Ver los post creados")

### Configuracion de codigo para que funcione con base de datos
    Ahora nuestro programa en vez de funcionar con archivos, funciona con base de datos y por lo mismo hay que hacer unos pequeños cambios que basicamente consisten en cambiar $slug por $id

![Visual Studio Code]( ./Images/cambio%20por%20id%20routes.PNG "Cambio por $id")

![Visual Studio Code]( ./Images/cambio%20por%20id%20post.PNG "Cambio por $id")



## 21. Eloquent Updates and HTML Escaping
    En este modulo le damos un poco mas de formato a el HTML y tambien nos muestan los cuidados que hay que tener a la hora de "Escape" cierta informacion, para evitar errores, o problemas de seguridad
    
### formato extra para el HTML
    le agragamos el tag de <p> a el body para que la informacion que se muestra a continiacion no este pegado, en este caso el boton de volver a la pagina principal

![Terminal bash]( ./Images/Cambios%20en%20el%20body%20de%20post.PNG "Cambios en el body de post")

### HTML Escaping info
    Tambien se nos explica que hay que tener cuidado a la hora de hacer esto porque por ejemplo en el titulo se podria hacer esto, pero al hacer esto podemos causar un problema de seguridad ya que le damos la posibilidad de generar un error, por utilizar el mismo ejemplo meter codigo JS en el titulo, entonces cada vez que se cargue el post ejecutaria el JS, lo cual no es de nuestro interes

![Google Chrome]( ./Images/Escaping%20info%20title.PNG "Error al cargar el post")


## 22. 
## 23. 
## 24. 
## 25. 
## 26. 
## 27. 
## 28. 
## 29. 
## 30. 
 
