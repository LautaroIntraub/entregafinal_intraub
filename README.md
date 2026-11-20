# 📦 Article Management System

Aplicación web de gestión de artículos desarrollada con **Java y Spring Boot**, conectada a una base de datos MySQL. Permite administrar artículos mediante operaciones CRUD a través de una API REST y una interfaz web moderna e intuitiva.

## 🎥 Demo del proyecto

Mirá el siguiente video para conocer el funcionamiento de la aplicación:

[▶️ Ver demostración del proyecto en YouTube](https://youtu.be/Pr8BBJuUNvU)

## ✨ Características principales

- **Gestión de artículos (CRUD):** creación, consulta, modificación y eliminación de registros.
- **API REST:** endpoints para interactuar con los datos mediante solicitudes HTTP.
- **Persistencia de datos:** almacenamiento de información utilizando MySQL.
- **Buscador dinámico:** permite filtrar artículos por nombre.
- **Dashboard administrativo:** visualización de estadísticas generales.
- **Estadísticas:** cantidad de artículos registrados, valor total y precio promedio.
- **Interfaz responsive:** diseño adaptable a diferentes dispositivos.
- **Validaciones:** controles básicos para evitar el ingreso de datos incorrectos.

## 🏗️ Arquitectura del proyecto

El proyecto utiliza una arquitectura por capas para separar responsabilidades y facilitar el mantenimiento del código.

```text
src/
└── main/
    ├── java/
    │   └── com/teclab/articulomysql/
    │       ├── controller/
    │       │   └── ArticuloController.java
    │       │
    │       ├── model/
    │       │   └── Articulo.java
    │       │
    │       ├── repository/
    │       │   └── ArticuloRepository.java
    │       │
    │       ├── service/
    │       │   ├── ArticuloService.java
    │       │   └── ArticuloServiceImpl.java
    │       │
    │       └── ArticulomysqlApplication.java
    │
    └── resources/
        ├── static/
        │   └── index.html
        │
        └── application.properties
```

### Responsabilidades de cada capa

- **Controller:** recibe las solicitudes HTTP y expone los endpoints de la API.
- **Service:** contiene la lógica de negocio de la aplicación.
- **Repository:** administra las operaciones de acceso a datos mediante Spring Data JPA.
- **Model:** representa la entidad Articulo y su correspondencia con la tabla de MySQL.
- **Static:** contiene la interfaz web desarrollada con HTML, CSS y JavaScript.

## 🔌 Endpoints de la API

La API REST está disponible bajo la ruta `/api/articulos`.

| Método | Endpoint | Descripción |
|---|---|---|
| GET | `/api/articulos` | Listar todos los artículos |
| GET | `/api/articulos/{id}` | Obtener un artículo por ID |
| POST | `/api/articulos` | Registrar un nuevo artículo |
| PUT | `/api/articulos/{id}` | Actualizar un artículo |
| DELETE | `/api/articulos/{id}` | Eliminar un artículo |

### Ejemplo de objeto JSON

```json
{
  "nombre": "Teclado mecánico",
  "precio": 25000.00
}
```

Una vez iniciado Spring Boot, ingresar desde el navegador:

```text
http://localhost:8080/
```

La interfaz web se sirve directamente desde Spring Boot mediante la carpeta `static`.

## 🎯 Objetivo del proyecto

Este proyecto fue desarrollado como trabajo práctico final con el objetivo de aplicar conceptos de programación orientada a objetos, arquitectura por capas, persistencia de datos, desarrollo de APIs REST e integración entre backend y frontend.

Permite poner en práctica el uso de tecnologías del ecosistema Java y comprender el funcionamiento de una aplicación web conectada a una base de datos relacional.

---
