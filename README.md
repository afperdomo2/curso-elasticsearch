# Docker Compose para Elasticsearch

Este archivo `docker-compose.yml` se utiliza para configurar y ejecutar un contenedor Docker para Elasticsearch.

## Descripción del archivo docker-compose.yml

El archivo `docker-compose.yml` contiene la siguiente configuración:

- `version`: La versión de Docker Compose a utilizar.
- `services`: Define los servicios que se ejecutarán. En este caso, solo hay un servicio llamado `es01`.
- `es01`: Este es el servicio que ejecutará Elasticsearch.
  - `image`: La imagen de Docker a utilizar para este servicio.
  - `container_name`: El nombre del contenedor Docker.
  - `environment`: Las variables de entorno para configurar Elasticsearch.
  - `ulimits`: Los límites de los recursos del sistema para el contenedor.
  - `volumes`: Define los volúmenes para el contenedor.
  - `ports`: Los puertos que se expondrán al host.
  - `networks`: Las redes a las que se conectará el contenedor.
- `volumes`: Define los volúmenes que se utilizarán. En este caso, solo hay un volumen llamado `data01`.
- `networks`: Define las redes que se utilizarán. En este caso, solo hay una red llamada `elastic`.

## Cómo usar el archivo docker-compose.yml

Para usar este archivo, necesitarás tener Docker y Docker Compose instalados en tu máquina. Una vez que los tengas instalados, puedes ejecutar el siguiente comando en la misma carpeta que el archivo `docker-compose.yml`:

```bash
docker-compose up
```

## Endpoints

```
localhost:9200/usuarios/_doc/1
localhost:9200/usuarios/_doc?refresh
localhost:9200/usuarios/_bulk
```
