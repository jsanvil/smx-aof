---
title: Introducció a les bases de dades
weight: 11
pre: "<b>11. </b>"
---
	
### Introducció a les bases de dades

# 1. Bases de datos

La gran cantidad de información que manejamos en la actualidad, requiere de cierta organización que conlleva la necesidad de elementos que:

Almacenen la información de forma organizada
Permitan localizar los datos de manera rápida y sencilla
Ordenen la información basándose en criterios
Realicen cálculos con los datos numéricos
Por todo ello, podemos definir una base de datos como un conjunto de datos que están organizados para un uso determinado o, también, como un conjunto de herramientas que permiten gestionar información relacionada de un tema determinado.

## 1.1. Ejemplo: agenda organizada
Si nos fijamos en el concepto de organización podemos encontrar un ejemplo bastante claro en la diferencia existente entre un montón de números de teléfono y direcciones escritos en trozos de papel (lo que conocemos como post-it) o tenerlos organizados en una agenda. En ambos casos tenemos la misma información, pero mientras que en el primero encontrar un número de teléfono puede llevarnos bastante tiempo, en el segundo caso, el trabajo se puede reducir a unos pocos segundos. La diferencia se encuentra en la forma en que la información está almacenada y organizada.



# 2. Aplicación práctica de las bases de datos. Usos
Las bases de datos son un elemento fundamental que ofrecen multitud de ventajas a la hora de organizar y almacenar datos. Entre los usos más habituales que suelen tener se encuentran:

Banca: información de clientes, cuentas, transacciones, préstamos, etc.
Transporte: información de clientes, horarios, destinos, incidencias, tráfico en tiempo real, sistemas GPS, etc.
Educación: información de estudiantes, cursos, materias (asignaturas), horarios, etc.
Fuerzas y cuerpos de seguridad del Estado: antecedentes penales, infracciones, datos personales, DNI electrónico, etc.
Sanidad: datos de pacientes, historiales médicos, datos de centros hospitalarios, datos de pruebas médicas, etc.
Información personal: redes sociales, directorios telefónicos, callejero electrónico, agenda de contactos, etc.
Telecomunicaciones: información de llamadas, gastos, saldos, consumos, etc.
Internet: portales y plataformas, blogs, correo electrónico, enciclopedias digitales, diccionarios, traductores, bibliotecas virtuales, etc.

# 3. Sistemas gestores de bases de datos (SGBD)

Anteriormente explicábamos que las bases de datos permiten, entre otras cosas, organizar los contenidos de forma que sean fácilmente localizables. Para poder utilizar las bases de datos necesitamos de un soporte que permita introducir, organizar y recuperar la información de éstas, en deﬁnitiva, administrarlas, llamado sistema gestor de base de datos (SGBD). Dicho de otro modo, un SGBD es un programa informático que gestiona una base de datos.

Existen muchos tipos distintos de gestores de bases de datos, aunque casi todos los sistemas modernos almacenan y tratan la información utilizando el modelo de gestión de bases de datos relacional. En este sistema, los datos se organizan en tablas, las cuales se encuentran relacionadas de alguna forma entre ellas. Dichas tablas almacenan información sobre un tema, como pueden ser los usuarios de una red social, los clientes de una empresa, los pedidos realizados por cada uno de ellos o los libros de una biblioteca.

LibreOffice_Base es un sistema gestor de bases de datos relacionales (SGBDR) que permite almacenar y recuperar la información en las tablas de una base de datos, de acuerdo con las relaciones que se hayan establecido. Además de ser libre, ofrece distintas versiones que permiten adaptarse a los diferentes sistemas operativos existentes.

 	 
Contenidos	
Contenidos
 	
# 4. Elementos

Prácticamente, en cualquier base de datos actual, existen cuatro elementos esenciales: tablas, consultas, formularios e informes. Todos son indispensables y necesarios. Esta es una definición muy básica de cada uno de los elementos que forman parte de una base de datos pero suficiente para comenzar a familiarizarnos con estos conceptos:

