# Conversaciones: Soporte del profesorado

## Elaboración de ejercicios y prácticas

**Diseñame un modelo de datos para llevar a cabo la gestión de préstamos de libros de una biblioteca.**

>A continuación presento un modelo de datos para llevar a cabo la gestión de préstamos de libros de una biblioteca:
>
>Tabla de Libros:
>
> - ID del Libro (Primary Key)
> - Título
> - Autor
> - Año de Publicación
> - Editorial
> - Género
> - Cantidad de Copias Disponibles
>
>Tabla de Usuarios:
>
> - ID del Usuario (Primary Key)
> - Nombre
> - Apellido
> - Dirección
> - Correo Electrónico
> - Teléfono
> - Fecha de Nacimiento
>
>Tabla de Préstamos:
>
> - ID del Préstamo (Primary Key)
> - ID del Libro (Foreign Key, relacionado con la Tabla de Libros)
> - ID del Usuario (Foreign Key, relacionado con la Tabla de Usuarios)
> - Fecha de Préstamo
> - Fecha de Devolución
> - Devuelto (Boolean)
>
>Este modelo de datos permite registrar la información de los libros disponibles en la biblioteca, los detalles de los usuarios y los detalles de los préstamos de libros, incluyendo la fecha en la que se prestó el libro y la fecha en que se espera su devolución. También se puede registrar si un libro ha sido devuelto o no.
>
>La relación entre las tablas se establece mediante claves foráneas, lo que permite obtener información detallada sobre los libros prestados a cada usuario y sobre los usuarios que han prestado cada libro.

**Modifica el modelo de datos de forma que se añada una tabla de tipo de usuario, y que dentro del tipo de usuario se indique el tiempo máximo de préstamo. De esa forma, la fecha de devolución se debe de calcular en función de la fecha de préstamo y el tiempo máximo de préstamo del usurio que lo realiza.**

>A continuación presento una modificación del modelo de datos para incluir una tabla de tipo de usuario y para calcular la fecha de devolución en función de la fecha de préstamo y el tiempo máximo de préstamo del usuario:
>
>Tabla de Libros:
>
> - ID del Libro (Primary Key)
> - Título
> - Autor
> - Año de Publicación
> - Editorial
> - Género
> - Cantidad de Copias Disponibles
>
>Tabla de Usuarios:
>
> - ID del Usuario (Primary Key)
> - Nombre
> - Apellido
> - Dirección
> - Correo Electrónico
> - Teléfono
> - Fecha de Nacimiento
> - ID del Tipo de Usuario (Foreign Key, relacionado con la Tabla de Tipo de Usuario)
>
>Tabla de Tipo de Usuario:
>
> - ID del Tipo de Usuario (Primary Key)
> - Nombre del Tipo de Usuario
> - Tiempo Máximo de Préstamo (en días)
>
>Tabla de Préstamos:
>
> - ID del Préstamo (Primary Key)
> - ID del Libro (Foreign Key, relacionado con la Tabla de Libros)
> - ID del Usuario (Foreign Key, relacionado con la Tabla de Usuarios)
> - Fecha de Préstamo
> - Fecha de Devolución (calculada a partir de la fecha de préstamo y el tiempo máximo de préstamo del usuario)
> - Devuelto (Boolean)
>
>Este modelo de datos permite registrar la información de los libros disponibles en la biblioteca, los detalles de los usuarios y los tipos de usuario existentes, incluyendo el tiempo máximo de préstamo permitido para cada tipo de usuario. También permite registrar los detalles de los préstamos de libros, incluyendo la fecha en la que se prestó el libro, y la fecha de devolución, que se puede calcular automáticamente en función de la fecha de préstamo y el tiempo máximo de préstamo del usuario. La relación entre las tablas se establece mediante claves foráneas, lo que permite obtener información detallada sobre los libros prestados a cada usuario y sobre los usuarios que han prestado cada libro.

**Quiero que el modelo también permita controlar renovaciones de préstamos, guardando información de cada ocasión en la que se ha renovado un libro.**

