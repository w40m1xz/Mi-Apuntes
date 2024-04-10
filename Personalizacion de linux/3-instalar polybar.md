Por aquí os comparto el primer comando que introducimos al empezar la clase, necesario para instalar una serie de dependencias previas a la instalación de la Polybar:

- **apt install cmake cmake-data pkg-config python3-sphinx libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev libxcb-xkb-dev libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev libjsoncpp-dev libmpdclient-dev libuv1-dev libnl-genl-3-dev**

**IMPORTANTE**: En caso de que os de problemas el paquete ‘**python3-sphinx**‘, simplemente quitadlo del comando anterior. Primero probadlo con el paquete ‘**python3-sphinx**‘ incluido, quitadlo sólo si os da problemas.

Posteriormente, debéis clonar en vuestra carpeta de descargas el repositorio de la polybar:

esto se hace e
- git clone --recursive https://github.com/polybar/polybar
- [Son 2 guiones donde pone ‘**recursive**‘]

Una vez hecho, os tenéis que meter en la carpeta creada resultante de haber clonado previamente el repositorio y ejecutar los siguientes comandos:
dentro de la carpeta polybar
- **mkdir build**
- **cd build**
en la misma carpeta hacemos esto
- **cmake ..**
- **make -j$(nproc)**
- **sudo make install**

Recordad que otra forma de instalar la polybar de manera más sencilla, es haciendo un ‘**apt install polybar**‘, pero recomendamos esta forma que mostramos con el objetivo de asegurar que la Polybar esté en su última versión.

Con esto, ¡ya deberíais tener la polybar instalada!


si esto te da problema puedes hacer esto


![[Pasted image 20230604163520.png]]

pero la otra version es mejor porque esta mas actualizada po  porq lo toma del mismo github

es mil veces mejor la forma anterior si