Elemento	Función
Tablas	Permiten almacenar los datos.
Consultas	Con las consultas podemos acceder a los datos almacenados, ordenarlos y filtrarlos por diferentes criterios.
Formularios	Facilitan las tareas de introducción de datos en las tablas, de forma que sean más intuitivas y sencillas para el ser humano.
Informes	Representan la forma más eficaz de presentar nuestros datos, tanto por pantalla como por impresora.

## 4.1. Tablas

Dentro de una base de datos, la información se almacena y se organiza en tablas, habiendo en cada una de ellas una o varias series de filas y columnas. A las filas se les denomina registros, a las columnas, campos, y a la intersección de un registro con un campo se le llama dato. La estructura es similar a una hoja de cálculo, aunque el funcionamiento y la nomenclatura difieren.

Nombre en hoja de cálculo	Nombre en base de datos
Fila	Registro
Columna	Campo
Celda	Datos
En la imagen se muestran ejemplos de los conceptos explicados:

## 4.2. Consultas

Las consultas tienen como propósito recuperar la información almacenada en las tablas, es decir, permiten ver un conjunto de datos de una tabla a partir de una petición o pregunta que realicemos.

Ejemplo de consulta del catálogo de libros disponible en una biblioteca, en orden alfabético:

## 4.3. Formularios

Los formularios nos ayudarán principalmente en tareas de introducción, modificación y borrado de información, ya que muestran los datos de modo diferente al de una tabla, de manera más vistosa y agradable. Cuando se trata de incluir pocos datos podemos hacerlo directamente sobre las tablas pero cuando el volumen es importante, este método se vuelve poco eficaz. Para resolver este problema tenemos los formularios donde la inclusión de datos se hace de forma mucho más intuitiva y sencilla.

Ejemplo de formulario que podría ser utilizado para la gestión de música de una discoteca:

## 4.4. Informes

Los informes tienen como objetivo proporcionar las herramientas necesarias para obtener una copia por pantalla o impresa de los datos existentes en una base de datos. Habitualmente, los informes se suelen construir a partir de los resultados obtenidos de la ejecución de consultas, lo que combina la posibilidad de seleccionar sólo los datos que queremos que nos ofrezcan las consultas con la ventaja de imprimirlos, tanto por pantalla como en papel. Éstos pueden ser configurados con diferentes estilos de modo que se puedan adaptar a los distintos usuarios y circunstancias en las que sean requeridos.

Ejemplo de informe del catálogo de libros de una biblioteca:

## 4.5. Ejemplo práctico: centro educativo

A continuación vamos a ilustrar con un ejemplo los elementos de las bases de datos con el fin de que queden claros todos los conceptos estudiados. Para ello vamos a utilizar la base de datos de un centro educativo:

Tablas: profesores, alumnos, matrículas, asignaturas, grupos, cursos, etc.
Consultas: asignaturas que tiene cada alumno, alumnos de cada grupo, grupos de cada curso, etc.
Formularios: alumnos, profesores, asignaturas por alumno, grupos de cada curso, etc.
Informes: profesores por grupo, alumnos matriculados, asignaturas impartidas, porcentaje de aprobados, etc.
Como se puede observar, cada tabla almacenará información de cada elemento del instituto, cada consulta permitirá obtener datos que podrán ser utilizados en informes, y cada formulario permitirá introducir y modificar, de forma sencilla e intuitiva, la información de una o varias tablas.

Ejercicios	
Ejercicio
 	
Cuestionario

Contesta a las preguntas del cuestionario.
 	 
Contenidos	
Contenidos
 	
# 5. Introducción a LibreOffice Base
LibreOffice_Base es un programa de bases de datos que gestiona la creación y manejo de éstas, además de posibilitar la elaboración de formularios e informes que proporcionan a los usuarios un acceso fácil a los datos. Su interfaz es sencilla, lo que permite gestionar las bases de datos de igual manera que aplicaciones de características similares.

