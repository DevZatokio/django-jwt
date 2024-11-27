# Django Users API

Este es un proyecto Django que implementa una API básica para la gestión de usuarios, incluyendo registro, inicio de sesión y autenticación utilizando **Django REST Framework (DRF)** y **JWT** (JSON Web Tokens).

---

## Características

- Registro de usuarios.
- Inicio de sesión para obtener tokens JWT (access y refresh).
- Protección de rutas mediante autenticación JWT.
- Estructura básica para extender funcionalidad en el futuro.

---

## Requisitos

Antes de comenzar, asegúrate de tener instalados los siguientes programas:

- Python 3.8+ 
- pip (gestor de paquetes de Python)
- virtualenv (opcional pero recomendado)
- Git

---

## Instalación

Sigue estos pasos para clonar y configurar el proyecto en tu máquina local.

### 1. Clonar el repositorio
```bash
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_DIRECTORIO>
```

### 2. Crear un entorno virtual
```bash
python -m venv venv
source venv/bin/activate   # En Linux/Mac
venv\Scripts\activate      # En Windows
```

### 3. Instalar dependencias
```bash
pip install -r requirements.txt
```

### 4. Configurar las migraciones
```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Crear un superusuario (opcional)
```bash
python manage.py createsuperuser
```

### 6. Ejecutar el servidor
```bash
python manage.py runserver
```

El servidor estará disponible en [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

---

## Endpoints

### **Autenticación**

| Método | Endpoint           | Descripción                       |
|--------|--------------------|-----------------------------------|
| POST   | `/api/users/register/` | Registrar un nuevo usuario        |
| POST   | `/api/users/login/`    | Obtener tokens de acceso y refresh |
| POST   | `/api/users/token/refresh/` | Refrescar el token de acceso      |

### **Ejemplo de Registro**

**Solicitud:**
```http
POST /api/users/register/
Content-Type: application/json
```

**Cuerpo:**
```json
{
  "username": "testuser",
  "email": "test@example.com",
  "password": "securepassword"
}
```

**Respuesta Exitosa:**
```json
{
  "id": 1,
  "username": "testuser",
  "email": "test@example.com"
}
```

---

## Tecnologías Utilizadas

- **Django**: Framework backend principal.
- **Django REST Framework**: Construcción de API RESTful.
- **SimpleJWT**: Manejo de autenticación basada en tokens.
- **SQLite**: Base de datos por defecto para desarrollo.

---

## Próximos pasos

- Agregar funcionalidad para restablecimiento de contraseñas.
- Crear documentación con Swagger/OpenAPI.
- Mejorar la validación y personalización de los serializadores.
- Configurar despliegue para producción con Docker y PostgreSQL.

---

## Contribuciones

Las contribuciones son bienvenidas. Por favor, sigue estos pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama: `git checkout -b feature/nueva-funcionalidad`.
3. Realiza los cambios y haz commits: `git commit -m "Descripción de la funcionalidad"`.
4. Envía tus cambios: `git push origin feature/nueva-funcionalidad`.
5. Crea un Pull Request en GitHub.

---

## Licencia

Este proyecto está licenciado bajo la [MIT License](LICENSE).

---

## Autor

- DevZatokio
  - GitHub: [DevZatokio](https://github.com/DevZatokio)  
  - Email: [devzatokio@gmail.com](mailto:devzatokio@gmail.com)

---


### Cómo Usarlo  🚀
1. Guarda este contenido en un archivo `README.md` en el directorio raíz de tu proyecto.
2. Personaliza los campos como tu nombre, correo electrónico, y la URL del repositorio si es necesario.
3. Si tienes un archivo de licencia, asegúrate de incluirlo y vincularlo en la sección de Licencia.