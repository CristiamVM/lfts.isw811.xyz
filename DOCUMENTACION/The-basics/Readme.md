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

## 08. How a Route Loads a View
## 09. How a Route Loads a View
## 10. How a Route Loads a View
## 11. How a Route Loads a View
## 02. Find a Composer Package for Post Metadata
## 13. Collection Sorting and Caching Refresher