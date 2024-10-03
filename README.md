# VentaCasas
Proyecto en php utilizando gulp y sass

1.	Posibles Bugs

Manejo de errores en la conexión a la base de datos:
	Ya que se está manejando la conexión a la base de datos, no se está manejando un posible error en la conexión. Así que se agregara una validación que capture errores de conexión.

2.	Vulnerabilidades
Inyección SQL
	Aunque se esté usando la función mysqli_real_escape_string para escapar las entradas del formulario, es insuficiente contra inyecciones SQL. Por ende, es más seguro usar consultas preparadas con sentencias preparadas en lihar de concatenar cadenas SQL. 

3.	Code Smells
Repetición de ‘mysqli_real_escape_string’
	Esta parte del código se repite varias veces, así que se creara una función que simplifique el escape de variables para reducir la redundancia:
