# Hola Mundo en Docker

`hello-world`

### 1. **`docker pull hello-world`**
   - **Descripción**: Este comando descarga (si no está ya en el sistema) la imagen de Docker llamada `hello-world` desde el Docker Hub (el repositorio de imágenes de Docker).
   - **Resultado**: La imagen `hello-world` se almacena localmente en tu máquina, lista para ser utilizada.

### 2. **`docker container run hello-world`**
   - **Descripción**: Este comando ejecuta un contenedor basado en la imagen `hello-world`. Si la imagen no está disponible localmente, Docker la descarga automáticamente (como ya has hecho con el `pull`) y luego la ejecuta.
   - **Resultado**: El contenedor muestra un mensaje simple de "Hello from Docker!" que confirma que Docker está funcionando correctamente. El contenedor se detiene y se elimina automáticamente después de mostrar este mensaje, ya que es un contenedor de tipo "one-shot".

### 3. **Repeticiones del Comando `docker container run hello-world`**
   - **Descripción**: Cada vez que ejecutas `docker container run hello-world`, Docker inicia un nuevo contenedor desde la misma imagen `hello-world` y muestra el mensaje "Hello from Docker!" nuevamente.
   - **Resultado**: Cada ejecución crea un contenedor nuevo, ejecuta el proceso (mostrar el mensaje) y luego Docker elimina automáticamente el contenedor después de completar la ejecución. 

### **Resumen:**
- **`docker pull hello-world`**: Descarga la imagen de `hello-world` desde Docker Hub.
- **`docker container run hello-world`**: Crea y ejecuta un contenedor basado en la imagen `hello-world`. El contenedor muestra un mensaje y luego se elimina.

Es normal que puedas ejecutar este comando varias veces, ya que cada ejecución es independiente de las anteriores. Docker maneja esto eficientemente creando y eliminando contenedores temporales.