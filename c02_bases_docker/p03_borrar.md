# Borrar contenedores e imágenes

### **Comandos para Contenedores**

1. **`docker container run hello-world`**
   - **Descripción**: Ejecuta un contenedor basado en la imagen `hello-world` y muestra un mensaje de prueba. Este contenedor se detiene y elimina automáticamente después de ejecutarse.
   
2. **`docker container --help`**
   - **Descripción**: Muestra la lista de comandos y opciones disponibles para administrar contenedores en Docker.

3. **`docker container ls`**
   - **Descripción**: Lista los contenedores en ejecución actualmente.
   - **Resultado**: Si no hay contenedores en ejecución, este comando no mostrará nada.

4. **`docker container ls -a`**
   - **Descripción**: Lista todos los contenedores, incluidos los que han finalizado su ejecución.
   - **Resultado**: Verás todos los contenedores, incluyendo aquellos que han terminado su ejecución (como los de `hello-world`).

5. **`docker container rm 451fa52a3155`**
   - **Descripción**: Elimina un contenedor específico identificado por su ID (en este caso, `451fa52a3155`).
   - **Resultado**: El contenedor especificado es eliminado.

6. **`docker container ls -a`**
   - **Descripción**: Vuelve a listar todos los contenedores, incluidos los que han finalizado, para verificar qué contenedores aún existen.

7. **`docker container rm 067 0d5`**
   - **Descripción**: Elimina múltiples contenedores en un solo comando utilizando parte de sus IDs.
   - **Resultado**: Los contenedores correspondientes a esos IDs son eliminados.

8. **`docker container prune`**
   - **Descripción**: Elimina todos los contenedores detenidos. Es una forma rápida de limpiar contenedores que ya no necesitas.
   - **Resultado**: Todos los contenedores que no están en ejecución son eliminados.

9. **`docker container ls -a`**
   - **Descripción**: Vuelve a listar todos los contenedores para confirmar que han sido eliminados.
   - **Resultado**: No debería aparecer ningún contenedor si han sido eliminados todos correctamente.

### **Comandos para Imágenes**

1. **`docker images --help`**
   - **Descripción**: Muestra la lista de comandos y opciones disponibles para administrar imágenes en Docker.

2. **`docker image --help`**
   - **Descripción**: Similar al anterior, muestra las opciones y comandos para administrar imágenes.

3. **`docker image ls`**
   - **Descripción**: Lista todas las imágenes locales disponibles en tu sistema Docker.
   - **Resultado**: Verás una lista de todas las imágenes descargadas, incluyendo `hello-world`.

4. **`docker image rm hello-world`**
   - **Descripción**: Elimina la imagen `hello-world` de tu sistema.
   - **Resultado**: La imagen `hello-world` es eliminada del almacenamiento local de Docker.

### **Resumen:**
- **Contenedores**: Has aprendido a listar, eliminar y limpiar contenedores que ya no están en uso.
- **Imágenes**: Has aprendido a listar y eliminar imágenes de Docker.

Estos comandos son esenciales para mantener tu entorno de Docker limpio y evitar acumulaciones innecesarias de contenedores e imágenes que ya no necesitas.