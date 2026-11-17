# Red para el servidor del hogar

Esta documentación hablará de la red en la que se encuentra el servidor en el que se ha trabajado, incluyento servicios, ubicación de archivos, funcionalidades y descripciones.
## Indice
* [1.- Servicios Disponibles](#1.)
* [2.- Políticas de Seguridad](#políticas-de-seguridad)
* [### 2.1- Política de autorización de admisión de hardware a la red](#)
* []()

## 1.- Servicios Disponibles

**1 - File browser:** Servicio de portal de archivos para videojuegos en formatos varios, con el objetivo de preservarlos para que allegados personales (de momento) puedan descargarlos y hacer uso de ellos libremente.

**2 - Next Cloud:** Servicio de portal alternativo. Cumple la función de _File Browser_, ofreciendo otras herramientas y haciendolo, ganaré experiencia para futuros empleos donde se use, puesto que es una herramienta amplaimente usada en empresas.

**3 - VSFTPD:** Servidor FTP por defecto de _Linux_, para envío de archivos via red, como podrán ser imagenes, videos, o juegos en formatos varios.

**4 - Syncthing:** Herramienta de sincronización continua de archivos que conecta directamente los dispositivos sin depender de servidores de terceros ni de servicios en la nube.

**5 - Caddy:** Servidor para host de páginas web y proxy inverso muy eficiente que destaca por su extrema facilidad de configuración. Su mayor atractivo para servidores domésticos es que solicita y renueva automáticamente los certificados SSL/TLS (HTTPS) de forma nativa para tus servicios.

**6 - Servicio RSS:** Servicio de portal de noticias en formato RSS para que los clientes del servidor obtengan información actualizada de avances y actualizaciones de dicho servidor. Además, se busca experimentar con el servicio RSS que poseen los sistemas PSP.

**7 - Cockpit:** Interfaz gráfica de red que permite administrar y monitorizar  el servidor desde cualquier navegador. Facilita el control del rendimiento, la gestión de almacenamiento, servicios (systemd), contenedores y la instalación de actualizaciones sin usar la terminal.

**8 - SearXNG:** Servicio de buscador de internet estilo _Google_, _Yahoo_ o _DuckduckGo_, cuyo objetivo es ofrecer un servicio privado, sin analisis de datos externos ni integraciones indeseadas.

**9 - Wireguard (VPN):** Protocolo VPN moderno, extremadamente rápido y ligero, integrado directamente en el kernel de Linux. Utiliza criptografía de vanguardia para crear túneles seguros entre redes o dispositivos, destacando por su alta velocidad y configuración simplificada.

**10 - Obsidian:** Potente base de conocimiento y toma de notas basada en archivos de texto plano (Markdown) guardados localmente. Puedes sincronizar su "bóveda" en tu servidor para gestionar documentación técnica o personal, interconectando ideas mediante enlaces bidireccionales y grafos visuales.

**11 - ARR Suite:** Suite de programas como _Radar_, _Sonar_ y más, que facilitarán la obtencion de material como juegos, música, cine y, en general, ocio multimedia; de manera automatizada.

**12 - Jellyfin:** Servicio de streaming de series, peliculas y música para uso personal, tal y como ofrecen plataformas como _Netflix_, _HBO_, _Deezer_ o _Spotify_ para ofrecer un servicio de la mejor calidad posible, gratuitamente, y sin limitaciones.

**13 - TeamSpeak 6:** Servicio de chat directo, mediante mensajes, audio y video, como alternativa a la plataforma _Discord_, para ofrecer un servicio personal y privado, sin analisis de datos externos.

**14 - PostgreSQL (extra):** Sistema gestor de base de datos estandar y de código abierto, con un rendimiento excelente. Esta herramienta será poco prioritaria, puesto que podria llevar demasiado tiempo desarrollarlo. Su creación será en ultima instancia, y si el tiempo lo permite.

**15 - Gemma AI (extra):** Familia de modelos de lenguaje de peso ligero y pesos abiertos desarrollados por Google. Al estar optimizados para eficiencia, se podrá alojar en el servidor (mediante Ollama, por ejemplo) para tener un asistente de IA privado que no envíe tus datos a la nube.

```
                  [ USUARIOS / AMIGOS / INTERNET ]
                                 │
                                 ▼
                     [ Wireguard (VPN / Acceso) ]
                                 │
                                 ▼
                   [ Caddy (Proxy Inverso + SSL) ]
                                 │
     ┌───────────────────────────┼───────────────────────────┐
     ▼                           ▼                           ▼
[ Almacenamiento ]       [ Entretenimiento ]       [ Gestión e IA ]
 ├─ File Browser          ├─ Jellyfin               ├─ Cockpit
 ├─ VSFTPD (Retro)        ├─ ARR Suite (Radarr...)  ├─ SearXNG
 ├─ Syncthing             └─ Servicio RSS           ├─ TeamSpeak 6
 └─ Obsidian (Notas)                                ├─ Ollama / Gemma AI
                                                    └─ PostgreSQL (BD)
```

## 2.- Políticas de Seguridad
Este ecosistema cuenta con una serie de políticas de seguridad, garantizando robustez en este aspecto. Las politicas son:

### 2.1- Política de autorización de admisión de hardware a la red

Todo hardware, sea independiente (ordenadores, moviles, consolas, televisores...) o sean periféricos con riesgo (pendrives, ) solo podra entrar al ecosistema o ser conectado a algun elemento del mismo, debe tener autorización previa del administrador para ser conectado a la red. En caso de no estar disponible el administrador, no se podra hacer ninguna modificación.

### 2.2.- Política de Autenticación

Todo archivo, sistema o dispositivo sensible o con riesgo, necesitará autenticación para su modificación y/o manipulación.

### 2.3.- Política de Contraseñas

Las contraseñas, para tener una seguridad robusta y potente, deberán cambiarse una vez cada 6 meses. Además, presentarán una estrategia nemotécnica para asegurar un tamaño interesante y una variedad de caracteres desafiante.

1. Escoger canción
    * Se escogerá una canción al gusto, de un artista no usado previamente, y cuanto más underground, mejor.
    * Cutthroat carnival, de Lorne Balfe
2. Dar Formato
    * A dicha canción, se le dará un formato sencillo.
    * cutthroat carnival - lorne balfe
3. Sustitución de vocales
    * Se cambiarán todas las vocales por un número concreto, como cuando se utilizaban redes sociales como _Tuenti_ o _Messenger_
        *   A = 4
        *   E = 3
        *   I = 1
        *   O = 0
        *   U = 2
    *  c2tthr04t c4rn1v4l - l0rn3 b4lf3
4. Sustitución de espacios por ";"
    * Puesto que las listas de contraseñas de los softwares de fuerza bruta separan sus opciones comunmente con ";", escoger esta como la opcion de caracter especial es muy buena idea, puesto que contar en estas listas caracteres así, es mas complicado. Lo que se hará es sustituir los espacios por este símbolo, suprimiendo el guión y uno de los espaciós circundantes.
    *  c2tthr04t;c4rn1v4l;l0rn3;b4lf3
5. Mayusculas
    * Se le darán mayúsculas a la primera palabra del nombre de la canción y del artista.
    *  C2tthr04t;c4rn1v4l;L0rn3;b4lf3
6. Supresión de nombre de autor
    * Por último, para facilitar su memorización, se le suprimirán todas las palabras posteriores al primer nombre que tenga el artista.
    *  C2tthr04t;c4rn1v4l;L0rn3

### 3.3.- Política de plan de contingencia

## 3.- Subred de router "welcome\_to\_the\_cumzone"

Esta es una subred de la red principal.

**Sesión de adminsitración del router**

* Nombre de usuario - big\_boss
* Contraseña - Sh0w;4d0

**Configuración red 2.4G**

* Nombre de red - "Welcome\_to\_the\_cumzone_2.4G"
* Seguridad - WPA3-Personal+WPA2-PSK[AES]
* Contraseña -  Z4z2,ch2ch3
* Banda - 2.4GHz
* OFDMA
* TWT

**Configuración red 5G**

* Nombre de red - "Welcome\_to\_the\_cumzone_5G"
* Seguridad - WPA3-Personal+WPA2-PSK[AES]
* Contraseña -  Z4z2,ch2ch3
* Banda - 5GHz
* OFDMA
* TWT

**Configuración red invitados**

* Nombre de red - "Welcome\_to\_the\_cumzone_Guests"
* Seguridad - WPA2/WPA3-Personal
* Contraseña -  Apple esta sobrevalorado
* Banda - 2.4GHz

**Configuración red IoT**

* Nombre de red - "Welcome\_to\_the\_cumzone_IoT"
* Seguridad - WPA2/WPA3-Personal
* Contraseña -  Z4z2,ch2ch3
* Banda - 2.4GHz

**Configuración DHCP**

* Rango de IPs - 192.168.0.100 - 192.168.0.150
* Máscara de subred - 255.255.255.0 (CIDR - 24)
* Tiempo de concesión - 1440 minutos (24h)
* Puerta de enlace - 192.168.0.1
* Dominio  - cumzone.local

**IPs estáticas / reservadas**

| Puesto | IP | Dispositivo | Dirección MAC | Tipo de IP|
| --- | --- | --- | --- | --- |
| 1 | 192.168.0.1 | Router principal | B0:BE:76:8E:50:BC | IP Fija |
| 2 | 192.168.0.2 | Router Retrocompatibilidad | 1a:1b:1c:1d:1e:1f | IP Fija |
| 3 | 192.168.0.103 | Servidor | 30:9C:23:0E:AC:4A | IP Fija |
| 4 | 192.168.0.104 | PC principal | 34:5A:60:3E:80:A3 | IP Fija |
| 5 | 192.168.0.105 | Televisor | 1C:5A:6B:FB:F5:01 | IP Fija |
| 6 | 192.168.0.106 | Televisor Maca | D4:AB:CD:FE:38:BB | IP Fija |
| 7 | 192.168.0.107 | Televisor Mama | E8:F2:E2:8A:14:00 | IP Fija |
| 8 | 192.168.0.108 | Aspiradora | 2a:2b:2c:2d:2e:2f | IP Fija |
| 9 | 192.168.0.109 | Alexa Xabel | A0:D2:B1:7C:AA:98 | IP Fija |
| 10 | 192.168.0.110 | Alexa Maca | B4:E4:54:A3:F8:D3 | IP Fija |
| 11 | 192.168.0.111 | Alexa Mama | B0:F7:C4:9F:B7:01 | IP Fija |
| 12 | 192.168.0.112 | Luz Xabel | 3a:3b:3c:3d:3e:3f | IP Fija |
| 13 | 192.168.0.113 | Luz Maca | 4a:4b:4c:4d:4e:4f | IP Fija |
| 14 | 192.168.0.114 | Lámpara Mama | 5a:5b:5c:5d:5e:5f | IP Fija |
| 15 | 192.168.0.115 | PlayStation 2 Fat | 6a:6b:6c:6d:6e:6f | IP Fija |
| 16 | 192.168.0.116 | PlayStation 3 Slim | 28:0D:FC:DC:43:9B | IP Fija |
| 17 | 192.168.0.117 | PlayStation 4 | F8:46:1C:F8:73:9B | IP Fija |
| 18 | 192.168.0.118 | Nintendo Wii | 78:a2:a0:14:69:48 | IP Reservada |
| 19 | 192.168.0.119 | Nintendo Wii U | 7a:7b:7c:7d:7e:7f | IP Reservada |
| 20 | 192.168.0.120 | Portátil | 8C:C8:4B:F7:3E:37 | IP Reservada |
| 21 | 192.168.0.121 | Teléfono Xabel | 48:EF:1C:02:FA:5B | IP Reservada |
| 22 | 192.168.0.122 | Teléfono Maca | EA:F2:64:8C:3C:0F | IP Reservada |
| 23 | 192.168.0.123 | Tablet Huawei | A0:D8:07:28:45:12 | IP Reservada |
| 24 | 192.168.0.124 | PlayStation Vita Fat | D4:4B:5E:87:B7:9C | IP Reservada |
| 25 | 192.168.0.125 | Nintendo DSi XL | A4:5C:27:47:21:51 | IP Reservada |
| 26 | 192.168.0.126 | Nintendo 3DS | 2C:10:C1:05:88:07 | IP Reservada |
| 27 | 192.168.0.201 | Máquina TeamSpeak (Debian Server 13) | BC:24:11:C3:AD:9A | IP Fija |
| 28 | 192.168.0.201 | Julia (Máquina Web-Services) | BC:24:11:28:3C:55 | IP Fija |

**Puertos abiertos:**

* *Datos TeamSpeak 6:*
* Puerto de servicio -  30033
* Dirección IP - 192.168.0.4
* Puerto Interno - 30033
* Protocolo - TCP

* *Voz TeamSpeak 6:*
* Puerto de servicio - 9987
* Dirección IP - 192.168.0.4
* Puerto Interno - 9987
* Protocolo - UDP

## Virtualización ProxMox

Este sistema es un SO de virtualización de tipo 1, donde tendremos las máquinas con los servicios, en vez de directas en el servidor.
Más información de documentación en la [ve.Proxmox.com](https://pve.proxmox.com/pve-docs/)

**Sesión**

* Usuario administrador - root
* Contraseña administrador - Sn4k3;34t3r;Cynth14

## Máquina Debian Server 13:

En esta máquina estarán corriendo la inmensa mayoría de servicios.

**Sesión**

* Usuario administrador - root
* Contraseña administrador - Sn4k3;34t3r;Cynth14
* Usuario cliente - mondo-ds13
* Contraseña cliente - 1Trixie3

**Servicios:**  
*Team Speak 6:*  
Este es un servicio que permite el uso del programa TeamSpeak 6, utilizando como host el servidor en el que está instalado dicho servicio, ofreciendo la posibilidad de estar en chats de voz y mensajes con múltiples funciones.

Código de recuperación de usuario de TeamSpeak 6 - Ns6OLFh/4kpqyUr98AKcLmejAJdnT79wrxBozmJTjQ0=  
Código token de Teamspeak6 admin - 0xAt0AVRkc4Z59+V66uWfjFJ1na3oC7CxaZoxRN0

* Ruta de los archivos - /opt/teamspeak6
* Usuario de servicio - teamspeak:teamspeak
* Datos del usuario - /opt/teamspeak6/users

## CT (Container Tool) Web-Services

En esta máquina estarán corriendo los servicios web como el buscador SearXNG o la pagina web

**Datos**
* CT ID - 101
* Hostname - Julia
* unprivileged container - *Si*
* Nesting - *Si*
* Usuario administrador - root
* Contraseña administrador - G1mm13;6;D33W2nn


### Servicios de la máquina Web-Serices

#### SearXNG
SearXNG es un navegador de codigo abierto y privado para substituir Google o DuckduckGo

#### phpMyAdmin
phpMyAdmin es un sistema de bases de datos relacional basado en mysql y php
Usuario: usumariadb
Contraseña: b3A8m9b3A8m9

## 4.- Detalles extra

Para subir datos a GitHub desde Git de esta documentación:
$ git status
$ git add . <"." para cuando se hace en la terminal de visual studio, si es en otra a parte, pon el nombre del archivo>
$ git commit -m "<mensaje de interés>"
