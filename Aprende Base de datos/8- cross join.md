
El `CROSS JOIN` es otra cláusula utilizada en SQL para combinar cada fila de la primera tabla con cada fila de la segunda tabla, lo que resulta en un conjunto de resultados que es el producto cartesiano de ambas tablas. En otras palabras, cada fila de la primera tabla se combina con todas las filas de la segunda tabla.

El `CROSS JOIN` no requiere ninguna condición de join, ya que combina todas las filas de ambas tablas sin considerar ninguna condición de coincidencia. Por esta razón, puede generar un conjunto de resultados muy grande si las tablas implicadas tienen un gran número de filas.

Este tipo de join se utiliza cuando necesitas combinar todas las filas de una tabla con todas las filas de otra tabla y no necesitas una condición de join específica.

Aquí tienes un ejemplo de cómo se vería la consulta:

sqlCopy code

`SELECT * FROM tabla1 CROSS JOIN tabla2;`

En esta consulta, `tabla1` y `tabla2` son los nombres de las tablas que deseas combinar mediante `CROSS JOIN`. Cada fila de `tabla1` se combinará con cada fila de `tabla2`, lo que resultará en un conjunto de resultados que contiene todas las posibles combinaciones de filas de ambas tablas.

EJEMPLO


![[Pasted image 20240410000616.png]]
TENEMOS esto

| primera | segunda |
|---------|---------|
|       1 |       a |
|       1 |       b |
|       1 |       c |
|       1 |       d |
|       2 |       a |
|       2 |       b |
|       2 |       c |
|       2 |       d |
|       3 |       a |
|       3 |       b |
|       3 |       c |
|       3 |       d |
|       4 |       a |
|       4 |       b |
|       4 |       c |
|       4 |       d |
![[Pasted image 20240410000655.png]]
se juntan 


![[Pasted image 20240410000830.png]]
queda 
# select u.id, u.name, p.id, p.name from user u cross join product p;

no se especifica donde se va juntar una tabla con respecto a la otra

![[Pasted image 20240410000944.png]]

se cruzan 
