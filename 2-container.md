# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine

```
docker create --name srv-web nginx:alpine
```

<img width="532" height="49" alt="image" src="https://github.com/user-attachments/assets/b7eebb59-3b52-4f5e-a21e-c3ce3e161d48" />

# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

```
docker create hello-world
```

<img width="542" height="45" alt="image" src="https://github.com/user-attachments/assets/ac79e50d-d809-441a-9544-680bf78523dd" />


# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```

<img width="1088" height="98" alt="image" src="https://github.com/user-attachments/assets/77677c9d-94e2-49d6-a91d-3eb572835710" />

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
```
docker start srv-web
```
<img width="319" height="38" alt="image" src="https://github.com/user-attachments/assets/e1dbf548-2ed9-4f9c-aa75-f28f747a8fd7" />

# COMPLETAR

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

<img width="855" height="65" alt="image" src="https://github.com/user-attachments/assets/181b020a-0500-4a7d-b191-945d65b8a496" />

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

```
docker stop srv-web
```
<img width="333" height="47" alt="image" src="https://github.com/user-attachments/assets/3180e9ae-7234-4c8f-8c8d-8748081ebb26" />

<img width="616" height="48" alt="image" src="https://github.com/user-attachments/assets/876f977b-dad0-4022-9216-95c6f9f92810" />

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine

```
docker run --name srv-web2 nginx:alpine
```

<img width="777" height="397" alt="image" src="https://github.com/user-attachments/assets/d5c19857-0d64-4c3b-8df2-2f10a8958278" />

# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**

La terminal no permite recibir más instrucciones, está dedicada a la ejecución del contenedor. 

# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```


Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine

```
docker run -d --name srv-web3 nginx:alpine
```

<img width="548" height="42" alt="image" src="https://github.com/user-attachments/assets/a84dc0a1-5bcb-4b51-8649-6755ec98d8ed" />

<img width="868" height="69" alt="image" src="https://github.com/user-attachments/assets/da0d35bf-513b-41e2-9fb0-42e985b65b13" />

# COMPLETAR

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 


```
docker rm  bold_proskuriakova
```
<img width="409" height="49" alt="image" src="https://github.com/user-attachments/assets/95038df1-5a54-43b3-bd9f-9950205ee62b" />

# COMPLETAR

Verificar que el contenedor que se eliminó

```
docker ps -a
```
<img width="1011" height="112" alt="image" src="https://github.com/user-attachments/assets/62e2ae3e-19d4-4592-a19f-92d4beeba286" />

# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

```
docker rm -f srv-web3
```
<img width="333" height="45" alt="image" src="https://github.com/user-attachments/assets/3285e5dc-896b-41e5-9348-7acf50032d66" />


# COMPLETAR

Verificar que el contenedor que se eliminó

```
docker ps
```

<img width="586" height="47" alt="image" src="https://github.com/user-attachments/assets/66d8ea62-da63-4d23-8b3a-aa9a6e348f25" />

# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 

```
docker inspect srv-web
```

<img width="1513" height="675" alt="image" src="https://github.com/user-attachments/assets/a0cc7a11-9593-4e62-818e-90b211f797ae" />

# COMPLETAR
