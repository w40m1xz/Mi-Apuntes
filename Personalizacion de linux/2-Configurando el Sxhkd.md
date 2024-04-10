
creamo dos directorio

![[Pasted image 20230604032240.png]]
UNA VEZ LISTO VAMOS  al directorio bswpm que bajamos  y q esta en la carpeta descargar


![[Pasted image 20230604033247.png]]
nos metemos a este directorio
![[Pasted image 20230604033311.png]]
tendremos esto
![[Pasted image 20230604034033.png]]
copiamos esto dos archivos bspwm  a la carpeta bspwm  y sxhkdrc a la carpeta sxhkd
![[Pasted image 20230604033812.png]]
aca podemos ver archivo                                                                                                                                       

![[Pasted image 20230604034450.png]]

debes esta amarillo con permiso de ejecutar 
OJO  hacer esto
chmod +x sxhkdrc

luego instalamo kitty

![[Pasted image 20230604143949.png]]

![[Pasted image 20230604144106.png]]

ponermos para que con windows + enter podras abrir terminal con kitty

2)
abrimos el archivo  sxhkd

con esto sirve para abria x ventana donde quieras  pero cambiemo para que lo hagamos por teclado
![[Pasted image 20230604144324.png]]

con windows + tecla arriba abajo etc
![[Pasted image 20230604144659.png]]

asi lo dejamos esto es para el marco ojo
lo mismo
![[Pasted image 20230604145437.png]]
lo preselectores donde va el progama que desee como en ese marco lo dejamos asi

para cancelar la cosa  de lo preselectore lo dejamos asi
![[Pasted image 20230604145849.png]]
ahora esto

![[Pasted image 20230604145925.png]]

es para cuando tiene una ventana normal la puede convertir una ventana flotante

osea de la proporción q tiene lo puedes cambia a tu gusto

esto lo comentamos
![[Pasted image 20230604150557.png]]
pero agregamos shilt para mover ventana
agregamos esto
![[Pasted image 20230604153300.png]]
de bajo de lo ultimo move floating windows
con una ventana alt +w arriba para ir resisando el tamaño de la ventana actual

![[Pasted image 20230604153826.png]]
agregamos la direccion del scripts con esto de la direeciones que luego creamos

luego creamo la carpeta scripts
![[Pasted image 20230604155545.png]]

luego 

lo que hacemos aca es crear el archivo y darle permiso de ejecucion

![[Pasted image 20230604155557.png]]
a su vez
usaremos un script este lo agregamos a ese archivo
#!/usr/bin/env dash

if bspc query -N -n focused.floating > /dev/null; then
	step=20
else
	step=100
fi

case "$1" in
	west) dir=right; falldir=left; x="-$step"; y=0;;
	east) dir=right; falldir=left; x="$step"; y=0;;
	north) dir=top; falldir=bottom; x=0; y="-$step";;
	south) dir=top; falldir=bottom; x=0; y="$step";;
esac

bspc node -z "$dir" "$x" "$y" || bspc node -z "$falldir" "$x" "$y"































