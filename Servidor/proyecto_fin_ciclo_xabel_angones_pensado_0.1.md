# Proyecto de Fin de Ciclo

**Creado por:** Xabel Angones Pensado  
**Título:** Creación de una red y un servidor domésticos  
**Versión:** 0.1  

---

## 1. Índice

1. [Índice](#1-índice)
2. [Introducción](#2-introducción)
3. [Seguridad](#3-seguridad)
4. [Administración del Router](#4-administración-del-router)
5. [Servidor](#5-servidor)
   - [5.1 Servicios Disponibles](#51-servicios-disponibles)

---

## 2. Introducción

Este proyecto consistirá, en primer lugar, en montar una **red doméstica y privada** con múltiples dispositivos conectados para dar un servicio de conectividad potente y multifunción en mi entorno personal (es decir, mi habitación y las estancias colindantes de mi familia). 

Contará con una herramienta principal que constituirá el pilar más importante de todo el proyecto: el **servidor personal**.

---

## 3. Seguridad

Este ecosistema contará con una serie de políticas de seguridad, de uso de contraseñas, de protocolos de emergencia por si suceden ataques, prevenciones varias, copias de seguridad y, en definitiva, un compendio de *medidas integrales diseñadas para salvaguardar la confidencialidad, integridad y disponibilidad de la información, garantizando así la continuidad operativa ante cualquier amenaza*.

---

## 4. Administración del Router

Este punto tendrá gran importancia, puesto que es donde se gestionarán los aspectos más críticos:

* **Conexión entre sistemas:** Gestión de direccionamiento e IP mediante el protocolo *DHCP*.
* **Seguridad integral:** Control del perímetro de la red, al ser la puerta de entrada directa desde el exterior ante eventuales amenazas de *malware*.

---

## 5. Servidor

El servidor será, con diferencia, el punto más denso del proyecto, ya que en él se alojarán (*hostearán*) todos los servicios para la red, lo que requerirá considerable trabajo, esfuerzo y configuración.

### 5.1 Servicios Disponibles

Los servicios inicialmente planteados para el servidor son los siguientes:

1. **SearXNG:** Servicio de motor de búsqueda de Internet estilo *Google*, *Yahoo* o *DuckDuckGo*, cuyo objetivo es ofrecer búsquedas privadas, sin análisis de datos externos ni integraciones indeseadas.
2. **TeamSpeak 6:** Servicio de chat directo mediante mensajes, audio y vídeo. Se plantea como alternativa a la plataforma *Discord* para ofrecer un servicio personal y privado sin recopilación de datos por terceros.
3. **Servicio RSS:** Portal de noticias en formato RSS para que los clientes obtengan información actualizada sobre avances y cambios en el servidor.
   * *Nota experimental:* Se busca explorar el servicio RSS nativo presente en consolas *PSP*.
4. **File Browser:** Portal web de archivos orientado a videojuegos en diversos formatos, enfocado en la preservación digital para que allegados puedan descargarlos y hacer uso de ellos libremente.
5. **Jellyfin:** Plataforma de *streaming* de series, películas y música para uso personal (similar a *Netflix*, *HBO*, *Deezer* o *Spotify*) que ofrece máxima calidad, de forma gratuita y sin limitaciones.
6. **ARR Suite:** Conjunto de aplicaciones automáticas (como *Radarr*, *Sonarr*, entre otras) que facilitan la obtención y organización autónoma de material multimedia (juegos, música, cine, etc.).
7. **WireGuard:** Protocolo VPN moderno, extremadamente rápido y ligero, integrado directamente en el kernel de Linux para acceso remoto seguro.
8. **Caddy:** Servidor web y proxy inverso de alto rendimiento que destaca por su facilidad de configuración y gestión automática de certificados SSL/TLS (HTTPS).
9. **Obsidian:** Potente base de conocimiento y gestión de notas basada en archivos de texto plano (*Markdown*) guardados localmente para su posterior interconexión con otros sistemas.
10. **Cockpit:** Interfaz gráfica web para la administración, monitorización de recursos y mantenimiento del servidor directamente desde cualquier navegador.
11. **PostgreSQL *(Módulo extra)*:** Sistema gestor de bases de datos relacional estándar y de código abierto, con un rendimiento excelente. *Prioridad secundaria*: su implementación se realizará en última instancia si la disponibilidad de tiempo lo permite.
12. **Gemma AI *(Módulo extra)*:** Familia de modelos de lenguaje ligeros y de código abierto desarrollados por Google. *Prioridad secundaria*: debido a los recursos limitados del servidor, su uso intensivo de *tokens* podría impactar el rendimiento general del sistema.
