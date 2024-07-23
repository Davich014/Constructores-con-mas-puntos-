# Constructores-con-mas-puntos-
Una aplicación de escritorio que muestra los resultados de los constructores de Fórmula 1 en una tabla. Permite al usuario filtrar los resultados para ver solo el constructor con más puntos o resetear la vista para mostrar todos los resultados. Utiliza JavaFX para la interfaz gráfica y JDBC para la conexión a la base de datos.

Clase ConstructorResults

Esta clase representa los resultados de los constructores en una carrera de Fórmula 1. Sus atributos son:


constructorResultId: Identificador único del resultado del constructor.

raceId: Identificador de la carrera.

constructorId: Identificador del constructor.

points: Puntos obtenidos en la carrera.

status: Estado del resultado (por ejemplo, si fue una victoria, abandono, etc.).

Métodos

Constructor: Inicializa los atributos de la clase.

Getters y Setters: Métodos para obtener y modificar los atributos.

Clase ConstructorResultsApp

Esta clase es una aplicación JavaFX que muestra una tabla con los resultados de los constructores.


Atributos

constructorResults: Lista observable que almacena los resultados de los constructores.

Método start

Este método es el punto de entrada de la aplicación JavaFX.


Creación de la Tabla:


Se crea un TableView para mostrar los resultados.
Se definen varias columnas (constructorResultIdCol, raceIdCol, etc.) para mostrar los diferentes atributos de ConstructorResults.
Se establece el CellValueFactory para cada columna, que indica de dónde obtener los datos.


Conexión a la Base de Datos:

Se conecta a una base de datos MySQL usando JDBC.
Se ejecuta una consulta SQL para obtener todos los registros de la tabla constructorresults.
Por cada resultado obtenido, se crea un objeto ConstructorResults y se añade a la lista constructorResults.
Botones para Filtrar y Resetear:

Se crea un botón para filtrar los resultados y mostrar solo el constructor con más puntos.
Se implementa la lógica para encontrar el constructor con más puntos y actualizar la tabla.
Se crea otro botón para resetear la tabla y mostrar todos los resultados.
Diseño de la Interfaz:

Se utiliza un BorderPane para organizar la disposición de los elementos.
Se establece un Label en la parte superior, la tabla en el centro y los botones en la parte inferior.
Se crea una escena y se muestra en el Stage.


Método main

Este método inicia la aplicación JavaFX.

CAPTURAS DEL CODIGO EJECUTADO
![image](https://github.com/user-attachments/assets/75ab3151-4a69-432a-bf27-14a82e812870)
![image](https://github.com/user-attachments/assets/c6850466-c8f2-4b92-9d48-7020b19ebc8f)

