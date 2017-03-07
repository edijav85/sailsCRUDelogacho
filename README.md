# DEBER DE TECNOLOGÍAS WEB CON JAVASCRIPT
-------------------------------------------
###Materia: Tecnologias Web con Java Script
###Tema: Sailsjs CRUD Raza y Edicion Mascotas Tarea
###Fecha: 02/02/2016
###Profesor:TANIA CALLE Y ADRIAN EGUEZ

#INDICE DE CONTENIDOS
-------------------------------------------
- <a href="#tema">Tema</a>
- <a href="#objetivos">Objetivos</a>
- <a href="#marco-teorico">Sailsjs CRUD Raza y Edicion Mascotas Tarea</a>
- <a href="#desarrollo">Desarrollo de la Práctica</a>
- <a href="#conrec">Conclusiones y Recomendaciones</a>

<a name="tema"></a>
## Tema
Sailsjs CRUD Raza y Edicion Mascotas Tarea

<a name="objetivos"></a>
## Objetivos

- Continuar con la creacion de vistas y modelos para cumplir con el CRUD de Mascotas
- Establecer caracteristicas de las vistas para una presentacion final del proyecto

<a name="marco-teorico"></a>
## Marco Teorico
### Views
Las vistas son las páginas que se va a mostrar al usuario dependiendo de la lógica que tenga nuestra aplicación de sailsjs.

El View Engine es el que permite usar archivos o  templates estáticos en la aplicación. En runtime, este template reemplaza las variables con los valores que son inyectados desde los controladores y transforma el template a un archivo html que se lo envía al cliente.

Existen algunos Template Engines en el mercado como por ejemplo los siguientes:

  - EJS
  - PUG
  - Mustache
  - JADE    

### EJS
Sailsjs utiliza por default EJS el cual utiliza una síntaxis parecida a esto: <% %> . Dentro de estos tags podemos usar codigo javascript dentro de nuestra aplicación, para repetir código con un "for" por ejemplo. Tambíen EJS permite insertar el valor de las variables con el siguiente tag: <%= numeroEntero %> , en donde número entero es una variable JavaScript dentro de la vista.

### Rutas (routes.js)
Dentro de la carpeta de configuración de sailsjs tenemos un archivo llamado "routes.js" este archivo nos permite a nosotros delimitar 2 cosas básicamente.
  + RUTA

    ..La ruta es el URL al cual el usuario va a ser dirigido cuando sailsjs recepte su petición (request), para esto necesitamos definir dos cosas:

          -- Ruta en string: Una ruta es el URL a donde va a dirigir la petición el navegador o agente como por ejemplo: "/Usuario/CrearUsuario"

          -- Método HTTP: El método HTTP también puede ser definido dentro de las rutas, por default el método es "get", también podemos elegir entre los métodos post put delete siendo put y get los más usados en las rutas.


### Rutas
Las rutas son a donde vamos a direccionar nuestro trafico dependiendo los métodos HTTP y el URL de nuestros recursos.
Link Documentación Oficial: Routes


### Controladores
Los controladores dentro de Sailsjs tienen como finalidad brindar los métodos CRUD de nuestros modelos, así también como exponer la lógica de negocio que se defina en la aplicación, como por ejemplo la autenticación.


### Pipeline
En el archivo pipeline.js dentro de la carpeta task se encuentran las diferentes configuraciones de GRUNT que es un automatizador de actividades con JavaScript. Dentro de este podemos configurar los assets que van a ser inyectados en TODAS las vistas de nuestra aplicación en Sailsjs.

###<a name="#desarrollo">PRACTICA</a>
