# Variables de entorno

### **Variables de Entorno en Docker**

Las variables de entorno se usan para configurar parámetros específicos dentro de un contenedor Docker. Estas se pasan al contenedor en el momento de su creación usando la opción `-e` en el comando `docker container run`.

### **Ejemplo con PostgreSQL**

**Pasos que has seguido:**

1. **Descargar la Imagen de PostgreSQL:**
   ```bash
   docker pull postgres
   ```
   Este comando descarga la imagen oficial de PostgreSQL desde [Docker Hub](https://hub.docker.com/_/postgres).

2. **Crear un Contenedor con PostgreSQL y Configurar Variables de Entorno:**
   ```bash
   docker container run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
   ```
   Aquí estás creando y ejecutando un contenedor con la imagen de PostgreSQL:
   - `--name some-postgres`: Da un nombre al contenedor (en este caso, `some-postgres`).
   - `-e POSTGRES_PASSWORD=mysecretpassword`: Configura la variable de entorno `POSTGRES_PASSWORD` para establecer la contraseña del usuario `postgres`.
   - `-d`: Ejecuta el contenedor en modo desapegado (detached), es decir, en segundo plano.

3. **Verificar que el Contenedor Está Corriendo:**
   ```bash
   docker container ls
   ```
   Este comando lista todos los contenedores en ejecución, permitiéndote verificar que el contenedor `some-postgres` está activo.

### **Uso de Variables de Entorno en PostgreSQL**

Las variables de entorno permiten configurar diferentes aspectos del contenedor PostgreSQL:

- **`POSTGRES_PASSWORD`**: Establece la contraseña para el usuario `postgres`.
- **`POSTGRES_USER`**: (Opcional) Define el nombre de usuario que se creará (por defecto es `postgres`).
- **`POSTGRES_DB`**: (Opcional) Nombre de la base de datos que se creará al inicio (por defecto es `postgres`).

Puedes pasar múltiples variables de entorno al contenedor al crearlo, simplemente agregando más flags `-e`:

```bash
docker container run --name my-postgres-container \
-e POSTGRES_USER=myuser \
-e POSTGRES_PASSWORD=mypassword \
-e POSTGRES_DB=mydatabase \
-d postgres
```

### **Explorando Tags de la Imagen en Docker Hub**

El enlace proporcionado te lleva a la página de Docker Hub donde puedes explorar los diferentes **tags** disponibles para la imagen de PostgreSQL. Cada tag representa una versión específica de PostgreSQL o una configuración particular (por ejemplo, `alpine`, `9.6`, `13`, etc.). Puedes explorar estos tags en [Docker Hub](https://hub.docker.com/_/postgres/tags).

### **Conclusión**

Las variables de entorno son una herramienta poderosa para personalizar la configuración de tus contenedores sin necesidad de modificar la imagen base. En el caso de PostgreSQL, se usan principalmente para establecer credenciales y configurar la base de datos inicial.