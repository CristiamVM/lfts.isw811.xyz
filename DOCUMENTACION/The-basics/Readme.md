# LFTS - The Basis

## 05. How a Route Loads a View

### Como funcionan las rutas
    En la primera parte nos muesta como fuciona las rutas y nos muestra donde esta la pagina por default de laravel, en esta pagina y a modo de demostracion cambiamos un poco esta pagina encerrando uno de los textos en una etiquetas "strong" y vemos como cambia en la pagina

![Visual Studio Code]( ./images/strong%20en%20el%20default.PNG "agregamos etiqueta <strong>")
![Google Chrome]( ./Images/strong%20en%20el%20default%20page.PNG "Resultado de la modificacion")

    Aparte de vistas en las rutas podemos imprimir texto plano

![Visual Studio Code]( ./images/helloworldVS.PNG "modificamos la ruta")
![Google Chrome]( ./Images/helloworldPage.PNG "Resultado de la modificacion")

    Aparte podemos incluso retornar Json

![Visual Studio Code]( ./images/JsonVS.PNG "modificamos la ruta")
![Google Chrome]( ./Images/JsonPage.PNG "Resultado de la modificacion")


## 06. Include CSS and JavaScript
    Empezamos modificando por completo la pagina por defecto de laravel y introduciomos el siguiente codigo

![Visual Studio Code]( ./images/Codigodummy6.PNG "Modificacion de la pagina default")

    Y obiamente el resultado va a ser el siguiente

![Google Chrome]( ./Images/Codigodummy6Resultado.PNG "Resultado de la modificacion")

### Implementacion CSS
    Vamos a la public y creamos una carpeta que se va a llamar "app.css" y le metemos una modificaciones para la pagina

![Visual Studio Code]( ./images/app.css.png "Modificacion de la pagina default")

    Y obiamente el resultado va a ser el siguiente

![Google Chrome](./Images/app.cssPage.png "Resultado de la modificacion")

    creamos un archivo JS que como resultado da lo siguiente

![Google Chrome]( ./Images/resultadoJS6.PNG "Resultado de la modificacion")


## 07. Make a Route and Link to it
    Modificamos el nombre del archivo por defecto para que pase de "Welcome" a "posts" y le agregamos unas pequeñas modificaciones al la pagina que veniamos creando, tambien modificamos el CCS para que sea un texto decente de utilizar
    
![Visual Studio Code]( ./images/modificacion%20del%20nombre%20posts.PNG "Modificacion de el nombre de la paginar por defecto")
![Visual Studio Code]( ./images/modificaciondelposts.PNG "Modificacion de la pagina posts")

    Ahora vamos a crear un nuevo archivo que se va a llamar "post" para la ruta que vamos a crear y la cual la va a redirigir los titulos de los post que creamos en posts

![Visual Studio Code]( ./images/rutapost.PNG "Creacion de la ruta post")
![Google Chrome]( ./images/paginapost.PNG "Resultado final de post")


## 08. Store Blog Posts as HTML Files
    Ahora basicamente ocupamos que los post que estamos creando sean dinamicos y no tenga problemas para eso podemos asigarle una variable a post en vez del texto quemado, pero ocupamos configurar la rutas para esto


### creacion de la variable en post
Vamos a crear una ruta dinamica para cada post

![Visual Studio Code]( ./images/variablepost.PNG "Creacion de la variable post")

### configuracion de la ruta dinamica
    Al crear el codigo necesario para tener acesso de manera dinamica a los archivo tambien vamos a crear un control de errores, com se muestra en el codigo a continuacion
![Visual Studio Code]( ./images/configuracion%20de%20ruta%20dinamina.PNG "Creacion de la ruta post")

### creacion de los archivos
    Para estos archivos vamos a crearlos en la carpetas de resources, creamos una carpeta posts y alli metemos  los archivos HTML de los post

![Visual Studio Code]( ./images/HTMLpost.PNG "Creacion de la ruta post")

### Resultado
    Ahora podemos acceder a cada uno de los archivos post de una manera un poco mas dinamica

![Google Chrome]( ./images/resultado8.PNG "Resultado")


## 09. Route Wildcard Constraints
    En este episodio del curso basicamente le agregamos un poco de seguridad a la ruta del wildcart para que solo accepte un grupo que nosotros asignamos atravez de regular expressions

![Visual Studio Code]( ./images/regularexpressionswildcart.PNG "Creacion de la expresion regular")

## 10. How a Route Loads a View
## 11. How a Route Loads a View
## 02. Find a Composer Package for Post Metadata
## 13. Collection Sorting and Caching Refresher