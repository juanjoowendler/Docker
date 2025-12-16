
# Docker 

---

## Recursos útiles

* Docker Hub: [https://hub.docker.com/](https://hub.docker.com/)
* Docker Samples (oficial): [https://docs.docker.com/reference/samples/](https://docs.docker.com/reference/samples/)
* Simple Deploy (DigitalOcean): [https://www.digitalocean.com/](https://www.digitalocean.com/)

---

## Conceptos clave

* **Imagen** : plantilla inmutable para crear contenedores.
* **Contenedor** : instancia en ejecución de una imagen.
* **Dockerfile** : archivo con instrucciones para construir una imagen.
* **Docker Compose** : herramienta para definir y correr aplicaciones con múltiples contenedores.
* **Volúmenes** : persistencia de datos fuera del ciclo de vida del contenedor.
* **Redes** : permiten la comunicación entre contenedores.

---

## Comandos más utilizados 

### Imágenes

* `docker build -t nombre:tag .` → Construir una imagen
* `docker images` / `docker image ls` → Listar imágenes
* `docker image rm imagen` → Eliminar imagen

### Contenedores

* `docker run nombre` → Crear y ejecutar contenedor
* `docker run -it nombre` → Ejecutar en modo interactivo
* `docker run -d -p 8080:80 nombre` → Ejecutar en segundo plano y mapear puertos
* `docker ps` → Contenedores en ejecución
* `docker ps -a` → Todos los contenedores
* `docker stop contenedor` → Detener contenedor
* `docker rm contenedor` → Eliminar contenedor
* `docker exec -it contenedor bash` → Entrar a un contenedor

### Limpieza rápida

* `docker container rm -f $(docker container ls -aq)` → Eliminar todos los contenedores
* `docker image rm $(docker image ls -q)` → Eliminar todas las imágenes

---

## Volúmenes y archivos

* `docker volume create nombre` → Crear volumen
* `docker volume inspect nombre` → Inspeccionar volumen
* `docker cp contenedor:/ruta/archivo .` → Copiar archivos desde un contenedor

---

## Docker Compose

Comandos más habituales:

* `docker compose up` → Levantar servicios
* `docker compose up -d` → Levantar en segundo plano
* `docker compose build` → Construir imágenes
* `docker compose ps` → Ver estado de servicios
* `docker compose logs -f` → Ver logs
* `docker compose down` → Detener y eliminar servicios

---

## Dockerfile — instrucciones principales

* `FROM` → Imagen base
* `WORKDIR` → Directorio de trabajo
* `COPY` → Copiar archivos al contenedor
* `ADD` → Copiar/descargar archivos (menos usado que COPY)
* `RUN` → Ejecutar comandos durante el build
* `ENV` → Variables de entorno
* `EXPOSE` → Documentar puertos usados por la app
* `USER` → Usuario que ejecuta el contenedor
* `CMD` → Comando por defecto (reemplazable)
* `ENTRYPOINT` → Comando fijo de arranque

---

## Buenas prácticas 

* Usar imágenes oficiales y livianas (alpine)
* Minimizar capas en el Dockerfile
* No guardar secretos en imágenes
* Usar `.dockerignore`
* Preferir `COPY` sobre `ADD`
