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



## 22. 3 Ways to Mitigate Mass Assignment Vulnerabilities
    Nos enseñan 3 formas de migrar datos utilizando el php artisan tinker

Una de estas formas ya la conociamos, es como habiamos estado introduciendo datos hasta ahora

![Terminal bash]( ./Images/Creacion%20de%20post%20phptinker.PNG "Creacion de Post")

Otra formas es metiendo todo en una misma linea

![Terminal bash]( ./Images/Creacion%20de%20post%20phptinker.PNG "Creacion de Post")

Pero para esto es importante modificar nuesto modelo de Post

![Visual Studio Code]( ./Images/Post-22.PNG "Modificacion de Post")

Tambien podemos actualizar informacion

![Terminal bash]( ./Images/actulizar%20info%20m1.PNG "Actualizacion de Post")

Y con el siguiente comando lo volvemos a su estado original 

![Terminal bash]( ./Images/tinker%20fresh.PNG "volver al estado anterior")

O con un metodo mas directo con el cual podemos actualizar

![Terminal bash]( ./Images/actulizar%20info%20m2.PNG "Actualizacion de Post")




## 23. Route Model Binding
Nos enseñan a utilizar las wildcart de otra mananera y obtener un URL mas completo

### Migracion de la tabla Posts
    Para esto tenemos que agregarle un parametro a la tabla de posts para esto nos vamos a la carpeta de migracion y lo agregamos

![Visual Studio Code]( ./Images/modificacion%20de%20nuestra%20migracion-23.PNG "")

    Pero para que se guarde hay que aplicar la migracion, pero vamos a crear todo desde 0 con el parametro recien creado

    ```
    php artisan migration:fresh
    ```
![Visual Studio Code]( ./Images/migracion-fresh-23.PNG "Migracion de las tablas")

#### Resultado

![Workbench]( ./Images/Resultado%20de%20la%20migracion.PNG "Ver columnas creadas")

Y despues simplemente en nuestro archivo de rutas modificamos la funcion

![Visual Studio Code]( ./Images/routesconslug.PNG "modificacion de routes")

Tambien esta la posibilidad de hacerlo de la siguiente manera

#### archivo de rutas

![Visual Studio Code]( ./Images/routesconslugm2.PNG "Modificacion de")

#### Modelo Post

![Visual Studio Code]( ./Images/Postconslugm2.PNG "Modificacion de Modelo Post")

#### Resultado de ULR
![Visual Studio Code]( ./Images/URLconslug-23.PNG "Resultado de la pagina con Slug")



## 24. Your First Eloquent Relationship
    Asiganamos una categoria a cada post

### Creacion de las categorias
    Para crear las categorias primero tenemos que crear la tabla y Modelo de categorias, para esto utilizamos el artisan

![Terminal Bash]( ./Images/creacion%20Modelo%20y%20tabla%20category.PNG "Creacion de modelo y tabla categories")

#### Ahora creamos las categorias
  
![Visual Studio Code]( ./Images/creacion%20de%20categorias.PNG "Creacion de categorias")

#### Utilizando nuestro administrador de base de datos ahora podemos ver la relacion que estableciomos, obiviamente a la hora de crear los post nuevos hay que agregar una nueva columna que va a hacer una llave foranea que va a ser nuestra manera de establecer la conexion entra las tablas 

![Workbench 8]( ./Images/Prueba%20de%20categoria%2024.PNG "Prueba de relaciones")


### Creacion de funcion relacional
    Si probamos en el tinker la relacion

    ```
    $post->category 
    ```

    nuestra null, para arreglar esto vamos a ir a el Modelo Post 

![Visual Studio Code]( ./Images/funcionCategoryPost.PNG "Modificacion de Modelo Post")

### Testeo de Relaciones
    Con el php artisan tinker probamos nuestras relaciones

![Terminal Bash]( ./Images/ResultadophpArtisan%2024.PNG "Prueba de relaciones con el php artisan tinker")

### Modificacion de las paginas
    Modificamos la pagina principal como la pagina de cada post para que se muestre la categoria

![Visual Studio Code]( ./Images/posts-24.PNG "Modificacion de archivo posts")

![Visual Studio Code]( ./Images/post-24.PNG "Modificacion de archivo post")


#### Resultado final

