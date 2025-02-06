 ## LABORATORIO 7 - PHP

 ### Actividad 1

- Propósito de los comentarios (#) en httpd.conf:
    - Los comentarios explican las configuraciones sin afectar el funcionamiento del servidor. También se utilizan para desactivar líneas de configuración sin eliminarlas.

- Valores por defecto de ServerName y DocumentRoot:

    - ServerName define el nombre del servidor (ejemplo: localhost). DocumentRoot es la ruta donde se almacenan los archivos web, generalmente /var/www/html.

- Efecto de Include /etc/httpd/mod_php.conf:

    - Permite la carga del módulo PHP en Apache, permitiendo la ejecución de scripts PHP.

### Actividad 2

- Por qué reiniciar httpd tras cambios en la configuración:
    - Apache debe recargar los archivos de configuración para aplicar cambios.

- Análisis del comando ps aux | grep httpd:

    - ps aux muestra procesos en ejecución. grep httpd filtra los procesos relacionados con Apache. | es un operador de pipe que pasa la salida de un comando como entrada de otro.

- Salida esperada de ps aux | grep httpd:

    - Si httpd está corriendo, se listarán varios procesos de Apache.
    - Si no está corriendo, solo se mostrará la línea de grep httpd.


### Actividad 3

- ¿Qué tiene de especial index.html?
    - Es la página por defecto que carga Apache si no se especifica otra.

![]()

![]()

### Actividad 4

- Diferencia entre CLI y GUI
    - CLI usa comandos en texto, GUI tiene una interfaz gráfica.

- ¿Qué tiene de especial 127.0.0.1?
    - Es la dirección local del sistema (localhost).

![]()

### Actividad 5

- Función de phpinfo():

    - Muestra información de PHP, módulos instalados y configuración.

![]()

![]()

### Actividad 6

![]()

![]()