# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**

<img width="670" height="129" alt="image" src="https://github.com/user-attachments/assets/ed3d9197-5e32-40d9-b9db-90b8a428f6a7" />

# COMPLETAR

**¿Qué es nginx**

Servidor web para contenido estático

Descargar la imagen  **nginx** en la versión **alpine**

<img width="655" height="222" alt="image" src="https://github.com/user-attachments/assets/83214db4-51aa-4cbe-b75c-88a0ac50444f" />

# COMPLETAR

### Listar imágenes

```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 

<img width="494" height="81" alt="image" src="https://github.com/user-attachments/assets/cd4bfa89-7cae-45f1-b8d5-42be1e2de668" />


**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 

<img width="771" height="422" alt="image" src="https://github.com/user-attachments/assets/17a0f1b0-9bb4-4699-b088-443234ea6d66" />

# COMPLETAR

**¿Con qué algoritmo se está generando el ID de la imagen**

SHA-256 (Secure Hash Algorithm 256-bit).

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

<img width="459" height="56" alt="image" src="https://github.com/user-attachments/assets/e64d6167-66c2-4eab-b88a-39239427aab0" />


### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```
Eliminar la imagen hello-world 

<img width="657" height="63" alt="image" src="https://github.com/user-attachments/assets/d12a6286-7247-4f2c-b454-631d8c98470d" />

# COMPLETAR

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```

<img width="663" height="448" alt="image" src="https://github.com/user-attachments/assets/f634939a-0f53-4cf6-867a-ea671843bbe0" />

