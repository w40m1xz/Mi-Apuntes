En resumen, primeramente ejecutaremos el siguiente comando:

-   **apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev**

Posteriormente, aplicaremos una actualización del sistema con el comando ‘**apt update**‘. Acto seguido, tenéis que dirigiros a la carpeta de descargas de vuestro equipo y descargar los proyectos ‘**bswpm**‘ y ‘**sxhkd**‘ con los siguientes comandos:

-   **git clone https://github.com/baskerville/bspwm.git**
-   **git clone https://github.com/baskerville/sxhkd.git**
sxhkd -> atajo teclado
bspwm ->entorno

Para instalar cada uno de estos, lo que debéis hacer es meteros en ambos directorios por separado y ejecutar los comandos ‘**make**‘ y ‘**sudo make install**‘.

En caso de que os salga algún error relacionado con ‘**xinerama**‘, podéis ejecutar este comando:

-   **sudo apt install libxinerama1 libxinerama-dev**

Finalmente, instalaremos ‘**bspwm**‘ con el comando ‘**sudo apt install bspwm**‘. Este es un paso que se me olvida aplicar en esta clase, pero aún así lo hacemos más adelante. Mi recomendación es que lo hagáis ya para evitar problemas futuros.

¡Recordad que está prohibido hacer un ‘**apt upgrade**‘!