![Google Chrome]( ./Images/pageposts%20con%20categoria.PNG "Resultado final")

![Google Chrome]( ./Images/pagepost%20con%20categoria.PNG "Resultado final")



## 25. Show All Posts Associated With a Category
    Ahora vamos a crear el la ruta para acceder a los post por categoria

### Creacion de ruta
    Primero en nuestro archivo de rutas vamos a crear el "path" hacia lo que ocupamos

![Visual Studio Code]( ./Images/nueva%20ruta%20para%20las%20categorias.PNG "Creacion de ruta para categorias")

### Creacion de funcion para cargar los post
    Ahora vamos a la funcion para que se cargen todos los post que pertenecen a una categoria

![Visual Studio Code]( ./Images/funcion%20para%20cargar%20todos%20los%20post%20de%20una%20categoria.PNG "Creacion de funcion para cargar post")

### Y Como ultimo le asignamos la ruta en la vista
    Le asignamos la ruta en la vista para que sea cargue la pagina que buscamoss

![Visual Studio Code]( ./Images/posts-25.PNG "Modificacion de php")

![Visual Studio Code]( ./Images/post-25.PNG "Modificacion de php")

### Resultado

![Google Chrome]( ./Images/Resultado%2025.PNG "Resultado")



## 26. Clockwork, and the N+1 Problem
    Basicamente nos explican que hay un problema con las solicitudes, y que que estan ejecutando varias querys de manera inecesarria

### Instalar clockwork
    Instalamos clockwork junto con su extencion para ver los querys solicitados

![Terminal Bash]( ./Images/install%20clockwork.PNG "Instalamos clockwork usando composer")

### Solucion
    Hacemos una pequeña modificacion en el archivo de rutas

![Visual Studio Code]( ./Images/modificacion%20de%20route%2026.PNG "Modificacion del archivo de rutas")

### Resultado
    Pasamos de tener 4 querys para cargar la vista a solo tener 2

![Visual Studio Code]( ./Images/Resultado%2026.PNG "Resultado")



## 27. Database Seeding Saves Time
    Nos enceñar a crear un seeder para no tener que estar creando datos de prueba cada vez que hacemos una migracion

### Modificacion de tabla posts
    Ocupamos agregarle una llave foranea a posts para que tenga una relacion con el usuario que se creo 

![Visual Studio Code]( ./Images/forranea%20para%20usuarios%2027.PNG "add llave foranea")
    

### Creacion del seeder
    Utilizamos el archivo seeder que esta por defecto en la carpeta de base de datos, aqui le vamos a meter todos los datos que queremos que el seeder cree

![Visual Studio Code]( ./Images/creacion%20del%20seeder%2027.PNG "Creacion de los datos en el seeder")

#### Ahora cada vez que migramos la base de datos le podemos agregar "--seed" para que ademas de remigrar las tablas ejecute el seeder y cree los datos por defecto

```
php artisan migrate::fresh --seed
```

### Modificacion de modelos

![Visual Studio Code]( ./Images/ModeloUser%2027.PNG "Modificacion de modelo")

![Visual Studio Code]( ./Images/ModeloPost%2027.PNG "Modificacion de modelo")

### Modificacion de vistas

![Visual Studio Code]( ./Images/post%2027.PNG "modificamos la vista")

![Visual Studio Code]( ./Images/posts%2027.PNG "modificamos la vista")



## 28. Turbo Boost With Factories
    Creacion de datos aleatorios

### Creacion de factories
Utilizando el artizan creamos los arvhivos de factory

![Terminal Bash]( ./Images/creacion%20de%20factorys%2028.PNG "Creacion de los archivos Factory")


### Asignacion de datos a los factories

![Visual Studio Code]( ./Images/factoryPost%2028.PNG "Agregamos los datos que queremos crear")

![Visual Studio Code]( ./Images/factoryCategory%2028.PNG "Agregamos los datos que queremos crear")

### Modificacion del Seeder
    Ahora los datos del seeder se pueden fabricar de manera aleatoria y cuantos nosotros queramos, en este caso vamos a crear 5 posts, que todos provengan del mismo usuario

![Visual Studio Code]( ./Images/seeder%2028.PNG "modificamos la vista")

#### Resultado

![Google Chrome]( ./Images/seeder%2028.PNG "Resultado")

## 29. 
## 30. 
 
