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
_docker push a22brycanmar/ngnxx:tagname_

**MEJORAS A IMPLEMENTAR
**
- Generar un servicio de nginx en un contenedor Docker para hacer un ataque en cadena.

- Modificarlo para que ejecute el ataque en cadena, por ejemplo, cambiando un carácter para que descargue el nuestro, como un alias, y que les salte un mensaje 
 diciendo que han sido hackeados. La descarga puede ser exactamente igual que el programa que queremos imitar, y que dé como resultado un mensaje “¡HAS SIDO 
 HACKEADO!”

- Crear y subir a github, con su readme, una imagen vulnerable

- Poner en este doc el enlace al repositorio de github

- En la máquina virtual crear un alias “fake docker pull”, que simule un docker pull, pero que saque la imagen de nuestro github.
