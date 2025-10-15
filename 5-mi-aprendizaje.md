## ¿Qué pude aprender?

### **Ciclo de Vida de Contenedores**
Comprendí el ciclo de vida de un contenedor: desde la descarga de imágenes, creación, ejecución, gestión, hasta la eliminación. 

### **Introducción a servicios containerizados**
Cómo ejecutar servidores web y herramientas de CI/CD (Jenkins) mediante contenedores. 

## Comandos Docker - Tabla Resumen

| **Comando** | **Explicación** | **Ejemplo del Repo** |
|-------------|-----------------|---------------------|
| `docker pull <imagen>` | Descarga una imagen desde Docker Hub | `docker pull hello-world` |
| `docker pull <imagen>:<tag>` | Descarga una versión específica de una imagen | `docker pull nginx:alpine` |
| `docker images` | Lista todas las imágenes descargadas localmente | `docker images` |
| `docker rmi <imagen>:<tag>` | Elimina una imagen permanentemente | `docker rmi hello-world:latest` |
| `docker create --name <nombre> <imagen>` | Crea un contenedor sin iniciarlo | `docker create --name srv-web nginx:alpine` |
| `docker start <contenedor>` | Inicia un contenedor previamente creado | `docker start srv-web` |
| `docker run --name <nombre> <imagen>` | Crea y ejecuta un contenedor inmediatamente (primer plano, terminal bloqueada) | `docker run --name srv-web2 nginx:alpine` |
| `docker run -d --name <nombre> <imagen>` | Crea y ejecuta un contenedor en segundo plano (detached) | `docker run -d --name srv-web3 nginx:alpine` |
| `docker ps` | Lista los contenedores en ejecución | `docker ps` |
| `docker ps -a` | Lista todos los contenedores (ejecutándose y detenidos) | `docker ps -a` |
| `docker stop <contenedor>` | Detiene un contenedor en ejecución | `docker stop srv-web` |
| `docker rm <contenedor>` | Elimina un contenedor detenido | `docker rm bold_proskuriakova` |
| `docker rm -f <contenedor>` | Elimina un contenedor ejecutándose (forzado) | `docker rm -f srv-web3` |
| `docker inspect <contenedor>` | Muestra información detallada del contenedor | `docker inspect srv-web` |
| `docker exec <contenedor> <comando>` | Ejecuta un comando en un contenedor en ejecución | `docker exec jenkins_server ls -l` |
| `docker exec -i <contenedor> <comando>` | Ejecuta un comando manteniendo stdin abierto | `docker exec -i jenkins_server bash` |
| `docker exec -it <contenedor> <comando>` | Ejecuta un shell interactivo bidireccional | `docker exec -it jenkins_server whoami` |
| `docker logs -n <líneas> <contenedor>` | Muestra los logs del contenedor | `docker logs -n 20 jenkins_server` |

## Comandos Especiales 

- **`docker exec jenkins_server cat /var/jenkins_home/secrets/initialAdminPassword`**: Obtiene la contraseña inicial de Jenkins
---

