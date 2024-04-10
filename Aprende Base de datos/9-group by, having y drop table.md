

 by group ahí se utiliza con instrucciones que por lo general tienden a agrupar elementos como por ejemplo count en este caso van a tomar todos los registros en base a un pivote como por ejemplo podría ser la marca y lo que va a hacer es que los va a agrupar en registros completamente individuales en este caso nosotros tenemos seis productos los cuales son todos de la misma marca y por ende lo que hará será mostrarnos un registro y luego indicar a que esté en total son seis pensando que son los productos que nosotros hemos ingresado hasta ahora
 
  ![[Pasted image 20240410001838.png]]
  si nosotros hiciéramos esta misma agrupación pero por ejemplo con el usuario nosotros tendríamos que esta instrucción de count tendría algo así como 3 productos para el primer usuario 2 para el segundo 2 para el 3 0 1 y así sucesivamente no me acuerdo exactamente cuántos usuarios crearon cuantos productos pero se va a ver algo más o menos así vamos a ver ahora es
![[Pasted image 20240410001908.png]]
![[Pasted image 20240410001958.png]]
# select count(id), marca from product group by marca;

![[Pasted image 20240410002019.png]]

vemos que tenemos 6 productos de apple


### select count(p.id), u.name from product p left join user u on u.id = p.created_by group by p.created_by;


  
La consulta que proporcionaste realiza lo siguiente:

1. Selecciona el recuento de la columna `id` de la tabla `product` (representado como `COUNT(p.id)`).
2. También selecciona el nombre del usuario de la tabla `user` (representado como `u.name`).
3. Combina las tablas `product` y `user` utilizando un `LEFT JOIN`, donde la relación es que el ID del usuario (`u.id`) es igual al campo `created_by` en la tabla `product` (`p.created_by`).
4. Agrupa los resultados por el nombre del usuario (`u.name`) usando `GROUP BY u.name`.
![[Pasted image 20240410002750.png]]
oscar creo 3 producto
layla 2  producto
nicollas 1 producto

si no queremos el registro de nicolas

![[Pasted image 20240410002859.png]]

usamos el having count(p.id) >=2;

![[Pasted image 20240410003016.png]]




## DROP TABLE


PARA ELIMINAR LA TABLAS

EJEMPLO queremos borrar la tabla de producto

![[Pasted image 20240410003142.png]]

![[Pasted image 20240410003517.png]]

![[Pasted image 20240410003532.png]]

si le damos al icono de refresca ya no sale
	



