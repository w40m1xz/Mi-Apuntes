
ya aprendimos la 4 acciones principales

![[Pasted image 20240409163223.png]]
ahora se vera

profundizar un poco mas ,otras forma que nosotros podemos seleccionar los elementos  que se puede encontrar dentro de una tabla

vamos a crear una nueva tabla  ( de usuario)


![[Pasted image 20240409191301.png]]


CREATE TABLE user (
      id int not null auto_increment,
      name varchar(50) not null,
      edad int not null,
      email varchar(100) not null,
      primary key (id)
);
luego insertamos datos para hacer consulta
INSERT iNTO user (name, edad, email) values ('Oscar'. 25. 'oscar@gmail.com');


ejecutamos la primero para crear y luego cada uno de lo que insertamos

seleccionando todo y luego dandole ctrl + enter

y lo de inserta uno por uno lo seleccionamos y le damos ctrl + enter


Seleccionamos select * user para ver to lo que tenemos

![[Pasted image 20240409193014.png]]
![[Pasted image 20240409193042.png]]

vamos usar ahora lo mismo

![[Pasted image 20240409193127.png]]

pero con limit lo que hace es limitar la cantidad de recurso que se va retornar a nosotros en ese caso le decimos 1

![[Pasted image 20240409193318.png]]
lo que no limita y no retornar el primer registro que este encuentra

tambien


![[Pasted image 20240409193419.png]]
podemos asignarle cierta  indicacion donde edad tiene que ser mayo a 15

select * from user where edad > 15;
![[Pasted image 20240409193548.png]]
nos devolvio solo la edad mayor
![[Pasted image 20240409193621.png]]
en este caso es si es igual o mayor a 15 por eso no muestra layla que tiene 15

select * from user where edad >= 15;


O otro caso




![[Pasted image 20240409193846.png]]




select * from user where edad > 20 and email = 'nico@gmail.com';

independiente si existe otro usuario porque solo hay 1 con 20 años y con ese correo

![[Pasted image 20240409193941.png]]


EN ESTE CASO

![[Pasted image 20240409194022.png]]
select * from user where edad > 20 or email = 'layla@gmail.com';

EN este caso ocurre esto

van a traer todo lo registro que cumpla la condicion que cumpla 20 años

pero si independiente de eso existe un registro que contiene el correo layla@gmail.com en ese caso tambien lo devuelve

![[Pasted image 20240409194257.png]]

![[Pasted image 20240409194336.png]]
esto lo que hace es buscar todo lo registro quecumpla con no tener el correo layla@gmail.com

![[Pasted image 20240409194436.png]]


si queremos buscar una edad hasta cierta 
![[Pasted image 20240409194543.png]]

usamos el between para buscar la edad entre 15 y 30

![[Pasted image 20240409194644.png]]



Ahora veremos una instrucción para cual sirve para buscar registro a la base de dato es mas practica cuando el usuario quiere buscar algo

*EL CASO DE USO MAS PRACTICO tomar los datos en un formulario y luego se pasa ese dato a esa consulta sql pero no antes debe si o si ir  sanitizado *





![[Pasted image 20240409195219.png]]

# select * from user where email like '%gmail%';

EN ESTE CASO buscar en el campo de email esta cadena
donde me da igual el inicio y el final 

podria decir lalagmail y podria ser valido

o gmail a seca y tmb

devuelve todo lo registro al final porque todo tiene un correo

# EJEMPLO 2 

![[Pasted image 20240409195409.png]]
SI LE QUITAMOS el & del final

la palabra de gmail puede comenzar con cualquier cosa pero debe terminar con gmail

![[Pasted image 20240409195447.png]]
el resultado es nada

![[Pasted image 20240409195545.png]]

en este caso buscara lo que comienza con oscar pero luego despues de oscar da igual 
solo si empieza con oscar nomas
![[Pasted image 20240409195623.png]]



# ORDER BY

ordenar la edad por ordenar acendente menor a mayor
# select * from user order by edad asc;

![[Pasted image 20240409195749.png]]

ordena lo resultado segun la edad menor a mayor

al revez seria

![[Pasted image 20240409195902.png]]

## select * from user order by edad desc;
![[Pasted image 20240409195949.png]]


BUSCAR LA EDAD MAS GRANDE (SOLO DANDOME EL RESULTADO )

![[Pasted image 20240409200023.png]]
##### select max(edad) as mayor  from user;

para buscar el menor
select min(edad) as menor  from user;

![[Pasted image 20240409200201.png]]


explicando

![[Pasted image 20240409200247.png]]


 usamos la palabra reservada select(para seleccionar)

podemos usar max o min que tendra () donde dentro va  el parametro que va siendo el nombre de la columna
luego  indicamos como se llame as sobrenombre  que este tenga

y luego ponemos from user porq queremos seleccionar user