Base proporciona varias características interesantes tales como: la habilidad de analizar y editar relaciones a partir de la vista de un diagrama, la incorporación de HSQLDB como su motor de bases de datos relacional por defecto, la posibilidad de utilización de otras bases de datos en formatos como dBASE, MYSQL, etc., o cualquier base de datos compatible con ODBC o JDBC.

Además de las características anteriores, Base incluye, al igual que las demás aplicaciones de la suite LibreOffice, multitud de asistentes y vistas para hacer el trabajo más fácil a los usuarios poco acostumbrados a este tipo de programas.

 	 
Ejercicios	
Ejercicio
 	
Crear acceso directo

Ve al menú de Lliurex (parte inferior izquierda de la pantalla) Aplicaciones → Oficina → LibreOffice Base y manteniendo presionado el botón izquierdo del ratón, arrastra la opción de menú al escritorio. Acabamos de crear un acceso directo en el escritorio de Lliurex.


 	 
Contenidos	
Contenidos
 	
# 6. Operaciones con bases de datos
Los sistemas gestores de bases de datos permiten realizar un conjunto de acciones sobre las bases de datos:

Abrir una base de datos para gestionarla
Crear una nueva base de datos para rellenarla
Cerrar una base de datos ya abierta
El SGBD Base ofrece las operaciones mencionadas, aunque previamente debemos abrirlo. Existen diferentes formas dependiendo de la configuración del sistema operativo, si bien principalmente se puede arrancar de dos distintas:

Haciendo doble clic sobre un acceso directo ubicado en el escritorio
Accediendo al menú de LibreOffice y pulsando sobre LibreOffice Base
Una vez abierto podemos observar el asistente para bases de datos en el cual se muestran diferentes opciones, tanto para crear una base de datos como para abrir/conectarse a una ya existente.

## 6.1. Creación de una base de datos

### 6.1.1. Paso 1

Para crear una nueva, selecionamos la primera opción Crear nueva base de datos.

### 6.1.2. Paso 2
Después, hacemos clic en el botón Siguiente, lo que nos llevará a otra pantalla con dos opciones (que debemos dejar con los valores por defecto).

Las opciones son las siguientes:

Registrar la base de datos. Sirve para indicar a LibreOffice dónde localizar los datos y cómo se organizan. Es decir, debemos registrar nuestra base de datos si queremos que la información que guardemos sea localizable desde otras aplicaciones. Por ejemplo, si en el procesador de textos Writer queremos mostrar una tabla con datos guardados en nuestra base de datos, debemos registrarla antes.
Abrir la base de datos para editarla. Es obligatorio tenerla marcada porque, si no, después de crear la base de datos se cerraría Base.

Pulsando el botón Finalizar se abrirá un cuadro de diálogo donde debemos indicar la carpeta en la que se almacenará la base de datos así como el nombre con el que se guardará. Para terminar la creación pulsamos el botón Guardar y se abrirá la pantalla principal.

## 6.2. Apertura de una base de datos
Para abrir una base de datos existente selecionaremos la primera opción Abrir un archivo de base de datos existente. Si hemos estado trabajado recientemente con el archivo, podemos seleccionarlo en el desplegable ubicado debajo de la opción anterior.



En caso contrario pulsaremos el botón Abrir y se abrirá un dialogo donde podemos seleccionar la ruta de la base de datos (fichero con extensión .ODB).

 	 
Ejercicios	
Ejercicio
 	
Carpeta de trabajo

Ve a tu carpeta personal de documentos.
Crea una nueva carpeta llamada “BASE”.
Crear una base de datos: Biblioteca

Vamos a crear una base de datos vacía que utilizaremos en las siguientes prácticas. Al final de todas esas prácticas la subiremos al portal.

Ve a tu carpeta personal de documentos.
Crea una nueva base de datos vacía con las opciones por defecto: que se abra para editarla al finalizar la creación y que quede registrada. 
Guarda la base de datos en la carpeta "BASE" con el nombre "biblioteca".


