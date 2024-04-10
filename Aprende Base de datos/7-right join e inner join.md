 
 aquí nosotros tenemos a nuestra tabla de usuario y acá tenemos a nuestra tabla de producto cuando nosotros hacemos un radio vendría siendo lo mismo que el lección pero el que va a traer absolutamente todos los datos dependiendo de la consulta va a hacer de la tabla de la derecha que en este caso vendría siendo de nuestra tabla de productos y en el caso que él encuentre datos dentro de la tabla de usuarios este los va a atraer pero si no existe un dato que se logre relacionar con algún elemento de la tabla de producto en ese caso sencillamente no lo va a traer de usuario entonces es como lo mismo que el left join pero en lugar de utilizar la tabla de usuario como la tabla principal utiliza la tabla de productos y eso lo que hace es que cambia el resultado que nosotros terminamos recibiendo
![[Pasted image 20240409234415.png]]
  
El `RIGHT JOIN` es una cláusula en SQL que se utiliza para combinar registros de dos tablas basándose en una condición especificada y devolver todos los registros de la tabla de la derecha (tabla del segundo argumento) y los registros coincidentes de la tabla de la izquierda (tabla del primer argumento), o `NULL` si no hay coincidencias.

El `RIGHT JOIN` es útil cuando deseas recuperar todos los registros de la tabla de la derecha, incluso si no hay coincidencias en la tabla de la izquierda. Esto puede ser útil en situaciones donde tienes una tabla principal y una tabla secundaria y deseas asegurarte de obtener todos los registros de la tabla secundaria, independientemente de si hay una correspondencia en la tabla principal.

Por ejemplo, considera una tabla de empleados y una tabla de departamentos. Si deseas obtener todos los departamentos, junto con la información de los empleados que pertenecen a esos departamentos, incluso si hay departamentos sin empleados, podrías usar un `RIGHT JOIN` para asegurarte de que obtienes todos los departamentos, con o sin empleados asignados.

Aquí tienes un ejemplo de cómo se vería la consulta:


`SELECT d.department_name, e.employee_name FROM departments d RIGHT JOIN employees e ON d.department_id = e.department_id;`

En esta consulta, se seleccionarían todos los departamentos de la tabla `departments`, y si hay empleados asociados a esos departamentos en la tabla `employees`, se mostrarían sus nombres. Si no hay empleados asociados a un departamento, el campo de nombre del empleado sería `NULL`, pero aún así se mostraría el nombre del departamento.

# volvemos al ejemplo del curso :

![[Pasted image 20240409234648.png]]


## select u.id, u.email, p.name from user u right join product p on u.id= p.created_by;

esto nos devuelve

![[Pasted image 20240409234736.png]]
![[Pasted image 20240409234747.png]]
lo principal que nos devuelve es lo producto

si se fija muestra el id del usuario

 pero el usuario chanchito no lo está mostrando y esto es porque no se encontró un registro en la tabla de la derecha que en este caso en la tabla de productos que pudiera ser asociado con la tabla de usuario esta es la razón por la cual nosotros acá estamos que no solamente el listado de productos pero también nos falta el usuario de chanchito


# Inner join


El `INNER JOIN` es otra cláusula utilizada en SQL para combinar registros de dos tablas basándose en una condición especificada. La principal diferencia entre un `INNER JOIN` y otros tipos de join, como `LEFT JOIN` o `RIGHT JOIN`, es que un `INNER JOIN` solo devuelve los registros que tienen coincidencias en ambas tablas.

En otras palabras, cuando usas un `INNER JOIN`, solo obtienes las filas donde hay coincidencias entre las tablas en la columna especificada en la condición de join.

Por ejemplo, si tienes una tabla de empleados y una tabla de departamentos, y deseas obtener una lista de todos los empleados junto con sus respectivos departamentos, solo si los empleados están asignados a un departamento, usarías un `INNER JOIN` para asegurarte de obtener solo los registros donde haya coincidencias en ambas tablas.

Aquí tienes un ejemplo de cómo se vería la consulta:

`SELECT e.employee_name, d.department_name FROM employees e INNER JOIN departments d ON e.department_id = d.department_id;`

En esta consulta, solo se devolverán las filas donde haya coincidencias en la columna `department_id` entre las tablas `employees` y `departments`. Si hay empleados sin departamento o departamentos sin empleados, estas filas no se incluirán en el resultado de la consulta.

## SIGUIENDO CURSO

![[Pasted image 20240409235534.png]]
EN el caso de inner join
[[]]
Nos va traer tanto usuario  como producto

siempre y cuando  esto dos puedan ser asociado

osea la interseccion de estas dos tabla

![[Pasted image 20240409235827.png]]

![[Pasted image 20240409235839.png]]
en este caso nos traer todos los productos que se encuentra registrado (porque todo estan asociado a un usuario)