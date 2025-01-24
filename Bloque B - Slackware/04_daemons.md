## LABORATORIO 4 - DAEMONS

#### Ejercicio 4.1

![](https://github.com/rbuegar/Despliegue/blob/master/Bloque%20B%20-%20Slackware/Imagenes2/LAB4%20F1.jpg?raw=true)

    -- Explicacion de los procesos:

    - kworker/0:0-events: Hilo del kernel que maneja eventos relacionados con hardware.
    - init: Proceso de inicialización principal del sistema que gestiona la carga de servicios en el arranque.
    - containerd: Demonio encargado de gestionar contenedores en el sistema.
    - dockerd: Demonio del Docker que administra contenedores, imágenes y redes.
    - systemd-journald: Servicio de systemd que gestiona los logs del sistema.
    - dbus-daemon: Sistema de mensajería que permite la comunicación entre procesos en el sistema.
    - rcu_preempt: Hilo del kernel que optimiza la sincronización de lectura-copia-actualización (RCU).
    - kworker/0:1H-kblockd: Hilo del kernel que gestiona operaciones de entrada/salida en bloque.
    - systemd: Servicio de inicialización y gestión de procesos del sistema.
    - systemd-timesyncd: Servicio encargado de sincronizar el reloj del sistema con servidores de tiempo en la red.


#### Ejercicio 4.2

![](https://github.com/rbuegar/Despliegue/blob/master/Bloque%20B%20-%20Slackware/Imagenes2/LAB4%20F2.jpg?raw=true)

#### Ejercicio 4.3

![](https://github.com/rbuegar/Despliegue/blob/master/Bloque%20B%20-%20Slackware/Imagenes2/LAB4%20F3.jpg?raw=true)   

#### Ejercicio 4.4

![](https://github.com/rbuegar/Despliegue/blob/master/Bloque%20B%20-%20Slackware/Imagenes2/LAB4%20F4.jpg?raw=true) 

![](https://github.com/rbuegar/Despliegue/blob/master/Bloque%20B%20-%20Slackware/Imagenes2/LAB4%20F4.2.jpg?raw=true) 

![](https://github.com/rbuegar/Despliegue/blob/master/Bloque%20B%20-%20Slackware/Imagenes2/LAB4%20F4.3.jpg?raw=true) 

![](https://github.com/rbuegar/Despliegue/blob/master/Bloque%20B%20-%20Slackware/Imagenes2/LAB4%20F4.4.jpg?raw=true) 


- What is sftp and ssh? Why is the use of telnet discouraged in the “real world”?

SFTP (Secure File Transfer Protocol) es un protocolo que permite transferir archivos de manera segura entre sistemas mediante una conexión cifrada, utilizando el protocolo SSH para proteger los datos.

SSH (Secure Shell) es un protocolo de red que permite acceder de forma segura a otro sistema mediante una conexión cifrada, proporcionando funciones de administración remota, ejecución de comandos y transferencia de archivos.

El uso de Telnet está desaconsejado en el "mundo real" porque no utiliza cifrado para las comunicaciones. Esto significa que toda la información, incluidas contraseñas y datos sensibles, viaja en texto plano, lo que la hace vulnerable a ataques como la intercepción de datos por terceros (sniffing). En su lugar, se recomienda usar SSH, que garantiza la seguridad mediante cifrado.


