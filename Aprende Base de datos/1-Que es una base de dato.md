

Es cualquier cosa que agrupa información y que esta tenga algun sentido

ejemplo 
![[Pasted image 20240409103632.png]]
lo importante es que tenga datos y que lo datos puedan ser relacionado entres si y tenga algun sentido lo que uno guarda


donde se guarda

![[Pasted image 20240409104250.png]]
Nuestra memoria  nosotros podemos interactuar con nuestra memoria
pero tambien podemos interactuar con memoria de otra persona
y que al final estaría encargado de gestionar  eso datos seria nosotros

hoja y lápiz que es una forma antigua para almacenar

computador 

poder acceder a un computador es mas rápido y eficiente y puede almacenar una gran cantidad de dato lo que le hace una buena alternativa 

para poder acceder a los datos dentro de nuestra de base de dato  usamos software  conocido
![[Pasted image 20240409104413.png]]
O como RDMS

es el software que usaremos para gestionar nuestras bases de datos

entre ellos existen

![[Pasted image 20240409104605.png]]
entre otros ( NOSQL ETC)


  el objetivo de todos estos software que nosotros estamos viendo acá es que éstos nos entreguen un acceso fácil a una base de datos ellos se van a encargar de la seguridad y de la integridad de nuestros datos también tienen otras funcionalidades como por ejemplo para poder efectuar respaldos de nuestras bases de datos tienen funcionalidades también como para importar y exportar los datos se van a encargar también de manejar la concurrencia que para que se hagan una idea la concurrencia vendría siendo que cuando más de una conexión está intentando acceder a la base de datos
![[Pasted image 20240409105242.png]]
ejemplo de  lo concurrencia

si tiene un usuario llamado chanchito feliz

y hay  hay un usuario que quiere accede a ese este usuario de chanchito feliz

pero sin embargo hay otro usuario es el admin

![[Pasted image 20240409105532.png]]
que quiere borrar el usuario de de chanchito feliz

sise hace esto

DE leer el usuario de chanchito feliz  y a la vez hay otro usuario que esta intentando eliminar el registro de chanchito feliz al mismo tiempo podria generar errores
de consistencia en lo datos ya sea quien lo este rayando y tambien para lo que lo escribe

existe manera para manejar esto  tipo de casos en lo distinto sistemas de gestión de base de datos
pero una forma mas comun

primero se encargar

1- LEER
mientras leer no se puede realizar ninguna operación mas
2-  Delete
luego puede borrar 

ya que si dos usuarios quieren hacer eso genera problemas

otro caso seria en que dos usuarios esta modificando el mismo registro 

-todo esto tipo de problema lo soluciona nuestro progama de gestión de base de datos


RDBMS - > LA TAREA IMPORTANTE ES QUE SE CONECTA CON LOS DIFENRENTES TIPOS DE LENGUAJE

![[Pasted image 20240409110954.png]]

Las operaciones mas comun que se ve en los software de gestión
de datos
![[Pasted image 20240409111058.png]]
mejor conocido como crud

que viene siendo
![[Pasted image 20240409111249.png]]
esto es lo mas comun y siempre lo usaras , la app giran  a estas operaciones

para que podamos acceder a lo registro y  tambien realizar toda esta operaciones que tiene que hacer un sistema de gestión de de base de datos 

![[Pasted image 20240409111647.png]]

es la Query  "consulta"

para entenderlo mejor  y mas fácil

es como voy a realizar una petición o una pregunta a mi software de gestión de base datos
si el puede crear el recurso el cual de estoy indicando que cree


![[Pasted image 20240409112200.png]]

hacer hilo twitter buscar foto etc es una consulta 

un ejemplo de empresas grande

veámoslo como una aplicación también es una de las aplicaciones más complejas que existen en la actualidad ellos lo que hacen es que a través de un de gestión de bases de datos realizan consultas a la base de datos para poder obtener esta información la cual se la devuelven al software de gestión de base de datos la cual finalmente es devuelta a la aplicación de facebook y finalmente tú la puedes ver esto ocurre por supuesto también con empresas 


![[Pasted image 20240409112640.png]]

como Amazon donde en Amazon el paso que tú vas a realizar va a ser el de ver un producto y bueno tú realizas esta acción de ver un producto lo que está ocurriendo es que amazon está accediendo a un software de religión data management system para poder ir a buscar todos los datos de los productos que tú estás viendo a una base de datos éstos después son devueltos al software de gestión de bases de datos y finalmente éstos se devuelven al sitio web de amazon para que tú finalmente puedas ver el producto que estabas buscando
![[Pasted image 20240409112648.png]]


existen  dos grande mundo al momento de elegir un software de gestión de base de datos tenemos  SQL( que son base de datos relacionales ) Y NO SQL

![[Pasted image 20240409113039.png]]
SQL usan tabla la cuales tiene filas y columna

