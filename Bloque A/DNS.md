# DNS

### ¿ Que es el DNS ? :
 El Sistema de Nombres de Dominio (DNS) es un componente fundamental del protocolo estándar de Internet, responsable de convertir los nombres de dominio de uso humano en direcciones del protocolo de Internet (IP) que los ordenadores utilizan para identificarse entre sí en la red.


### Resolucion :
 La resolución de nombres de dominio (DNS) es el proceso mediante el cual se traduce un nombre de dominio (como brave.com) a una dirección IP (como 192.0.2.1) que las máquinas pueden entender. Este proceso es esencial para acceder a sitios web, servicios en línea y otros recursos en Internet.


### Nombre de dominios : 
El sistema de nombres de dominio (DNS) utiliza varios tipos de registros para almacenar y gestionar la información de los nombres de dominio. A continuación, se presentan algunos de los registros más comunes:

A: Dirección (address). Se utiliza para traducir nombres de servidores de alojamiento a direcciones IPv4.

AAAA: Dirección (address). Se utiliza en IPv6 para traducir nombres de hosts a direcciones IPv6.

CNAME: Nombre canónico (canonical Name). Se utiliza para crear nombres de servidores de alojamiento adicionales, o alias, para los servidores de alojamiento de un dominio.

NS: Servidor de nombres (name server). Define la asociación que existe entre un nombre de dominio y los servidores de nombres que almacenan la información de dicho dominio.

MX: Intercambio de correo (mail exchange). Asocia un nombre de dominio a una lista de servidores de intercambio de correo para ese dominio.

PTR: Indicador (pointer). También conocido como “registro inverso”, funciona a la inversa del registro A, traduciendo IPs en nombres de dominio.

SOA: Autoridad de la zona (start of authority). Proporciona información sobre el servidor DNS primario de la zona.

SRV: Service record (SRV record). Se utiliza para especificar los servidores que ofrecen un servicio específico, como el servicio de correo electrónico.

ANY: Toda la información de todos los tipos que exista. (No es un tipo de registro, sino un tipo de consulta).

### Niveles de dominios :
El sistema de nombres de dominio (DNS) utiliza una estructura jerárquica para organizar los dominios y subdominios. Los niveles de dominio se clasifican en:

Nivel raíz (Root): Representado por un punto (.), es el nivel más alto y se considera el “comienzo” de la jerarquía.

Dominios de nivel superior (TLD, Top-Level Domain): Estos dominios se encuentran directamente debajo del nivel raíz y son gestionados por organizaciones como ICANN (Internet Corporation for Assigned Names and Numbers). Ejemplos de TLD incluyen .com, .org, .net, .es, .ar, etc.

Dominios de segundo nivel (SLD, Second-Level Domain): Estos dominios se encuentran debajo de los TLD y son gestionados por los propietarios de los dominios de nivel superior. Ejemplos de SLD incluyen example.com, hispanolinux.es, ccm.net, etc.

Subdominios: Estos son dominios que se encuentran debajo de los dominios de segundo nivel y se utilizan para crear subsecciones o secciones específicas dentro de un dominio. Ejemplos de subdominios incluyen www.example.com, blog.example.com, store.example.com, etc.


### Zonas de busqueda :
Una zona DNS (Domain Name System) es una subdivisión administrativa del espacio de nombres DNS, gestionada por una organización específica o un administrador. Esta zona incluye al menos un dominio y, si existen, otros subdominios. La zona DNS es una unidad administrativa y no debe confundirse con el concepto de dominio ni con un servidor de nombres específico.

La zona DNS contiene registros de recursos, como direcciones IP, servidores de nombres autoritativos y otros datos relacionados con el dominio. El archivo de zona DNS es la base técnica para almacenar esta información y se almacena en el sistema de archivos de un servidor. La estructura de un archivo de zona DNS se define en el documento RFC 1035.

### Tipos de servidores :
Los servidores DNS (Domain Name System) son fundamentales para traducir direcciones web (nombres de dominio) a direcciones IP. A continuación, se presentan los diferentes tipos de servidores DNS:

Servidores raíz (Root Servers): Estos servidores están autorizados para el dominio raíz “.” y son responsables de dirigir las consultas a los servidores TLD (Top-Level Domains).

Servidores TLD (Top-Level Domains): Estos servidores gestionan los dominios de nivel superior, como “.com”, “.org”, “.es”, etc.

Servidores autoritarios (Authoritative Servers): Estos servidores albergan la información de zona para un dominio específico y son responsables de responder a consultas sobre ese dominio.

Servidores secundarios (Secondary Servers): Estos servidores copian la información de zona de un servidor autoritario y pueden responder a consultas en caso de que el servidor autoritario no esté disponible.

Servidores caché (Cache Servers): Estos servidores almacenan las respuestas a consultas recientes para acelerar la resolución de nombres y reducir el tráfico en la red.

Servidores reenviadores (Forwarders): Estos servidores reenvían consultas a otros servidores DNS en lugar de intentar resolverlas ellos mismos.

Servidores locales (Local Servers): Estos servidores DNS se encuentran en la red local y se utilizan para resolver nombres de dominio dentro de la red.

### Resgistros :
Los registros DNS (o registros del Sistema de Nombres de Dominio) son los datos que se almacenan en la base de datos de un dominio y definen cómo se aloja el sitio web y qué se puede acceder en él

### Funcionamiento :
Consulta inicial: Cuando un usuario escribe un nombre de dominio en el navegador web, el sistema de resolución de DNS comienza a buscar la dirección IP correspondiente.

Servidor recursivo: El navegador web envía la consulta al servidor recursivo de DNS designado por el proveedor de servicios de Internet (ISP). El servidor recursivo tiene una caché de direcciones IP para nombres de dominio ya consultados anteriormente.

Servidor de nombres raíz: Si el servidor recursivo no tiene la respuesta en su caché, consulta el servidor de nombres raíz (Root DNS). El servidor de nombres raíz es el punto de partida para todas las consultas de DNS y conoce la jerarquía de dominios y servidores de nombres autorizados.

Servidores de nombres de primer nivel (TLD): El servidor de nombres raíz responde con la dirección del servidor de nombres de primer nivel (TLD) correspondiente al dominio consultado (por ejemplo, .com, .org, etc.).

Servidores de nombres autorizados: El servidor de nombres TLD proporciona la dirección del servidor de nombres autorizado para el dominio consultado (por ejemplo, los servidores de nombres de get.tech).

Registro de zona: El servidor de nombres autorizado almacena los registros DNS para el dominio consultado en un archivo de zona. Estos registros incluyen la dirección IP del servidor web, entre otros.

Registro A: El servidor recursivo obtiene el registro A (dirección IP) del servidor de nombres autorizado y lo almacena en su caché local.

Respuesta final: El servidor recursivo envía la respuesta con la dirección IP al navegador web, que luego conecta con el servidor web correspondiente.

#### DNS recursivo : 
Un servidor DNS recursivo es un intermediario entre los clientes y los servidores DNS que contienen la información verdadera que relaciona los nombres de dominio con una o varias direcciones IP. Su función es resolver consultas DNS no resueltas por sí mismo, consultando a otros servidores DNS en una búsqueda recursiva.

#### DNS iterativo :
El DNS iterativo es un tipo de consulta DNS en la que el cliente DNS se comunica directamente con cada servidor DNS implicado en la búsqueda de una dirección IP, hasta que se obtiene la respuesta final. En este proceso, el cliente DNS no delega la búsqueda a otro servidor, sino que sigue consultando a cada servidor DNS hasta que se encuentra la información solicitada.