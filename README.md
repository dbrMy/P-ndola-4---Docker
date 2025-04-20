# Pindola-4---Docker
**Repositorio del Grupo 4 de Píndolas M16 CIberseguridad
**
- El contenedor se ejecuta como root, lo que permite más privilegios.
- Se instalan herramientas peligrosas (netcat, curl, wget), que facilitan ataques desde dentro del contenedor.
- Las credenciales están en variables de entorno, lo que las expone fácilmente (docker inspect).
- Se sirven archivos del sistema, permitiendo a cualquiera descargar /etc/passwd y /etc/shadow.
- Deslimita el tamaño en requests, lo que deja expuesto a ataques DoS.
- Exposición innecesaria de puertos como 22 (SSH) y 3306 (MySQL), facilitando ataques remotos.

**LINK repositorio DockerHub de nuestra imagen.** [https://hub.docker.com/repository/docker/a22brycanmar/ngnxx/general](url)

_docker pull a22brycanmar/ngnxx:latest_

**MEJORAS A IMPLEMENTAR
**
- Generar un servicio de nginx en un contenedor Docker para hacer un ataque en cadena.

- Modificarlo para que ejecute el ataque en cadena, por ejemplo, cambiando un carácter para que descargue el nuestro, como un alias, y que les salte un mensaje 
 diciendo que han sido hackeados. La descarga puede ser exactamente igual que el programa que queremos imitar, y que dé como resultado un mensaje “¡HAS SIDO 
 HACKEADO!”

- Crear y subir a github, con su readme, una imagen vulnerable

- Poner en este doc el enlace al repositorio de github

- En la máquina virtual crear un alias “fake docker pull”, que simule un docker pull, pero que saque la imagen de nuestro github.

# Píldoras
----------------------------------------------------------------------------------------------------

Este proyecto cuenta con 3 documentos cuales son; Teoric, Narratiu y Práctico. Cada uno de ellos contiene información sobre lo que tratará el proyecto en todo su conjunto.

----------------------------------------------------------------------------------------------------

**Teoric**:\
Contiene información sobre docker, que es docker (explicando un poco sobre su historia, funcionamiento y sus características), una pequeña guia de como usar docker con algunos comandos. También contiene información sobre DockerHub sobre que es el propio DockerHub y los beneficios de usar esa plataforma.
También se comenta una pequeña explicacion sobre las diferencias que puede haber entre una Maquina Virtual o MV y el propio docker seguido por un apartado que comenta porque es importante la seguridad en docker y un listado de posibles ataques que se pueden llegar a hacer.
Al final de todo hay una conclusión de los conocimientos aprendidos en este proyecto.

**Narratiu**:\
Este es un documento mucho mas breve que el Teoric que consiste en marcar una pauta paso a paso de como se va a exponer el proyecto de una manera ordenada y toda la información que se va a cubrir durante su propia presentación.

**Práctico**:\
Aquí esta documentado el motivo por el cual se ha escogido este tipo de atque, seguido por una guia paso a paso documentada de como hacer el ataque y mostrando su resultado final. Al final hay una explicacion con las diferentes vulnerabilidades que se consiguen haciendo el dicho ataque.

