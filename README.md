# CRUD servido con API REST en JAVA

Este proyecto es una API REST desarrollada en **Java** que implementa un CRUD (Create, Read, Update, Delete). Su objetivo es servir como base para proyectos más complejos y aprender los fundamentos del desarrollo de APIs con Java y Spring Boot.

## Tecnologías utilizadas
1. **Spring Boot** – Framework para el desarrollo de aplicaciones web en Java
2. **Hibernate** – ORM para la gestión de bases de datos
3. **PostgreSQL** – Base de datos relacional
4. **Docker** – Contenedorización de la aplicación
5. **TablePlus** – Cliente para administrar la base de datos
6. **Postman** – Pruebas de endpoints de la API

## Cómo ejecutar el proyecto

### 1. Configurar la base de datos

Antes de ejecutar el proyecto, es necesario configurar la conexión con la base de datos. Para ello, edita el archivo `.env` y ajusta los valores según tu configuración.

### 2. Levantar el entorno con Docker

Asegúrate de que **Docker** está en ejecución antes de continuar. Luego, ejecuta el siguiente comando en la terminal:

docker-compose up -d

Este comando iniciará los contenedores necesarios para la base de datos y otros servicios requeridos.

### 3. Iniciar la API

Ejecuta el programa desde la terminal, asegurándote de que el punto de entrada sea `ApirestApplication.java`.

./mvnw spring-boot:run

(O si estás usando un IDE como IntelliJ IDEA o Eclipse, simplemente ejecuta la clase `ApirestApplication` como una aplicación de Spring Boot).

## Uso del CRUD

Para interactuar con la API, utiliza **Postman** o cualquier otro cliente REST.

### 1. Crear o modificar un producto (POST / PUT)

-   **Método:** `POST` o `PUT`
-   **URL:** `http://localhost:8080/productos`
-   **Body (JSON):**
    
    json - raw

	{
		  "nombre": "Nombre del producto",
		  "precio": 123.45
	}

### 2. Obtener todos los productos (GET)

-   **Método:** `GET`
-   **URL:** `http://localhost:8080/productos`

### 3. Obtener un producto por ID (GET)

-   **Método:** `GET`
-   **URL:** `http://localhost:8080/productos/{id}`
    -   Ejemplo: `http://localhost:8080/productos/3`

### 4. Eliminar un producto (DELETE)

-   **Método:** `DELETE`
-   **URL:** `http://localhost:8080/productos/{id}`
    -   Ejemplo: `http://localhost:8080/productos/3`
