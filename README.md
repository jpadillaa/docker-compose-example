# docker-compose-example
Antes de iniciar los contenedores Docker, ejecuta los siguientes comandos para crear directorios para el almacenamiento de datos y registros. Estos comandos también cambiarán la propiedad de los directorios recién creados al usuario del contenedor Docker.

El comando `chown` se utiliza para cambiar el propietario de los directorios, y requiere permisos de `sudo`. Puede que se te pida que ingreses una contraseña para otorgar acceso `sudo`:

```bash
mkdir -p ~/.mytb-data && sudo chown -R 799:799 ~/.mytb-data
mkdir -p ~/.mytb-logs && sudo chown -R 799:799 ~/.mytb-logs
```

Configura la terminal en el directorio que contiene el archivo `docker-compose.yml` y ejecuta los siguientes comandos para iniciar este Docker Compose directamente:

```bash
$ docker compose up -d
$ docker compose logs -f mytb
```


