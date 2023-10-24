# LFTS - Filtering


## 39. Advanced Eloquent Query Constraints
    En este capitulo nos enseñan otra manera de hacer el filtrado de categorias de una manera mas directa y limpia utilizando las propiedades que nos brinda "Eloquent"

![Visual Studio Code](./images/PostController%2039.PNG "Modificacion de Controlador")

![Visual Studio Code](./images/posts-header%2039.PNG "Modificacion de vista")

![Visual Studio Code](./images/Post%2039.PNG "Modificacion de Modelo post")


#### Al hacer la busqueda por categorias de esta menera nos ahorramos bastante codigo ya que ya no ocupamos la ruta que nos llevaba a la vista de la categoria que estabamos buscando

![Visual Studio Code](./images/routes%2039.PNG "Modificacion del archivo de rutas")



## 40. Extract a Category Dropdown Blade Component
    Ahora vamos a cambiar el dropdown de categorias para que utilice blade

![Visual Studio Code](./images/PostController%2040.PNG "Modificacion del controlador de post")

![Visual Studio Code](./images/categorydropdown%2040.PNG "Creacion de controlador para el dropdown de category")

![Visual Studio Code](./images/categorydropdown.blade%2040.PNG "Creacion de del arvhivo con formato blade para el dropdown de")


![Visual Studio Code](./images/routes%2040.PNG "Modificacion del archivo de rutas")


![Visual Studio Code](./images/index%2040.PNG "Ajuste de dependencias para que concuerde con los cambios de nombre")


![Visual Studio Code](./images/header%2040.PNG "Cambio a formato blade")


#### Tambien le cambiamos el nombre a los ciertos archivos por mero orden y los metemos en una carpeta que vamos a llamar posts
_posts-header.blade.php → _header.blade.php

posts.blade.php → index.blade.php

post.blade.php → show.blade.php

![Visual Studio Code](./images/posts%2040.PNG "Modificacion del controlador de post")



## 41. Author Filtering
 En este episodio como indica el titulo vamos a hacer la filtracion por autor, asi cada vez que clickeamos en el nombre de un autor vamos a ser capaces de ver todos los posts que tiene ese autor

![Visual Studio Code](./images/PostController%2041.PNG "Modificacion del controlador de post")

![Visual Studio Code](./images/post-model%2041.PNG "Modificacion del Modelo de post")

![Visual Studio Code](./images/post-card%2041.PNG "Modificacion de la vista post-card")

![Visual Studio Code](./images/post-featured%2041.PNG "Modificacion de la vista post-card")

![Visual Studio Code](./images/show%2041.PNG "Modificacion de la vista post especificos")


#### Con los cambios que hemos venido haciendo, ya no es necesario usar las rutas para los filtros que hemos venido modificando(categoria, autor) ahora todos lo hacemos desde el controlador y el modelo de los post utilizando querys

![Visual Studio Code](./images/routes%2041.PNG "Modificacion del controlador de post")



## 42.
## 43.