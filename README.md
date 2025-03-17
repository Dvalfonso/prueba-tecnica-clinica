# prueba-tecnica-clinica

# API REST para Gestión de Pacientes y Turnos Médicos

## Descripción
Este proyecto es una API REST desarrollada con Spring Boot, Spring Data JPA y PostgreSQL para la gestión de pacientes y turnos médicos.

## Tecnologías Utilizadas
- Java 21
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Maven
- Docker (Opcional)

## Instalación y Ejecución
### Requisitos Previos
- Tener instalado Java 21 o superior.
- Tener instalado Maven.
- Tener una instancia de PostgreSQL corriendo.

### Configuración de la Base de Datos
Modifica el archivo `application.properties` o `application.yml` con la configuración de tu base de datos:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/clinica
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### Construcción y Ejecución
Clona el repositorio:
```sh
git clone https://github.com/Dvalfonso/prueba-tecnica-clinica
cd cd prueba-tecnica-clinica
```

Compila y ejecuta la aplicación:
```sh
mvn clean install
mvn spring-boot:run
```

Si usas Docker, puedes levantar la base de datos con:
```sh
docker-compose up -d
```

## Endpoints Disponibles
### Pacientes (`/patients`)
- **POST** `/patients` → Crear un paciente.
- **GET** `/patients` → Obtener la lista de pacientes.
- **GET** `/patients/{id}` → Obtener un paciente por su ID.
- **PUT** `/patients/{id}` → Actualizar un paciente.
- **DELETE** `/patients/{id}` → Eliminar un paciente.

### Turnos (`/appointments`)
- **POST** `/appointments` → Crear un turno (asociado a un paciente).
- **GET** `/appointments` → Obtener la lista de turnos.
- **GET** `/appointments/{id}` → Obtener un turno por su ID.
- **PUT** `/appointments/{id}` → Actualizar un turno.
- **DELETE** `/appointments/{id}` → Eliminar un turno.

## Extras
- Autenticación JWT para proteger los endpoints.
- Paginación en las listas de pacientes y turnos.
- Logging con `SLF4J` y `Logback`.

## Autor
- Dvalfonso

