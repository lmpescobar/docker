# 15. Docker Desktop - Mismos comandos ejecutados

### **Docker Desktop: Interfaz Gráfica vs. Línea de Comandos**

#### **Interfaz Gráfica de Docker Desktop**
- **Buscar Imágenes**: Puedes buscar imágenes en Docker Hub directamente desde Docker Desktop. Aquí puedes ver si la imagen es oficial o de código abierto, y hacer clic para ver más detalles y documentación.
- **Descargar Imágenes**: Puedes descargar imágenes localmente usando el botón "Pull".
- **Ejecutar Contenedores**: Ejecutar un contenedor se puede hacer fácilmente con el botón "Run". También puedes configurar parámetros opcionales desde la interfaz gráfica.
- **Ver Logs**: Docker Desktop permite ver los logs del contenedor en ejecución a través de su interfaz.
- **Eliminar Contenedores e Imágenes**: Puedes eliminar contenedores e imágenes seleccionándolos y usando las opciones disponibles. Docker Desktop te notificará si intentas eliminar una imagen en uso, y te pedirá que primero elimines los contenedores asociados.

#### **Línea de Comandos de Docker**
- **`docker pull [imagen]`**: Descarga una imagen desde Docker Hub.
- **`docker container run [imagen]`**: Ejecuta un contenedor basado en la imagen especificada.
- **`docker container ls`**: Muestra los contenedores en ejecución.
- **`docker container stop [id]`**: Detiene un contenedor.
- **`docker container rm [id]`**: Elimina un contenedor detenido.
- **`docker image ls`**: Lista todas las imágenes locales.
- **`docker image rm [imagen]`**: Elimina una imagen local.

### **Conclusiones y Recomendaciones**
- **Docker Desktop vs. Línea de Comandos**: La interfaz gráfica es intuitiva y facilita la gestión de contenedores e imágenes sin necesidad de recordar los comandos. Sin embargo, aprender y practicar los comandos de la línea de comandos es esencial para tener un control más preciso y para entornos en los que solo se dispone de terminal.
- **Práctica**: Aunque la interfaz gráfica es útil, familiarizarse con los comandos es importante. Con práctica, los comandos se vuelven más naturales y fáciles de recordar.