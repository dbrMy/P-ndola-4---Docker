# Pindola-4---Docker
Repositorio del Grupo 4 de Píndolas M16 CIberseguridad

- El contenedor se ejecuta como root, lo que permite más privilegios.
- Se instalan herramientas peligrosas (netcat, curl, wget), que facilitan ataques desde dentro del contenedor.
- Las credenciales están en variables de entorno, lo que las expone fácilmente (docker inspect).
- Se sirven archivos del sistema, permitiendo a cualquiera descargar /etc/passwd y /etc/shadow.
- Deslimita el tamaño en requests, lo que deja expuesto a ataques DoS.
- Exposición innecesaria de puertos como 22 (SSH) y 3306 (MySQL), facilitando ataques remotos.
