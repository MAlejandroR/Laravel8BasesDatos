<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Bases de datos con Laravel
* Laravel permite tener un control absoluto sobre la estructura de la base de datos.
* Con esto me refiero a que a través del proyecto podemos sobre todas las tablas de nuestro proyecto 
 ** crear
 ** borrar
 ** modificar
 ** poblar 
* Para este cometido está el concepto de las **migraciones** en laravel que son ficheros php que contiene las instrucciones necesarias para realizar estas operaciones

* Ademas usaremos comando de artisan para agilizar el proceso de creación y ejecución de las migraciones
### Configurar la base de datos
*Para configurar la base de datos, hemos de especificar los siguientes parámetros:
 
<ol>
 <li>localhost</li>
 <li>usuario</li>
 <li>password</li>
 <li>base de datos</li>
</ol>

* Como todas las configuraciones, debemos ir al fichero de configuración de bases de datos

![Fichero de configuracion de base de datos](./documentacion/imagenes/config_base_datos.png)
  
Si vemos el contenido, vemos que es un array llamado **connections** el cual contiene tantas una serie de conexiones.

Podemos añadir más si necesitáramos, pero para este caso vamos a usar la ya conocida **mysql**

Si accedemos a ese elemento vemos su configuración:
<pre> 
'mysql' => [
        'driver' => 'mysql',
        'url' => env('DATABASE_URL'),
        'host' => env('DB_HOST', '127.0.0.1'),
        'port' => env('DB_PORT', '3306'),
        'database' => env('DB_DATABASE', 'forge'),
        'username' => env('DB_USERNAME', 'forge'),
        'password' => env('DB_PASSWORD', ''),
        'password' => env('DB_PASSWORD', ''),
    //.....
</pre>

Vamos como todos los parámetros, en lugar de asignarle directamente el valor, usamos la función **env**.

Esta función lo que hace es buscar el valor en el fichero *****.env*****, fichero ubicado en la carpeta raíz del proyecto
Si esta función localiza el parámetro que tiene como primer argumento en el fichero, retorna ese valor, si no, se retorna el valor que tiene como segundo argumento

El fichero *****.env***** es un fichero con información un tanto confidencial, por ser un fichero oculto, git no lo subirá al repositorio.

![Fichero .env](./documentacion/imagenes/fichero_env.png)

Por lo tanto es mejor asignar los valores en el fichero de configuración
<pre>
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel8basesdatos
DB_USERNAME=root
DB_PASSWORD=root
</pre>

Ahora debemos de crear la base de datos laravel8basedatos 

![Crear base de datos](./documentacion/imagenes/crear_base_datos.png)

### Instalar las migraciones
*Una vez creada la base datos vemos que está vacía

 ![Crear base de datos](./documentacion/imagenes/base_datos_vacia.png)

Ahora lo primero que debemos hacer es instalar las migraciones

 php artisan migrate:install




### Crear una migración para cada tabla

### Ejecutar una migración

### Modificar una migración y volver a ejecutarla para que se actualice en la tabla

### Borrar las tablas con las  migraciones

### Cómo poblar las tablas


### Interaccionar una tabla con una aplicación en laravel

#### Crear un modelo 

#### Crear un modelo con tabla, migración y preparada para ser poblada

#### Visualziar los datos


#### Concepto de resource: un CRUD


#### Guardar datos de un formulario en una tabla









que queramos inco





