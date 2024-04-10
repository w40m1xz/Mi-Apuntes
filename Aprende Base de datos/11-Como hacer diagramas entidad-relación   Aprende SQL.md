
nos vamos
![[Pasted image 20240410020257.png]]
a la casita
 y hacemos click
 ![[Pasted image 20240410020307.png]]
![[Pasted image 20240410020340.png]]
![[Pasted image 20240410020434.png]]

luego nos vamos add diagram
![[Pasted image 20240410020434.png]]

luego
![[Pasted image 20240410020442.png]]
nueva ves  alli le damos add diagram

![[Pasted image 20240410020519.png]]
y no abre esto

al lado derecho 
podemos utilizar pre tabla diseñado 

hacemos click dos veces a la tabla usuario



![[Pasted image 20240410020609.png]]

![[Pasted image 20240410020645.png]]

borramos el ultimo
![[Pasted image 20240410020721.png]]

![[Pasted image 20240410020822.png]]
y creamos una columna llamada id

cambiamos para que sea int

![[Pasted image 20240410020814.png]]

![[Pasted image 20240410020918.png]]

lo subimos para que id este en la primera
![[Pasted image 20240410020946.png]]

![[Pasted image 20240410021016.png]]
definimos nuestra id como nuestra primary key

![[Pasted image 20240410021052.png]]

tambien se marco NN  q es not null

![[Pasted image 20240410021134.png]]

marcamos UQ en username y email

UQ= QUE TIENE QUE SER UNICO

![[Pasted image 20240410021204.png]]
tambien ponemos email NN


como obtengo la consulta sql de esta tabla para eventualmente crearla en una consulta
le damos click a la tabla
![[Pasted image 20240410021319.png]]
donde dice SQL to clipboard

volvemos atras en nuestra otra pestaña

![[Pasted image 20240410021410.png]]
aca tenemos la tabla copiada
es util pero tambien es importante saber escribirlo a mano

tenemos alguna cosa
![[Pasted image 20240410021519.png]]

lo que dice es que si la tabla no existe creara

tmb

![[Pasted image 20240410021554.png]]
además tenemos unos índices , lo q hace toma eso campo y lo tomas en memoria , lo que hace mas rapido

osea
![[Pasted image 20240410021746.png]]
que se va carga en la memoria ram lo que hace una rapide en buscar 
en caso de tener casi infinito de info

Continuamos añadimos una tabla de producto

![[Pasted image 20240410021924.png]]

![[Pasted image 20240410021931.png]]
le damos click ai luego para poner una tabla

![[Pasted image 20240410022018.png]]

le ponemos el nombre de product

le pònemos colummna

![[Pasted image 20240410022050.png]]

pinchamos ai
![[Pasted image 20240410022308.png]]

![[Pasted image 20240410022215.png]]


![[Pasted image 20240410022802.png]]

en este caso debemos indicarle cual es la relacion de user y product

![[Pasted image 20240410022903.png]]

no vamos aca

![[Pasted image 20240410022946.png]]
ponemos foreig key  create_by

hace referencia a by
![[Pasted image 20240410023027.png]]
lo que genera altiro una relacion

![[sea21312313.png]]
![[Pasted image 20240410023731.png]]
ahora aca debemos indiciar cual es la columna que queremos referenciar en la tabla de origen y de destino

![[Pasted image 20240410023824.png]]

lo pinchamos

![[Pasted image 20240410024148.png]]
vemos asi significa que puede ser null porq  sale relleno con blanco

![[Pasted image 20240410024239.png]]

nos vamos aca a columms y le damos NN( NOT NULL)

![[Pasted image 20240410024336.png]]
![[Pasted image 20240410024341.png]]

![[Pasted image 20240410024431.png]]

![[Pasted image 20240410024441.png]]

aprovechamos de poner NN A name y brand

Para evitar la repeticion
podemos sacar brand varchar

es posible que se repite mucho una marca ejemplo ipad
ante de todos

![[Pasted image 20240410025304.png]]
cambiamos
![[Pasted image 20240410025313.png]]
de la tabla productor brand a brand_id

creamos una tabla
![[Pasted image 20240410024857.png]]
	![[Pasted image 20240410024948.png]]
	y lo dejamos asi


nos vamos a la tabla product
![[Pasted image 20240410025443.png]]
cambiamos brand a int

![[Pasted image 20240410025422.png]]
![[Pasted image 20240410025538.png]]
ponemos forig keyn brand_id que hace referencia a a la tabla brand

mientras lo seleccionas

![[Pasted image 20240410025628.png]]

le asignamos el brand_id


creamos nuestra tabla orden de compra

![[Pasted image 20240410025822.png]]

le añadimos esto
vamos abajo

![[Pasted image 20240410025838.png]]

donde dice abajo foreign key

![[Pasted image 20240410025927.png]]

pone esto 

un truco

nos vamos 

![[Pasted image 20240410030005.png]]

aca esa que dice n:m![[Pasted image 20240410030021.png]]

pinchamos

![[Pasted image 20240410030108.png]]
luego 

![[Pasted image 20240410030118.png]]

![[Pasted image 20240410030126.png]]

nos crea una tabla que se llama orde_has_product
lo vamos modificar un poco

![[Pasted image 20240410030211.png]]
quitamos pk

![[Pasted image 20240410030228.png]]

vemos q esta configurado

![[Pasted image 20240410030318.png]]

y añadimos id (pk)


![[Pasted image 20240410030344.png]]


como lo agarramos y transfórmalo en una  consulta sql

nos vamos  file

![[Pasted image 20240410030541.png]]


![[Pasted image 20240410030645.png]]

le damos continue

![[Pasted image 20240410030723.png]] 

y aca te entrega la consulta