# Publish and Detached modes

Dos modos importantes en Docker: **Detached Mode** (modo separado) y **Publish** (publicación de puertos).

### **Detached Mode y Publicación de Puertos**

1. **`docker container run docker/getting-started`**
   - **Descripción**: Ejecuta un contenedor basado en la imagen `docker/getting-started`. Este comando ejecuta el contenedor en el primer plano, lo que significa que el terminal quedará ocupado mientras el contenedor esté en ejecución.

2. **`docker container run -d docker/getting-started`**
   - **Descripción**: Ejecuta el contenedor en **modo separado** (`-d`), lo que permite que el contenedor se ejecute en segundo plano, liberando el terminal para que puedas seguir usando otros comandos.
   - **Resultado**: Docker devuelve el ID del contenedor, indicando que el contenedor se está ejecutando en segundo plano.

3. **`docker container ls`**
   - **Descripción**: Lista todos los contenedores que están actualmente en ejecución. Muestra los detalles como el ID del contenedor, la imagen utilizada, los puertos publicados, y el estado.

4. **`docker container stop`**
   - **Descripción**: Si ejecutas este comando sin un ID o nombre de contenedor, no hará nada. El comando necesita un identificador para detener un contenedor en ejecución.

5. **`docker container stop 04f1a828ef53`**
   - **Descripción**: Detiene el contenedor específico identificado por el ID `04f1a828ef53`.
   - **Resultado**: El contenedor se detiene, lo que significa que deja de ejecutar cualquier proceso y libera los puertos que estaba utilizando.

6. **`docker container run -d -p 80:80 docker/getting-started`**
   - **Descripción**: Ejecuta el contenedor en **modo separado** y publica el puerto 80 del contenedor en el puerto 80 del host. Esto permite acceder a la aplicación que se ejecuta en el contenedor a través de `http://localhost:80`.
   - **Resultado**: El contenedor se ejecuta en segundo plano y está disponible en el puerto 80 del host.

7. **`docker container ls`**
   - **Descripción**: Vuelve a listar los contenedores en ejecución, mostrando ahora el contenedor que está en segundo plano y que tiene el puerto 80 publicado.

8. **`docker container stop ee3`**
   - **Descripción**: Detiene el contenedor identificado por el ID parcial `ee3`, liberando el puerto 80.

9. **`docker container run -dp 8080:80 docker/getting-started`**
   - **Descripción**: Ejecuta el contenedor en **modo separado** y publica el puerto 80 del contenedor en el puerto 8080 del host (`-dp` es una combinación de `-d` y `-p`).
   - **Resultado**: El contenedor se ejecuta en segundo plano y está disponible en `http://localhost:8080`.

10. **`docker container ls`**
    - **Descripción**: Lista los contenedores en ejecución, incluyendo el contenedor que tiene el puerto 8080 publicado.

11. **`docker container stop e44`**
    - **Descripción**: Detiene el contenedor identificado por el ID parcial `e44`.

12. **`docker container start e44`**
    - **Descripción**: Inicia nuevamente el contenedor identificado por `e44`, que había sido detenido previamente.
    - **Resultado**: El contenedor se reinicia y vuelve a estar disponible.

13. **`docker container ls -a`**
    - **Descripción**: Lista todos los contenedores, incluyendo los que han sido detenidos, mostrando sus estados.

14. **`docker container prune`**
    - **Descripción**: Elimina todos los contenedores detenidos para liberar espacio y mantener el sistema limpio.
    - **Resultado**: Todos los contenedores detenidos se eliminan del sistema.

15. **`docker image ls`**
    - **Descripción**: Lista todas las imágenes de Docker disponibles localmente en tu sistema.

16. **`docker image rm docker/getting-started`**
    - **Descripción**: Elimina la imagen `docker/getting-started` de tu sistema, liberando espacio en el almacenamiento local de Docker.
    - **Resultado**: La imagen se elimina si no está en uso por ningún contenedor.

### **Resumen:**

- **Modo Detached (`-d`)**: Permite ejecutar contenedores en segundo plano, liberando el terminal.
- **Publicación de Puertos (`-p`)**: Asocia puertos del contenedor con puertos del host, permitiendo el acceso a las aplicaciones en el contenedor desde el exterior.
- **Manejo de Contenedores**: Has aprendido a iniciar, detener, y eliminar contenedores, así como a publicar puertos para hacer que las aplicaciones sean accesibles desde el host.

Estos son conceptos fundamentales para trabajar eficientemente con Docker, especialmente en entornos de desarrollo y producción.