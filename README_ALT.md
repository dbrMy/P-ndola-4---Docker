**Repositorio del Grupo 4 de Píndolas M16 CIberseguridad **

Este contenedor ha sido diseñado para realizar un ataque básico, pero efectivo, al suministro de la cadena en contenedores Docker. A continuación se detallan sus características clave:

Ejecución del contenedor con comando malicioso:
El contenedor está configurado para ejecutar el comando echo "¡HAS SIDO HACKEADO!", lo que permite mostrar un mensaje intimidatorio al ejecutar el contenedor. Esto representa un ataque a los usuarios que descargan y ejecutan la imagen, sin saber que la imagen ha sido manipulada.

Modificación de una imagen base confiable (Alpine):
Se ha utilizado una imagen base popular y confiable (Alpine), que es comúnmente empleada por desarrolladores para aplicaciones ligeras. El uso de una imagen base conocida aumenta las probabilidades de que los usuarios confíen en la imagen maliciosa y la descarguen sin sospechas.

Distribución de la imagen modificada a través de Docker Hub:
La imagen ha sido subida a Docker Hub, lo que permite que cualquier usuario que descargue la imagen desde el repositorio público ejecute el contenedor malicioso. Esto refleja cómo un atacante puede manipular imágenes públicas y hacer que otros las descarguen, creyendo que son seguras.

La cadena de suministro se ve comprometida:
Al distribuir esta imagen modificada (aunque aparentemente inofensiva), se compromete la cadena de suministro de contenedores. Los desarrolladores o usuarios que confían en las imágenes de Docker Hub pueden descargar sin saber que han obtenido una imagen con un comando malicioso. Esto pone en evidencia los riesgos que existen cuando las imágenes de Docker no son verificadas adecuadamente, permitiendo que los atacantes distribuyan código malicioso que puede desencadenar otros tipos de ataques.

Exposición a riesgos de seguridad:
Este ataque es una forma simple pero efectiva de mostrar cómo un atacante puede manipular una imagen Docker e inyectar código malicioso. Aunque el ataque aquí es solo un mensaje intimidatorio, en un escenario real, este podría evolucionar para ejecutar comandos más peligrosos, robar información o permitir acceso remoto al sistema comprometido.

**DOCKER PULL **

docker pull niko2005/ngnxx:latest
