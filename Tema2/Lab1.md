# IES Luis Braille

## ASIR2 

## IAW

<span class="header-section-number">1</span> Práctica 1: Instalación de la pila LAMP en una máquina virtual
===========================================================================================================

Crea una máquina virtual en [VirtualBox](https://www.virtualbox.org) con la última versión de [Ubuntu Server](https://www.ubuntu.com/server).
Instala todos los paquetes necesarios para tener una [pila LAMP](https://es.wikipedia.org/wiki/LAMP) en tu máquina virtual.

Una vez que hayas comprobado que todos los servicios de la [pila LAMP](https://es.wikipedia.org/wiki/LAMP) están funcionando
correctamente, instala y configura la aplicación web propuesta.

Crea un **script de Bash** con todos los pasos que has realizado, de manera que te permita automatizar el proceso de instalación y
configuración de la pila LAMP.

<span class="header-section-number">1.1</span> Repositorio del proyecto de ejemplo
----------------------------------------------------------------------------------

-   https://github.com/IESLuisBraille/iaw_asir2/blob/master/Tema2/LAMP_Stack.md

<span class="header-section-number">1.2</span> Arquitectura de red con un único servidor
----------------------------------------------------------------------------------------

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAATMAAAC4CAMAAAC4hvvDAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAA3NpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuNS1jMDIxIDc5LjE1NDkxMSwgMjAxMy8xMC8yOS0xMTo0NzoxNiAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wTU09Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9tbS8iIHhtbG5zOnN0UmVmPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvc1R5cGUvUmVzb3VyY2VSZWYjIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtcE1NOk9yaWdpbmFsRG9jdW1lbnRJRD0ieG1wLmRpZDpkOWJiZmQ5Ni03NzUwLTRlMTItYTA2OC0wOWFjMGIzZjA3ZjQiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6RjFCQzE2RkVFMDJFMTFFM0FFREFGREFBRDYzMkJDMTUiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6RjFCQzE2RkRFMDJFMTFFM0FFREFGREFBRDYzMkJDMTUiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENDIChNYWNpbnRvc2gpIj4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6YjEyZjZiYzEtZDZmYS00MTRiLWI3YTAtNTU4NGQ2NWFmNDU1IiBzdFJlZjpkb2N1bWVudElEPSJ4bXAuZGlkOmQ5YmJmZDk2LTc3NTAtNGUxMi1hMDY4LTA5YWMwYjNmMDdmNCIvPiA8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)

**Ventajas:**

-   Es una solución sencilla de implementar ya que sólo tenemos un único servidor.
-   Puede ser útil para aplicaciones que van a tener poca carga de trabajo.

**Inconvenientes:**

-   Esta solución puede provocar problemas de rendimiento ante una carga de trabajo elevada, ya que todos los servicios se están ejecutando
    sobre la misma máquina y tienen que competir por los mismo recursos.
-   Al estar todos los servicios ejecutándose sobre la misma máquina, no va a ser posible escalar nuestro sistema horizontalmente, es decir,
    añadiendo más nodos al sistema para repartir la carga. En este caso habrá que escalar verticalmente, añadiendo más recursos sobre la
    máquina donde están todos los servicios.

<span class="header-section-number">1.3</span> Entregables
----------------------------------------------------------

En esta práctica habrá que entregar un **documento técnico** con la descripción de los pasos que se han llevado a cabo.

El documento debe incluir **como mínimo** lo siguientes contenidos:

-   URL del repositorio de GitHub donde se ha alojado el documento técnico escrito en
    [Markdown](https://es.wikipedia.org/wiki/Markdown).
    
-   Descripción de la instalación de [Apache HTTP Server](https://httpd.apache.org), [PHP](http://www.php.net), [MySQL Server](https://www.mysql.com),
    [phpMyAdmin](https://www.phpmyadmin.net) en Ubuntu Server 20.04.
    
-   Descripción de la instalación de la [aplicación web propuesta](https://github.com/josejuansanchez/iaw-practica-lamp).
    
-   Descripción de la instalación de [Adminer](https://www.adminer.org).

-   Instalación del analizador de logs [GoAccess](https://goaccess.io) para Apache Server.
    
-   [Control de acceso a un directorio con `.htaccess`](https://httpd.apache.org/docs/trunk/es/howto/htaccess.html).
    
-   Script de Bash con la automatización del proceso de instalación y configuración.

Como **actividad de ampliación** se propone:

-   Instalación del analizador de logs [AWStats](https://awstats.sourceforge.io) para Apache Server.



<span class="header-section-number">2</span> Referencias
========================================================

-   [VirtualBox](https://www.virtualbox.org)
-   [Ubuntu Server](https://www.ubuntu.com/server)
-   [LAMP Stack](https://es.wikipedia.org/wiki/LAMP)
-   [PHP](http://www.php.net)
-   [Apache HTTP Server](https://httpd.apache.org)
-   [MySQL Server](https://www.mysql.com)
-   [Configuraciones comunes para aplicaciones
    web](https://www.digitalocean.com/community/tutorials/5-configuraciones-comunes-para-tus-aplicaciones-web-es)
-   [Markdown](https://es.wikipedia.org/wiki/Markdown)
-   [PHPMyAdmin](https://www.phpmyadmin.net)
-   [Adminer](https://www.adminer.org)
-   [GoAccess](https://goaccess.io)
-   [AWStats](https://awstats.sourceforge.io)
-   [Tutorial del Servidor Apache HTTP: Ficheros
    `.htaccess`](https://httpd.apache.org/docs/trunk/es/howto/htaccess.html)

<span class="header-section-number">4</span> Licencia
=====================================================

[![Licencia de Creative
Commons](data:image/png;base64,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)](http://creativecommons.org/licenses/by-nc-sa/4.0/)  

