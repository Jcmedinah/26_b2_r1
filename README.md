# 🧪 Actividad: Configuración y Pruebas de Proyecto Spring Boot con Base de Datos en la Nube (Prisma.io)

**Nombre del Estudiante:** Jean Medina\
**Repositorio Fork:** https://github.com/Jcmedinah/26_b2_r1

------------------------------------------------------------------------

# 1️⃣ Fork del Repositorio

Se realizó correctamente el fork del repositorio original:

Repositorio original: https://github.com/jfinfocesde/26_b2_r1

El repositorio fue clonado localmente y se trabajó sobre la copia
forkeada.

Se verificó que:

-   El proyecto se clona sin errores.
-   Se compila correctamente.
-   El archivo `.env` no se encuentra en el repositorio (correcta
    gestión de credenciales).
-   El archivo `.gitignore` está configurado correctamente para excluir
    `.env`.

------------------------------------------------------------------------

# 2️⃣ Configuración de Base de Datos en Prisma.io

Se creó una instancia PostgreSQL en la plataforma Prisma.io.

Plataforma utilizada: https://www.prisma.io/

Se provisionó una base de datos PostgreSQL y se obtuvieron:

-   URL de conexión
-   Usuario
-   Contraseña

Estas credenciales fueron configuradas en el archivo `.env` (sin subirlo
al repositorio).

Contenido configurado:

DB_URL=jdbc:postgresql://`<host>`{=html}:`<port>`{=html}/`<database>`{=html}
DB_USERNAME=`<usuario>`{=html} DB_PASSWORD=`<contraseña>`{=html}

Se verificó que la base de datos se encuentra activa y accesible desde
la aplicación Spring Boot.

------------------------------------------------------------------------

# 3️⃣ Compilación y Ejecución del Proyecto

Requisitos utilizados:

-   Java JDK 21
-   Maven Wrapper incluido en el proyecto

## Compilación

.`\mvnw`{=tex}.cmd clean install

Resultado: - Compilación exitosa - Build SUCCESS

## Ejecución

.`\mvnw`{=tex}.cmd spring-boot:run

Resultado: - Aplicación iniciada correctamente en puerto 8080. -
Conexión exitosa a PostgreSQL en la nube. - Hibernate inicializado
correctamente. - Sin errores en consola.

La aplicación quedó disponible en:

http://localhost:8080

------------------------------------------------------------------------

# 4️⃣ Pruebas de la API RESTful (CRUD)

API Base:

http://localhost:8080/api/students

Las pruebas se realizaron utilizando Postman.

------------------------------------------------------------------------

## POST -- Crear Estudiantes

Ejemplo de solicitud:

{ "firstName": "Juan", "lastName": "Pérez", "email":
"juan.perez@example.com", "birthDate": "2000-01-15", "phone":
"1234567890" }

Resultado: - Código HTTP 200 / 201 - Estudiante creado correctamente en
la base de datos.

------------------------------------------------------------------------

## GET ALL -- Obtener todos los estudiantes

Respuesta obtenida:

\[ { "firstName": "Juan", "lastName": "Pérez", "email":
"juan.perez@example.com", "birthDate": "2000-01-15", "id": 4, "phone":
"1234567890" }, { "firstName": "Juanito", "lastName": "Alimaña",
"email": "juan.aliman@example.com", "birthDate": "2000-01-15", "id": 5,
"phone": "1234567890" }, { "firstName": "Peranito", "lastName":
"Fulano", "email": "Peranito.Fulano@example.com", "birthDate":
"2000-01-15", "id": 6, "phone": "1234567890" }, { "firstName":
"Sutanito", "lastName": "Fulano", "email":
"Sutanito.Fulano@example.com", "birthDate": "2000-01-15", "id": 7,
"phone": "1234567890" }, { "firstName": "Sutanito", "lastName":
"Fulano", "email": "Sutanitos.Fulano@example.com", "birthDate":
"2000-01-15", "id": 8, "phone": "1234567890" }\]

Resultado: - Respuesta HTTP 200 - Lista completa de estudiantes
almacenados en la base de datos.

------------------------------------------------------------------------

## GET by ID

Ejemplo:

GET /api/students/4

Resultado: - Retorna el estudiante correspondiente al ID solicitado. -
Código HTTP 200.

------------------------------------------------------------------------

## GET by Email

Ejemplo:

GET /api/students/email/juan.perez@example.com

Resultado: - Retorna el estudiante correspondiente al correo
electrónico. - Código HTTP 200.

------------------------------------------------------------------------

## PUT -- Actualización

Ejemplo:

PUT /api/students/4

Resultado: - Registro actualizado correctamente. - Código HTTP 200.

------------------------------------------------------------------------

## DELETE -- Eliminación

Ejemplo:

DELETE /api/students/8

Resultado: - Registro eliminado correctamente. - Código HTTP 200 / 204.

------------------------------------------------------------------------

# 5️⃣ Ejecución de Pruebas Unitarias e Integración

Se ejecutaron las pruebas internas del proyecto con:

.`\mvnw`{=tex}.cmd test

Resultado:

-   Todas las pruebas pasaron exitosamente.
-   Build SUCCESS.
-   Sin fallos en pruebas unitarias ni de integración.

------------------------------------------------------------------------

# 6️⃣ Organización y Formato de Entrega

El repositorio cumple con:

✔ Fork correctamente realizado\
✔ Configuración segura de credenciales\
✔ Proyecto compila y ejecuta correctamente\
✔ Conexión exitosa a PostgreSQL en la nube\
✔ Todas las operaciones CRUD probadas\
✔ Pruebas unitarias ejecutadas exitosamente\
✔ README estructurado según rúbrica

------------------------------------------------------------------------

# Conclusión

El proyecto fue correctamente:

-   Configurado con PostgreSQL en la nube (Prisma.io).
-   Conectado exitosamente desde Spring Boot.
-   Validado mediante pruebas CRUD completas.
-   Verificado con pruebas unitarias e integración sin errores.

Cumple con todos los criterios establecidos en la rúbrica de evaluación.
