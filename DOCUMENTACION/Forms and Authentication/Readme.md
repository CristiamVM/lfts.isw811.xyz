# LFTS - Forms and Authentication

## 45. Build a Register User Page
    Como indica el titulo vamo a crear un registro para usuarios y que estos se guarden en la base de datos

![Visual Studio Code](./images/route%2045.PNG "Modificacion de Usuarios")

![Visual Studio Code](./images/create%2045.PNG "Creacion de vista para el form de registro de usaurios")

![Visual Studio Code](./images/user-model%2045.PNG "Modificacion del modelo de usuarios")

![Visual Studio Code](./images/register-control%2045.PNG "Creacion de Controlador para los usuarios que vamos a registrar")



## 46. Automatic Password Hashing With Mutators
    En este episodio nos enseñan a crear contraseñas encriptadas de forma automatica

![Visual Studio Code](./images/user-model%2046.PNG "Otra forma de hacer la encriptacions desde el Controlador para los usuarios") 

![Visual Studio Code](./images/register-control%2046.PNG "Modificacion del modelo de usuarios")



## 47. Failed Validation and Old Input Data
    En este episodio haces un poco de control de errores y validaciones

![Visual Studio Code](./images/create%2047.PNG "Modificacion del formulario de registro para que muestre los errores") 

![Visual Studio Code](./images/register-control%2047.PNG "Modificacion del controlador del registro para agregar validaciones")



## 48. Show a Success Flash Message
    Ahora vamos a crear un mensage que valide que nuestro usuario fue creado correctamente, obviamente nosotros en este momento tenemos que imnediatamente depues de que el usuario sea registrado pase a la pagina principal, y eso a nosotros nos sirve como validacion, pero al usuario claramente no, aparte dudo que este sea el estado final, falta el login

![Visual Studio Code](./images/register-control%2048.PNG "Modificacion del controlador del registro") 

![Visual Studio Code](./images/flash%2048.PNG "Creacion de el mensaje flash que se va a mostrar")

![Visual Studio Code](./images/layout%2048.PNG "Modificacion del layout principal para que se muestre el mensaje flash")


## 49.Login and Logout
    En este episodio creamos la logica para logear y desloguear de nuestra pagina

![Visual Studio Code](./images/route%2049.PNG "Modificacion del archivo de rutas `para crear las rutas de registro y cerrar session")

![Visual Studio Code](./images/layout%2049.PNG "Modificacion del layout principal para que se muestre el nombre del usuario que logueo y el boton para cerrar session")

![Visual Studio Code](./images/session-control%2049.PNG "Creacion del controlador de sessiones")

![Visual Studio Code](./images/register-control%2049.PNG "Modificacion del controlador de registros")




## 50. Build the Log In Page
    En este episodio vamos a crear todo lo que nos falta para iniciar sesion, esto obviamente seria una vista para el login y la validacion de credenciales 

![Visual Studio Code](./images/route%2050.PNGodificacion del controlador de registros")

![Visual Studio Code](./images/create-sesion%2050.PNG "Creacion de la pagina de login")

![Visual Studio Code](./images/session-control%2050.PNG "Modificacion del controlador de sesiones")

![Visual Studio Code](./images/route%2050.PNG "Modificacion del archivo de rutas")


## 51. Laravel Breeze Quick Peek
    Para este capitulo hay crear un nuevo proyecto y para conveniencia personal voy a utilizar uno de los sitios que creamos al princio del curso para evitar crear otro vhost y demas pasos

![Visual Studio Code](./images/session-control%2051.PNG "Modificacion del controlador de sesiones")


### proyecto nuevo
para esto vamos a usar el host virtual que habiamos creados en la primera clase llamado "crisitiam.isw811.xyz" y le vamos a meter laravel

![Google Chrome](./images/defaultlaravel%2051.PNG "Prueba de instalacion de laravel")

#### ahora vamos con laravel breeze

```
    composer require laravel/breeze --dev
    php artisan breeze:install
    npm install
    npm run dev
```

![Google Chrome](./images/laravel%20breeze%2051.PNG "Prueba de instalacion de laravel")