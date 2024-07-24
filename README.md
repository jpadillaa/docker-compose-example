# docker-compose-example
Antes de iniciar los contenedores Docker, ejecuta los siguientes comandos para crear directorios para el almacenamiento de datos y registros. Estos comandos también cambiarán la propiedad de los directorios recién creados al usuario del contenedor Docker.

El comando `chown` se utiliza para cambiar el propietario de los directorios, y requiere permisos de `sudo`. Puede que se te pida que ingreses una contraseña para otorgar acceso `sudo`:

```bash
# Crear directorios para almacenamiento de datos y registros
$ sudo mkdir -p /ruta/a/tu/directorio/de/datos
$ sudo mkdir -p /ruta/a/tu/directorio/de/registros

# Cambiar la propiedad de los directorios al usuario del contenedor Docker
$ sudo chown 1000:1000 /ruta/a/tu/directorio/de/datos
$ sudo chown 1000:1000 /ruta/a/tu/directorio/de/registros
```

Configura la terminal en el directorio que contiene el archivo `docker-compose.yml` y ejecuta los siguientes comandos para iniciar este Docker Compose directamente:

```bash
$ docker compose up -d
$ docker compose logs -f mytb
```


