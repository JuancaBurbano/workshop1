# Readme sobre Workshop1 

## Introducción

Para este proyecto se utilizo una fuente de datos proporcionada por el docente donde el contexto de esta, era un csv de canditatos con diferentes tipos de informaciones. Este csv se utilizo para todo el trabajo, donde se tenia que hacer una coneccion a un gestor de base de datos mediante el lenguaje de programacion python. Esto tambien implicaria crear una base de datos y una tabla para almacenar la informacion de la fuente de datos.
A esot no se le hizo un proceso de limpieza puesto que iniciando se pudo envidenciar qeu la fuente de datos ya estaba lista.

El estado de este proyecto esta finalizado, ya se realizaron todos los puntos que se pedian, mediante un notebook de jupyter, y una visualisacion en POWER Bi.

## Contenido del proyecto

Este proyecto contiene 3 archivos en si, muy sencillos cada uno para la facil elavoracion y llevada a cabo del proyecto. 
1. Workshop.ypynb: Un cuaderno de jupyter en el cual se hace todo el proceso para la coneccion al gestor de bases de datos, la creacion de la base y de las tablas como tal, asi como la inyeccion de los datos a estas tablas. (tablas en general porque más adelante se mostrara un proceso que involucra crear una nueva tabla)
2. candidates.csv: Este archivo es nuestra fuente de datos, un tipo CSV, donde almacena todos nuestros datos ceparados por (Comas).
3. credentials.json : Este es un archivo que ustedes mismos a la hora de correr el codigo debe gestionar, puesto que por razones se seguridad no puedo proporcionales mis credenciales para acceder a la base de datos, y ocurriria un error puesto qeu no son las mismas credenciales con su base de datos, mas adelante se les mostrara el proceso para que puedan correr esto sin ningun problema.

Como un plus al momento de insertar los datos a las tablas se creara un nuevo archivo llamado candidates2.csv, que contiene la información para lla segunda tabla.

## Instalación y configuración

Los comandos para poder descargar este proyecto son los basicos...

- Creas una carpeta donde almacenaras el proyecto
- Abrela con tu (gestor de codigo) favorito en este caso Usaremos Visual Studio Code
- Crea una nueva terminal
- Haz un git commit (link)

Y listo ya tienes el proyecto, ahora debes correrlo, para que esto pase sin ninugn problema esto es lo que debes hacer...

Lo primero que debes hacer es ir al cuaderno workshop.ipynb el cual contiene la información necesaria par aque funciones. este notebook esta explicado paso por paso en cada celda el como se debe aplicar el codigo, de igual manera en este readme tambien te proporcionare esta información. 

- Instala las librerias: La primera celda que nos sale en el readme es sobre las librerias que vamos a usar en este proyecto. (Debes correr esta celda)
- Crea tu archivo credentials.json: Tal cual el nombre desdes crear este archivo "credentials.json", este tendra la siguiente información...
```
{
    "host" : "localhost",
    "user" : "",
    "password" : "",
    "database" : ""  
}

```

Rellena la información del json con la tuya, pero aun no coloques nada en databes, pues aun no la hemos creado.

- Este proyecto tiene como gestor de bases de datos, MySQL, entonces si aunn no lo tienes, descargalo y haz el proceso de instalación, puedes descargarlo mediante el siguiente link: (https://dev.mysql.com/downloads/installer/)


Continuando, ya teniendo el gestor de base de datos vamos a proceder a la conexón. La siguiente celda de codigo, nos hace la coneccion trayendo el json que tenemos como credentials para usar esas "credenciales" al momento de hacer la conexión.
(Corre la celda)

- Ya que tenemos la coneccion al gestor, vamos a crear la base de datos con la que trabajaremos y la tabla principal, para correr esta celda de codigo no debes configurar nada, solo correrla, quedarias con una base de datos llamada workshopdb1 y con la tabla candidatos, con las columnas correspondientes.
(Corre la celda)

- Despues del paso anteriror y de haber creado la base de datos, ahora si la podemos configurar en credentials.json..

```
{
    "host" : "localhost",
    "user" : "",
    "password" : "",
    "database" : "workshopdb1"  
}

```
Asi deberia quedarte el json, claramente en user y en password, tus credenciales, despues de haber configurado de nuevo el json, guardalo y ve al cuaderno, ya puedes correr la siguiente celda sin problema.
(Corre la celda)

- Ya tenemos la coneccion al gestor, ya tenemos creada la base de datos, y ya tenemos la tabla con datos, procederemos a hacer un EDA a esta tabla que nos quedo, para las siguientes celdas de EDA no debes hacer ninguna configuración, solamente corres la celdas y puedes ver las conclusiones a las que se llego haciendo el Analisis Exploratorio de Datos.

- Creación de la nueva tabla: Despues de haber terminado el EDA se nos solicita que creemos una nueva tabla donde los candidatos que en las columnas TechnicalviewScore y CodeChallengeScore sean mayores que 7, se creara una nueva colomna en esta nueva tabla que apruebe al candidato en numeros binarios 0 y 1. Donde 1 quiere decir que si aplico y 0 es que no. Entonces corremos sin ningun problema las celdas que nos verifican los candidatos con estos resultaods.
(Corre la celda)

- Añadimos la tabla: Hacemos el mismo proceso que al momento de crear la primera tabla, se hace automatico con el .cursor asi que solo debes correr la celda para que se cree esta nueva tabla en la base de datos.
(Corre la celda)

- Creaccion de candidates2.csv: Importamos este nuevo dataframe que quedo con la nueva columna a un csv que posteriormente cargaremos a la nueva tabla.
(Corre la celda)

- Importamos los datos: La ultima celda que nos queda es la importación de los datos a nuestra nueva tabla, pues como al principio importamos el csv candidates a la tabla, relizamos el mismo proceso paara la segunda tabla, solo debes correr la celda que ya el proceso se hace automatico.
(Corre la celda)

## Pruebas de funcionamiento
En el anterior punto mostramos el paso a paso de como se corre este proyecto, en este se mostraran las pruebas y outputs que se realizan al momento de correr el proyecto.

Disponibles las muestras graficas en el siguiente documento o tambien en el informe: (https://docs.google.com/document/d/1uYlP_68EkMxUuMG5akHnbwSeNw25LtWMjek6rTcp234/edit?usp=sharing)
 
## Muestras de power BI

## Conclusiones

## Agradecimientos