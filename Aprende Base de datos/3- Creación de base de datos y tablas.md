

 Lo primero debemos crear una base de datos
 ![[Pasted image 20240409131956.png]]
 luego de eso crear nuestra tablas
nos vamos al progama

![[Pasted image 20240409132236.png]]
ponemos 
create database holamundo;
![[run.png]]
le damos al rayito para crearlo 

ese se encarga de ejecutar toda las consulta

abajo se vera que esto se realizo correctamente

![[Pasted image 20240409132344.png]]

para ver la data bases que tenemos podemos usar esto

show databases;

![[Pasted image 20240409132958.png]]
lo selecionas  y luego de las al rayito

![[Pasted image 20240409133147.png]]
nos mostrara la base de datos que tenemos

ahora podemos empezar a crear tablas

![[Pasted image 20240409133800.png]]
ponemos esto siempre se debe poner el punto y coma siempre

para crear una tabla ponemos CREATE TABLE nombretabla ();

luego nos vamos a devolver dentro de este parentesis
![[Pasted image 20240409133913.png]]
dentro de este paréntesis vamos a ingresar la columna de la tabla de animales

lo primero es el ID
que tenga un valor unico

![[Pasted image 20240409134032.png]]
tenemos que indicarle el tipo de datos que este va tener 

existe muchos

![[Pasted image 20240409134255.png]]
tenemos 

int  -> números enteros

float -> decimal

varchar -> palabras ,oraciones ,frases etc

![[Pasted image 20240409134428.png]]
ponermos id int (entero)
![[Pasted image 20240409134526.png]]
los definimos como varchar pero dentro se tiene que poner en ( ) que tan largo quieres que sea

![[Pasted image 20240409134701.png]]
lo siguiente
un estado

![[Pasted image 20240409134746.png]]

le debemos poner ingresar cual será nuestra clave primaria que es (id)

PRIMARY KEY (NOMBRE DE LA COLUMNA)
![[Pasted image 20240409143815.png]]

para poder ejecutarlo debemos indicarle que  base de dato debemos utilizar

porque si lo dejamos asi no sabe que base de dato va utilitzar

![[Pasted image 20240409145126.png]]
	ponemos use holamundo;
	lo seleccionas y hace click en el rayito
	![[Pasted image 20240409145218.png]]
	una vez echo


seleccionamos la peticion

![[Pasted image 20240409145359.png]]
y le damos a la rayita
![[Pasted image 20240409145434.png]]
podemos ver que se crea bien


podemos hacer la tablas que quedamos  pero por ahora veremos una



#### MODIFICAR TABLA (AFTER TABLE)


ante de inserta debemos hacer esto

debemos hacer que id se autoincremente solo para que cada vez que se añade un valor en la tabla
![[Pasted image 20240409150047.png]]

ALTER TABLE animales MODIFY COLUMN id int auto_increment;

(se pone que es int luego de autoincremento siempre)


# INGRESAR DATO INSERT INTO


![[Pasted image 20240409150317.png]]

INSERT INTO animales (tipo, estado) VALUES ('chanchito', 'feliz');

lo seleccionas y lo ponemos click en el rayito

puedes usar ctrl + enter para hacerlo rapido



# CREAR UNA TABLA


crearemos una tabla con ya con la incrementación anterior  de la id y los datos

podemos para tener una idea rapida para crearlo

![[Pasted image 20240409151242.png]]
SHOW CREATE TABLE animales;
para mostrar 

![[Pasted image 20240409151257.png]]

copiamos eso ctrl +c dandole click

![[Pasted image 20240409151343.png]]
y nos queda asi borramos eso despues de ) final


![[Pasted image 20240409152659.png]]
**ASI ES COMO SE CREA UNA TABLA 
estamos creando la tabla animales
vemos id  que es INT (ENTERO) , not null (que no puede ser nulo)  auto_increment(se autoincrementa )

 tenemos tipo  y estado , ambos  con varchar( de longitud 255) 
tenemos DEFAULT NULL (no es necesario agregarlo al  crear una tabla pero hace que sea mas especifico  para que despues lo veamos va tener ese valor)


### *comentar*
![[Pasted image 20240409152015.png]]
ponemos dos guion -- antes de codigo
![[Pasted image 20240409152141.png]]
esto no arroja ningún error 



INSERTAMOS MAS INFORMACION

![[Pasted image 20240409153124.png]]
Y Seleccionamos cada una  y lo ejecutas


# SELECT

![[Pasted image 20240409153507.png]]

SELECT * FROM animales;

y lo ejecutas

![[Pasted image 20240409153532.png]]
aca vemos los registro que hemos echo


## si queremos ver solo un registro

![[Pasted image 20240409153718.png]]
ponemos 

SELECT * FROM animales where id = 1;

selecciona absolutamente todo de la tabla de animales donde el id sea igual a 1

![[Pasted image 20240409153841.png]]

si queremos  ver mas de una seria asi

![[Pasted image 20240409153959.png]]
![[Pasted image 20240409154009.png]]

## tambien podemos buscar por el string

vemos ejemplo ver por el estado


![[Pasted image 20240409154138.png]]

SELECT * FROM animales WHERE estado= 'feliz';

![[Pasted image 20240409154306.png]]

me devolvió   dos registro con id 1 y id 2

tenemos chanchito y dragón feliz

podemos consultar por algun valor que exista dentro de alguna de la columnas para que este nos devuelva registro

![[Pasted image 20240409154612.png]]

en el caso id esta posee un valor unico por eso no dara un valor

pero si nosotros consultamos por esto valores ejemplo estado puede que no de mas de un registro 

porque puede que existir mas de un registro tenga el valor de feliz en su columna de estado



# AND

se usa dos condiciones que ambas se debe cumplir 
![[Pasted image 20240409155258.png]]
ejemplo

SELECT * FROM animales WHERE estado= 'feliz' AND tipo ='chanchito';
![[Pasted image 20240409155347.png]]
ahora si queremos cambiarlo por felipe

![[Pasted image 20240409155403.png]]
no nos devuelve nada

Ningun registro cumplo con ambos por eso no nos da nada debe si  o si
un estado feliz y un tipo felipe


# UPDATE

es para actualizar

![[Pasted image 20240409161624.png]]

mediante update

queremos actualizar dentro de nuestra tabla de animales nuestra columna de estado  que queremos que estado pase a ser feliz where(donde solamente esto) exista un registro id es 3

![[Pasted image 20240409161831.png]]
vemos actualizado


### DELETE

FORMA ERRONEA

![[Pasted image 20240409162301.png]]
ESTA ES LA FORMA que no se hace ya que ahora viene como en seguro que debe indicarle el id para estar seguro tmb update

LA FORMA CORRECTA

![[Pasted image 20240409162530.png]]

VEMOS como nos queda

![[Pasted image 20240409162541.png]]
![[Pasted image 20240409162715.png]]



