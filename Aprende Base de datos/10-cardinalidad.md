

Se refiere a la relaciones que puede tener una tabla y otras

![[Pasted image 20240410012909.png]]

lo que tenemos aca una tabla de producto

-que existe una columna llamada created_by(fk)

entonce con eso sabemos que la tabla de user y de producto tiene una relacion


 la cardinal  se refiere a las relaciones que pueden tener unas tablas y otras ,en este caso yo lo que voy a hacer es que me voy a crear una tabla por ejemplo la de usuario que es la que nosotros habíamos hecho antes y esta tabla de usuario contenía un id y un montón de otros datos que por ahora no son relevantes ,pero además nosotros teníamos una tabla de producto y esta tabla de producto también contenía una id pero dentro de todos los otros datos o todas las otras columnas que éste tenía también existía una columna que se llamaba create_by esta columna de created by era el id  del usuario pero sea esto de create by finalmente terminaba siendo una FK(clave foránea Foreign key) y que hacía referencia a la tabla de usuario más específicamente a su columna ID, de esta manera nosotros sabemos de que la tabla de productos tabla de usuario estos tienen una relación 
 
 y cuando nosotros sabemos de que en una de las tablas que se encuentran relacionadas se encuentra nuestra llave foránea en ese caso nosotros sabemos de que aquí se va a encontrar un n Y con el n me refiero de que va a existir mucho de eso comparado con lo otro y en este caso en la tabla de usuarios como no existe una referencia de la tabla de producto pero si existe una referencia al usuario en la tabla de producto nosotros decimos de que un usuario tiene un 1 y la relación entre ambas tablas es de 1 es a n ,donde un usuario puede tener muchos productos y un producto solamente puede tener un usuario en este caso el usuario que lo creó y en este caso tenemos la cardinal y that de 1 esa n 

ES DECIR:
La tabla de "Producto" contiene una columna llamada "created_by", que actúa como una clave foránea (FK) que referencia el ID del usuario que creó el producto en la tabla de "Usuario". Esta relación establece que un usuario puede crear muchos productos (relación de uno a muchos), pero un producto solo puede ser creado por un único usuario. La clave foránea garantiza que cada producto esté asociado con un único usuario.



	Si queremos agregar mas producto seria otra tipo de relacion n es a n

![[Pasted image 20240410014505.png]]
-
  "(PK)" indica que la columna es una clave primaria.
- "(FK)" indica que la columna es una clave foránea.
+-------------+           +-------------+          +-----------------+          +--------+
|                     |             |                     |            |                         |            |              |
|   User           |             |   Product     |            |   order_detail   |            | Order    |
|                     |             |                     |            |                        |             |              | 
+-------------+           +-------------+           +-----------------+         +--------+
| id (PK)          |            | id (PK)          |            | id (PK)               |           | id (PK)  |
|                     |            | created_by (FK)         | order_id (FK)     |           |              |
|                     |            |                      |            | product_id (FK) |           |              |
+-------------+           +-------------+          +-----------------+          +--------+

    ^                        ^                     ^                     ^
    |                        |                     |                     |
    |                        |                     |                     |
    |                        |                     |                     |
  Uno                      Uno                   Muchos                Muchos
    |                        |                     |                     |
    |                        |                     |                     |
    |                        |                     |                     |
    +---- Uno a muchos ---->+                     |                     |
    |                        +---- Uno a muchos --+                     |
    |                        |                                          |
    +------------------------+------------------------------------------+
![[Pasted image 20240410020048.png]]
![[Pasted image 20240410020105.png]]