Contenidos	
Contenidos
 	
# 7. Pantalla principal
Una vez dentro del programa, nos aparecerá una ventana con el aspecto de la figura siguiente (puede ser que lo que vemos en el ordenador no coincida exactamente con la imagen adjunta, pero eso es debido a que el aspecto del programa Base puede ser diferente para cada usuario).

## 7.1. Barra de título
Es la barra superior de la ventana en la que se muestra el nombre de la base de datos activa. Haciendo doble clic en ella, la ventana cambiará de tamaño maximizándose o de nuevo, con otro doble clic, recuperando su tamaño original. Así podremos ampliar o disminuir rápidamente el tamaño de la ventana del programa.

## 7.2. Barra de menús
Situada bajo la barra de título, la barra de menús proporciona acceso a todas las acciones que pueden realizarse en Base, organizadas en grupos homogéneos atendiendo a funciones semejantes. Cada entrada permite acceder a las distintas funciones y para activarlas podremos usar tanto el teclado como el ratón tal y como estamos acostumbrados en otras aplicaciones de LibreOffice: en Writer, Calc o Impress, por ejemplo.

## 7.3. Barra de herramientas estándar
Situada bajo la barra de menús, ésta muestra botones que permiten acceder a las funciones más habituales de Base: abrir, guardar, copiar y pegar, acceder a la ayuda, formularios, botones específicos para tablas, ordenar, etc. Podemos ver para qué sirve cada botón gracias a los cuadros informativos que aparecen al pasar el puntero del ratón por encima de ellos y se pueden personalizar de forma que sólo estén a la vista los botones que se usen frecuentemente.

## 7.4. Panel de base de datos
En la zona de la izquierda donde se puede seleccionar el tipo de objeto de la base de datos con el que se quiere trabajar. En una base de datos de Base hay cuatro tipos principales de objetos: tablas, consultas, formularios e informes. De momento sólo te hemos hablado del primero de ellos, pero a medida que avancemos iremos viendo para qué sirve cada uno de los objetos mencionados, cómo crearlos y cómo mantenerlos.

## 7.5. Panel de tareas
En la zona central se encuentran las tareas que se pueden realizar con el tipo de objeto seleccionado. Son herramientas diferentes según cada uno de ellos. Así, por ejemplo, en el caso de la captura de pantalla siguiente, el objeto seleccionado son las Tablas y podemos ver en el panel Tareas las tareas que son posibles realizar relacionadas con este tipo de objetos.

## 7.6. Panel de objetos
En la zona inferior aparecen los objetos creados del tipo seleccionado. En la figura se puede observar que dentro del tipo tabla, todavía no tenemos ningún objeto creado.

# 8. Ayuda de Base
Dentro de la barra de menús existen diferentes posibilidades que nos brindan todas las funcionalidades del programa. El último de todos ellos se llama Ayuda y en él aparecen las distintas opciones de ayuda de LibreOffice. Entre todas las opciones disponibles destacan dos:

Por un lado la opción Ayuda de LibreOffice que contiene una ayuda bastante extensa de todas las herramientas de LibreOffice clasificada por contenidos y con la opción incluida de buscar ayuda recorriendo el índice de contenidos o en función de una palabra clave.
Y, por otro lado, la opción ¿Qué es esto?, que permite que se muestre una pequeña información sobre el objeto en el que tengamos situado el cursor.
Nos centraremos en la primera de las opciones: Ayuda de LibreOffice, la cual mostrará, al ser pulsada, una ventana como la de la figura:
 	 
Ejercicios	
Ejercicio
 	
Cerrar la base de datos

Cierra la base de datos "biblioteca". Ve al menú Archivo → Cerrar.
 	 
 	
IMPORTANTE
 	 
Ojo	
En las prácticas siguientes vamos a trabajar sobre la misma base de datos "biblioteca". Cuando terminemos las prácticas de formularios, subiremos el archivo.
