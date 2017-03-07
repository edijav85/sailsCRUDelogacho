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
  * RUTA
   -La ruta es el URL al cual el usuario va a ser dirigido cuando sailsjs recepte su petición (request), para esto necesitamos definir dos cosas:

      + Ruta en string: Una ruta es el URL a donde va a dirigir la petición el navegador o agente como por ejemplo: "/Usuario/CrearUsuario"

      + Método HTTP: El método HTTP también puede ser definido dentro de las rutas, por default el método es "get", también podemos elegir entre los métodos post put delete siendo put y get los más usados en las rutas.

  * La acción del controlador o la vista
  Después de definir la ruta y el método http con el cuál el agente se va a comunicar con el servidor, necesitamos definir la acción o la vista que vamos a usar.

  La vista puede ser cualquiera de las vistas dentro de nuestra carpeta "views"

  Las acciones en cambió son los controladores dentro de nuestra aplicación, sean estos métodos dentro de los controladores del módelo o de un controlador aparte.


### Modelos (routes.js)
Los modelos son donde los datos dentro de una aplicación de sailsjs se guardan. Estos representan a Bases de Datos Relacionales como No Relacionales ya que sailsjs utiliza un ORM llamado WATERLINE el cuál puede conectarse a bases de datos como mysql postgresql oracle y tambien a bases de datos no relacionales como mongodb y redis.

### Controladores
Los controladores dentro de Sailsjs tienen como finalidad brindar los métodos CRUD de nuestros modelos, así también como exponer la lógica de negocio que se defina en la aplicación, como por ejemplo la autenticación.


### DOCUMENTACIÓN
Dentro de la DOCUMENTACIÓN de Sailsjs tenemos los siguientes conceptos:
  * ATTRIBUTES - Atributos.- Los atributos son información acerca de un modelo en sailsjs. Los atributos tienen un nombre y también validaciones
  * ASSOCIATIONS - Relaciones.- Con el ORM se pueden establecer varios tipos de relaciones
  * QUERY LANGUAGE - Lenguaje de Consulta.- El lenguaje de consulta en sailsjs es usado para utilizar operadores de las bases de datos como count por ejemplo desde nuestro ORM Waterline
  * MODEL SETTINGS - Configuración de los modelos.- tenemos los siguientes
    - Models.js ( Conexión General)
      + La primera es la "connection" donde pondremos el nombre de las conexiones disponibles en el archivo "connections.js".
      + El segundo es "schema" con valores de true o false lo que hace que nuestras tablas en la base de datos sean tratadas como bases de datos relacionales o bases de datos no relacionales (es decir poder agregar mas atributos que no esten definidos, o no)
   - Connection.js ( Conexión General)
          + En este archivo definimos todas las conexiones para nuestro orm, sean a postgresql, mysql, sqlserver, mongodb, redis, oracle y ¡otras más!. Para definir la cadena necesitamos datos como HOST o IP, Puerto, Nombre de Usuario, Nombre de la base, etc.
    - Conexión por Modelo (en cada uno de los archivos de las tablas)
    Por ultimo tenemos varias tipos de configuraciones para cada una de nuestras tablas que serían las siguientes:

      * identity
      * globalId
      * autoPK
      * autoCreatedAt
      * autoUpdatedAt
      * tableName      
