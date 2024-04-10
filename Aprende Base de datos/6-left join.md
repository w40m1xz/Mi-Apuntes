

se utliza para unir tablas los llamados join

![[Pasted image 20240409202615.png]]

creamo una nueva ventana (query )

y creamos una tabla

![[Pasted image 20240409203054.png]]

la tabla producto contiene 

id 
created_by
maca
definimos clave primaria id
definimos clave foranea created_by



###### CAMBIAR NOMBRE DE UNA TABLA

![[Pasted image 20240409203311.png]]
Ya que quiero que todo lo nombre sea singular

asi se se cambia
rename table products to product;
![[Pasted image 20240409205645.png]]
si no sale debe darle arriba para refrescar




# OTRA FORMA DE INSERTA en una tabla


![[Pasted image 20240409214641.png]]


asi no tenemos que añadir una en una

vemos como queda la tabla

![[Pasted image 20240409214712.png]]

![[Pasted image 20240409214731.png]]
asi queda


# AHORA HAREMOS UN 

# LEFT JOIN



-de la tabla de usuario y tabla producto
![[Pasted image 20240409215753.png]]

tenemos nuestra dos tabla

left join cuando nosotros hacemos un let join lo que vamos a hacer es indicar que tiene que traerme todos los registros que encuentre en la tabla de usuarios dependiendo de la consulta que nosotros hayamos creado y en el caso que se encuentra en registros dentro de nuestra tabla de producto que hayan sido creados por el uso que aparece en esta consulta de acá en ese caso estos productos van a aparecer dentro de nuestra consulta pero sí que se crearon productos los cuales no aparecen como resultado sus creadores acá en ese caso esos productos no van a aparecer esta es la razón por la cual nosotros podemos representar un led joint de esta manera en este caso el que manda es la tabla de usuarios por la consulta que nosotros hagamos vamos a traer todos los usuarios que esa consulta nos arroje y después si es que estos tienen datos en la tabla de producto en este caso traerlos si es que no deja sencillamente los datos como nulo 


![[Pasted image 20240409215947.png]]
la tabla de usuario manda

![[Pasted image 20240409220907.png]]

# SELECT u.id, u.email FROM user u;


En SQL, `u` es un alias de tabla que se utiliza para abreviar el nombre de la tabla `user`. Cuando ves `u.id`, significa que estás seleccionando la columna `id` de la tabla `user`, pero utilizando el alias `u` en lugar del nombre completo de la tabla. Los alias de tabla son útiles para hacer que las consultas SQL sean más legibles y concisas.

# user u; alli definimos la u como  alias 

![[Pasted image 20240409221348.png]]

tenemos todo los dato

![[Pasted image 20240409224154.png]]


vamos a tomar de la tabla user
ID
name

de la tabla producto OJO

tomaremos id y created by

haremos que created_by se una con el id respectivo 

osea si en 

Producto tenemos created_by id= 1 sea el  valor de la tabla de usuario 1
osea
En la tabla "Producto", hay una columna llamada "created_by" que se utiliza para registrar quién creó ese producto. En este caso, estamos diciendo que si el valor en la columna "created_by" de la tabla "Producto" es 1, entonces el producto fue creado por el usuario que tiene el ID 1 en la tabla "Usuario".

Entonces, cuando vemos que "created_by" tiene el valor 1 en la tabla "Producto", eso significa que el usuario que tiene el ID 1 en la tabla "Usuario" es el creador de ese producto.

establecemos una relación entre los productos y los usuarios mediante el uso de los IDs. El valor 1 en la columna "created_by" de la tabla "Producto" indica que el producto fue creado por el usuario que tiene el ID 1 en la tabla "Usuario".

Tabla: Producto
| id_producto | nombre    | created_by |
|-------------  |----------- |------------|
| 1                  | iPad         | 1          |
| 2                  | iPhone     | 1          |
| 3                  | Macbook | 2          |

Tabla: Usuario
| id_usuario | nombre   |
|------------|----------|
| 1          | Juan     |
| 2          | María    |
| 3          | Carlos   |

En esta tabla, tenemos dos tablas: "Producto" y "Usuario".

- En la tabla "Producto", cada fila representa un producto. El campo `created_by` indica el ID del usuario que creó ese producto.
- En la tabla "Usuario", cada fila representa un usuario. El campo `id_usuario` es el ID único para cada usuario.

Por ejemplo, en la primera fila de la tabla "Producto", tenemos un producto llamado "iPad" (con ID 1) y el campo `created_by` tiene el valor 1. Esto significa que el usuario que tiene el ID 1 en la tabla "Usuario" (es decir, Juan) fue quien creó el iPad.

![[Pasted image 20240409225333.png]]


select u.id, u.email, p.name from user u left join product p on u.id= p.created_by;


1. **SELECT**: Indica qué columnas se seleccionarán en el resultado.
    
2. **u.id, u.email**: Selecciona el ID y el correo electrónico de cada usuario de la tabla "user" (alias "u").
    
3. **p.name**: También selecciona el nombre de cualquier producto asociado a esos usuarios, de la tabla "product" (alias "p").
    
4. **FROM user u**: Establece que los datos se seleccionarán de la tabla "user" y le asigna el alias "u".
    
5. **LEFT JOIN product p**: Une la tabla "user" con la tabla "product" utilizando un "left join". Esto significa que todos los registros de la tabla "user" serán incluidos en el resultado, incluso si no hay una coincidencia en la tabla "product". La tabla "product" se denota con el alias "p".
    
6. **ON u.id = p.created_by**: Establece la condición de unión. Aquí, estamos uniendo las filas de las dos tablas donde el ID del usuario en la tabla "user" es igual al valor de la columna "created_by" en la tabla "product". Esto indica que estamos relacionando los productos con sus respectivos creadores.

# *explicacion paso a paso*


### select from user u - < asignamos un alias a la tabla de usuario

### entonce con esto ya creado

### select u.id,  u.email from user  u;

### select u.id,  u.email from user  u left join product;

queremos unir la tabla product

ASIGNAMOS UN alias a producto
# select u.id,  u.email, p.name from user  u left join product p;

definimos

# u.id = p.created_by;

le estamos diciendo


que el id de la tabla de usuario  sea =  a  la columna de created_by de producto

![[Pasted image 20240409233756.png]]


### select u.id,  u.email, p.name from user  u left join product p on u.id= p.created_by;


![[Pasted image 20240409233744.png]]

asi se ve  

la gracias es que se juntaron

tenemos una tabla de usuario y producto