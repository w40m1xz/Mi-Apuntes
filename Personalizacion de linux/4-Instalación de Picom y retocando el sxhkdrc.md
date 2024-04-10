Por aquí tenéis todo el comando necesario a ejecutar para instalar ciertas dependencias previas:

- **apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev libpcre2-dev libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev**

Posteriormente, os descargáis el picom a través del siguiente comando ejecutado en la carpeta de descargas:

- **git clone https://github.com/ibhagwan/picom.git**

Una vez hecho, nos metemos en el directorio creado y ejecutamos los siguientes comandos:

- **git submodule update --init --recursive** 
- [Son 2 guiones donde pone ‘**init**‘ y ‘**recursive**‘]
- **meson --buildtype=release . build** 
- [Son 2 guiones donde pone ‘**buildtype**‘] 

OJOOOOOO!
(esto es para kali linux solamente sudo apt-get install libev-dev libpcre3-dev)
- **ninja -C build**
- **sudo ninja -C build install**

En esta clase también hemos instalado ‘**rofi**‘, lo hemos hecho mediante la ejecución del siguiente comando:

- **apt install rofi**

Con esto hecho, ya migramos a nuestro entorno ‘**bspwm**‘ y verificamos que todos los atajos estén funcionando correctamente.

con esta forma se lanza lofi

![[Pasted image 20230604164823.png]]

lo que podiramos hace copiar eso
y abrimo este archivo
![[Pasted image 20230604164856.png]]



y modificamos asi
![[Pasted image 20230604165149.png]]

agregamos el rofi en progam launcher

 ahora le damos apt install  bspwm

matamos la seccion kill -9 -1
probamos cosita

windows + t para resetea y volver a donde etsaba
windows + click izquierdo  para arrastra

windwos + click derecho para mover donde quiera

windows + f  full pero no se recomienda queda fep


dejamos para  cerrar con w +q 

no vamos a
![[Pasted image 20230604170248.png]]

y dejamos asi

![[Pasted image 20230604170355.png]]

y esto que es para resetear bspwm
![[Pasted image 20230604170506.png]]

probamos esto agregando firefox

![[Pasted image 20230604170645.png]]


vemos la ruta absoluta
![[Pasted image 20230604170701.png]]

y lo copias

![[Pasted image 20230604170815.png]]

guardamo ctrl s  luego ctrl x



























































