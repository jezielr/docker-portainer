## Descripción

Portainer es una plataforma de administración y gestión de contenedores que proporciona una interfaz web para gestionar de forma centralizada entornos Docker y otras tecnologías de contenedores.

Permite administrar visualmente contenedores, imágenes, volúmenes, redes y stacks, facilitando tareas como crear, iniciar, detener, reiniciar, actualizar y eliminar contenedores sin depender exclusivamente de la línea de comandos.

### Docker Hub URL

https://hub.docker.com/r/portainer/portainer-ce/tags?name=latest

## Activar actualización de imagen docker con docker-controller-bot

[docker-controller-hub](https://github.com/dgongut/docker-controller-bot)  
Para realizar la actualización de manera automática se debe colocar la siguiente etiqueta "DCB-Auto-Update"

```
labels:  
    - "DCB-Auto-Update"  
```

## Levantar servicio

```
docker compose up -d
```

Para establecer la hora misma que la local se debe agregar esta configuración en la sección de volumes:
```bash
volumes:
     - /etc/localtime:/etc/localtime:ro
     - /etc/timezone:/etc/timezone:ro
```
