## Docker Supply Chain Attack Demo

Este repositorio contiene una práctica de seguridad enfocada en demostrar cómo un atacante puede comprometer la cadena de suministro de software a través de imágenes Docker manipuladas. El trabajo se divide en dos fases: un Proof of Concept (PoC) sencillo y un escenario avanzado con múltiples vulnerabilidades reales.

---

## Parte 1: Proof of Concept

Creamos una imagen personalizada basada en Alpine que simula un ataque a la cadena de suministro. La imagen, aparentemente inofensiva, simplemente muestra el mensaje `¡HAS SIDO HACKEADO!` al ejecutarse, imitando un caso de suplantación de imágenes comunes como `nginx`.

**Objetivo:** Comprender el funcionamiento básico de los Dockerfiles, cómo construir una imagen, subirla a Docker Hub y visualizar el impacto de un ataque simulado.

---

## Parte 2: Ejemplo Complejo

En esta segunda fase, construimos una imagen mucho más peligrosa basada en Nginx, añadiendo múltiples vulnerabilidades:

- Se ejecuta como **root**.
- Expone **credenciales sensibles** en variables de entorno.
- Abre **puertos innecesarios** (22, 3306).
- Instala herramientas como **curl**, **netcat** y **wget**.
- Sirve archivos del sistema como `/etc/passwd`.
- Desactiva configuraciones de seguridad en Nginx (`client_max_body_size`, etc).

**Objetivo:** Mostrar cómo una imagen aparentemente legítima puede volverse peligrosa al manipular su configuración y exponerla públicamente en Docker Hub.

---

## Tecnologías usadas

- Docker & Docker Hub
- Bash / CLI
- Nginx
- Alpine Linux
- GitHub

---

## Lecciones aprendidas

Durante esta práctica, comprendimos:

- Cómo construir y distribuir imágenes Docker personalizadas.
- Los riesgos de descargar imágenes desde fuentes no verificadas.
- El impacto de los ataques a la cadena de suministro de software.
- La importancia de aplicar **buenas prácticas** en el desarrollo con contenedores:
  - No ejecutar como root.
  - Revisar los `Dockerfile` antes de usarlos.
  - Utilizar imágenes oficiales o firmadas.
  - Escanear vulnerabilidades con herramientas como **Clair** o **Anchore**.
## Conclusión

Este proyecto nos permitió explorar de manera práctica cómo pueden explotarse los contenedores Docker cuando no se siguen medidas de seguridad adecuadas. Simulando ataques reales, comprendimos que la seguridad en la cadena de suministro no es opcional: es una responsabilidad crítica en el desarrollo moderno.
