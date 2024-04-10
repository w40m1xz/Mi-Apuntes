Recordad que en caso de que estéis teniendo problemas de red y no se os esté asignando dirección IP, podéis por un lado ejecutar estas instrucciones:

-   **ifconfig tuInterfaz up**
-   **ifconfig tuInterfaz ipDeseada netmask 255.255.255.0**
-   **route add default gw ipGateway**