>A continuación presento una modificación del modelo de datos para incluir renovaciones de préstamos:
>
>Tabla de Libros:
>
> - ID del Libro (Primary Key)
> - Título
> - Autor
> - Año de Publicación
> - Editorial
> - Género
> - Cantidad de Copias Disponibles
>
>Tabla de Usuarios:
>
> - ID del Usuario (Primary Key)
> - Nombre
> - Apellido
> - Dirección
> - Correo Electrónico
> - Teléfono
> - Fecha de Nacimiento
> - ID del Tipo de Usuario (Foreign Key, relacionado con la Tabla de Tipo de Usuario)
>
>Tabla de Tipo de Usuario:
>
> - ID del Tipo de Usuario (Primary Key)
> - Nombre del Tipo de Usuario
> - Tiempo Máximo de Préstamo (en días)
>
>Tabla de Préstamos:
>
> - ID del Préstamo (Primary Key)
> - ID del Libro (Foreign Key, relacionado con la Tabla de Libros)
> - ID del Usuario (Foreign Key, relacionado con la Tabla de Usuarios)
> - Fecha de Préstamo
> - Fecha de Devolución (calculada a partir de la fecha de préstamo y el tiempo máximo de préstamo del usuario)
> - Devuelto (Boolean)
>
>Tabla de Renovaciones:
>
> - ID de la Renovación (Primary Key)
> - ID del Préstamo (Foreign Key, relacionado con la Tabla de Préstamos)
> - Fecha de Renovación
>
>Este modelo de datos permite registrar la información de los libros disponibles en la biblioteca, los detalles de los usuarios y los tipos de usuario existentes, incluyendo el tiempo máximo de préstamo permitido para cada tipo de usuario. También permite registrar los detalles de los préstamos de libros, incluyendo la fecha en la que se prestó el libro, y la fecha de devolución, que se puede calcular automáticamente en función de la fecha de préstamo y el tiempo máximo de préstamo del usuario. Además, permite registrar las renovaciones de préstamos, incluyendo la fecha de renovación de cada préstamo. La relación entre las tablas se establece mediante claves foráneas, lo que permite obtener información detallada sobre los libros prestados a cada usuario, los usuarios que han prestado cada libro, y las renovaciones realizadas para cada préstamo.

**Quiero que propongas  preguntas sobre consultas SQL que utilicen el modelo propuesto, además de sus respectivas soluciones. Las consultas han de incluir operaciones JOIN, y la dificultad ha de ser creciente. **

>A continuación presento 4 preguntas sobre consultas SQL y sus respectivas soluciones, utilizando el modelo de datos propuesto:
>
>¿Cuántos libros ha prestado cada usuario?
>
>Solución:
```
SELECT Usuarios.Nombre, Usuarios.Apellido, COUNT(Préstamos.ID del Préstamo) AS Número de Préstamos
FROM Usuarios
JOIN Préstamos ON Usuarios.ID del Usuario = Préstamos.ID del Usuario
GROUP BY Usuarios.Nombre, Usuarios.Apellido
```
>¿Qué usuarios han renovado un libro específico?
>
>Solución:
```
SELECT Usuarios.Nombre, Usuarios.Apellido, Libros.Título
FROM Usuarios
JOIN Préstamos ON Usuarios.ID del Usuario = Préstamos.ID del Usuario
JOIN Renovaciones ON Préstamos.ID del Préstamo = Renovaciones.ID del Préstamo
JOIN Libros ON Préstamos.ID del Libro = Libros.ID del Libro
WHERE Libros.Título = 'Nombre del Libro'
```
>¿Cuántas veces se ha renovado cada libro?
>
>Solución:
```
SELECT Libros.Título, COUNT(Renovaciones.ID de la Renovación) AS Número de Renovaciones
FROM Libros
JOIN Préstamos ON Libros.ID del Libro = Préstamos.ID del Libro
JOIN Renovaciones ON Préstamos.ID del Préstamo = Renovaciones.ID del Préstamo
GROUP BY Libros.Título
```
>¿Cuántos libros ha prestado cada tipo de usuario y cuántos se han renovado?
>
>Solución:
```
SELECT Tipo de Usuario.Nombre del Tipo de Usuario, COUNT(Préstamos.ID del Préstamo) AS Número de Préstamos, SUM(CASE WHEN Renovaciones.ID de la Renovación IS NOT NULL THEN 1 ELSE 0 END) AS Número de Renovaciones
FROM Usuarios
JOIN Préstamos ON Usuarios.ID del Usuario = Préstamos.ID del Usuario
JOIN Tipo de Usuario ON Usuarios.ID del Tipo de Usuario = Tipo de Usuario.ID del Tipo de Usuario
LEFT JOIN Renovaciones ON Préstamos.ID del Préstamo = Renovaciones.ID del Préstamo
GROUP BY Tipo de Usuario.Nombre del Tipo de Usuario
```