y NoSQL tiene múltiples forma

las tablas son similares al Excel
![[Pasted image 20240409113249.png]]
	ejemplo aca tenemos la columnas id nombre edad



-la columna hacen referencia al dato mismo que se guarda
![[Pasted image 20240409113355.png]]

el ID es numero complemente único que se genera automática cuando creamos un registro , y esto cumple con la característica de ser autoincrementar

osea
cuando se ingresa el nombre de Felipe y edad 20 dentro de la tabla

de manera automática se le va asignar un valor lo cual va ser autoincrementar a Felipe :1

![[Pasted image 20240409113733.png]]
y la siguiente al id  va ir incrementando solo el id
![[Pasted image 20240409113807.png]]
asi hasta el ultimo registro que va ser único

	![[Pasted image 20240409113901.png]]
	el cuadrado gigante lo llamaremos tabla


la parte vertical va ser la columna

![[Pasted image 20240409113957.png]]

pero cuando hablamos de los datos que se encuentra dentro de la tabla , la parte horizontal

![[Pasted image 20240409114113.png]]
![[Pasted image 20240409114131.png]]
nos referimos como registro

los valores dentro que se va encontrar se le conoce como datos
![[Pasted image 20240409114232.png]]
1 -> datos
Felipe-> dato
20 > dato


pero cuando
![[Sin título.png]]



A TODA ESTA TABLA DE ASIGNAMOS EL NOMBRE USER

TABLA USUARIA

es alli cuando sabemos que lo datos que se encuentra guardados dentro en esta tabla hace referencia a un usuario y es en ese entonce cuando tenemos información

si nosotros no agrupáramos todos estos datos de una manera que hiciera sentido solo tendríamos
datos suelto 

-*pero no es hasta ahora cuando nosotros de damos un sentido es cuando pasan hacer información




ejemplo 2 tabla producto
podemos tener varios usuario  de la tabla producto : admin, usuario que vayan a comprar ,etc

en este ejemplo veremos el administrador el cual puede crear producto dentro de un software 


![[Pasted image 20240409115655.png]]

![[Pasted image 20240409120527.png]]
ejemplo tenemos el id 1 

nombre (del producto) ipad 
cantidad 500
creado por  :1 (el  usuario osea en este caso administrador es 1)

el usuario numero 1 tambien  puede crear diferente un listado de diferente producto


pero tambien podríamos tener mas de 1 administrador

se identifica un ID Diferente en la columna creado por
![[Pasted image 20240409120922.png]]

la razón por que le pasa un id a creador por
en lugar del nombre del usuario o lo que sea

lo datos podrían cambiar 
y evitar duplicar información

*toda la base de dato se mueven alrededor de este modelo*


guarda un registro en múltiples tabla , guarda otro registro en otra tabla  y asociarlo

en este caso
![[Pasted image 20240409121234.png]]

la forma que vimos se le conoce a esta relacion como *

##### 1 -> N

un usuario puede haber creado muchos producto

pero un producto puede haber sido creado por solo un usuario

##### tenemos caso 2
relacion entre alumnos  y deportes
![[Pasted image 20240409121711.png]]
donde un alumnos de un deporte puede estar inscrito en mas  de una rama deportiva

podemos hacer una tabla intermedia

![[Pasted image 20240409121914.png]]

una que contiene la tabla alumnos_deporte dentro tendriamos
id
alumnos_id
deporte_id

![[Pasted image 20240409122040.png]]

tengo un alumnos  con id 1 repetido dos veces 

el cual se encuentra matriculado en el deporte_id  1 y tambien en el deporte_id 2

pero tambien podriamos tener esto
![[Pasted image 20240409122324.png]]

tener un alumnos_id 2 registrado en el deporte_id  1


y esta relacion  que tiene la tabla alumnos con la tabla deporte se le conoce como una relacion de

# n <---------> n
# n a n


Donde 1 alumno puede estar inscrito en muchos deporte

donde 1 deporte puede tener muchos alumnos

para ir mas a lo conceptos


la columnas que se le llama generalmente id se le conoces como

![[Pasted image 20240409123235.png]]


LLAVE PRIMARIA


pero si este id se encuentra  ejemplo
![[Pasted image 20240409121234.png]]

El de la tabla de usuario se encontrara dentro de la tabla de producto para que nosotros podamos indicarle quien fue el que creo este  producto en este caso se va llamar

![[Pasted image 20240409123655.png]]
### Clave foránea


quedaría asi
![[Pasted image 20240409123821.png]]
ID es primary key (de la tabla User)
usar_id es forering keys (la tabla product)

y nuestra tabla  de alumno deporte

![[Pasted image 20240409124108.png]]
id del la tabla alumnos_deporte es primary key

alumnos_id y deporte_id es forering keys


