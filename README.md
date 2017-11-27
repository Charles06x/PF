# Proyecto Final
Proyecto final del curso Cloud Computing

## Docker

En la carpeta "Docker" se encuentra el archivo "Dockerfile" que lanzará una imagen limpia del sistema operativo Ubuntu 16.04
y posteriormente realizará la instalación de python.

Para esto es necesario el uso de la siguiente linea de comando:

    docker build -t {{ name }} .

Esto, directamente desde la carpeta donde recide el archivo. {{ name }} es la etiqueta que usted desee colocar.

## Ansible

En esta carpeta, encontramos un archivo "inicial.yml", el cual realiza una configuración sobre el servidor llamado [web], que está en el archivo "hosts", este último debe ser enviado como inventario utilizando -i.

Realizando las actividades (tasks) del rol "Apache", se instalan los requerimientos para apache2 junto a este.

### NOTA:
Index.html es sólo una página HTML cambiante para realizar las pruebas.
Para la prueba es necesario copiar el archivo "Index.html" al contenedor usando el siguiente comando:
                                
     $ cp Index.html {{ container_ID }}:/Index.html 
Para conocer el ID del contenedor, deberá usar:
    
     $ docker container ls
