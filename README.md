# Sistema de Gestión de Farmacia

## Descripción General del Proyecto
Este es un sistema de gestión de farmacia de pila completa que incluye:
- Frontend desarrollado con React (Vite)
- Backend desarrollado con Django
- Base de datos PostgreSQL
- Contenedorización con Docker

## Repositorios
- **Backend**: [full-stack-modulo-8-grupo-5](https://github.com/edson-yanez-villa/full-stack-modulo-8-grupo-5)
- **Frontend**: [react-vite](https://github.com/santosjared/react-vite)

## Tecnologías Utilizadas
- **Frontend**:
    - React con Vite
    - Lenguaje: JavaScript/TypeScript
- **Backend**:
    - Django
    - Lenguaje: Python
- **Base de Datos**: PostgreSQL
- **Contenedores**: Docker

## Requisitos Previos
Antes de comenzar, asegúrate de tener instalado:
- Docker Desktop
- Docker Compose
- Git
- Un editor de código (VS Code, PyCharm, etc.)

## Configuración del Proyecto

### Clonar los Repositorios
```bash
# Clonar repositorio de backend
git clone https://github.com/edson-yanez-villa/full-stack-modulo-8-grupo-5.git

# Clonar repositorio de frontend
git clone https://github.com/santosjared/react-vite.git
```

### Levantar la Aplicación
Para iniciar todos los servicios con Docker:
```bash
docker-compose up --build
```

### Servicios y Puertos
- **Frontend**:
    - Puerto: 8383
    - URL: http://localhost:8383
- **Backend**:
    - Puerto: 8001
    - URL: http://localhost:8001
- **Base de Datos**:
    - Puerto: 5432
    - Sistema: PostgreSQL

## Variables de Entorno
Configuraciones importantes:
- `VITE_API_URL`: Endpoint de la API de backend (por defecto: http://localhost:8001)
- `POSTGRES_DB`: Nombre de la base de datos
- `POSTGRES_USER`: Usuario de la base de datos
- `POSTGRES_PASSWORD`: Contraseña de la base de datos

## Estructura del Proyecto
```
proyectoFinal/
│
├── react-vite/         # Proyecto Frontend
│   ├── src/
│   ├── Dockerfile
│   └── docker-compose.yml
│
├── full-stack-modulo-8-grupo-5/   # Proyecto Backend
│   ├── backend/
│   ├── Dockerfile
│   └── docker-compose.yml
│
├── docker-compose.yml  # Configuración Docker a nivel de proyecto
└── README.md
```

## Despliegue en Docker Hub
Pasos para subir las imágenes:
```bash
# Iniciar sesión en Docker Hub
docker login

# Construir imágenes
docker-compose build

# Etiquetar imágenes (reemplaza 'tu-usuario' con tu usuario de Docker Hub)
docker tag proyecto-frontend tu-usuario/farmacia-frontend
docker tag proyecto-backend tu-usuario/farmacia-backend
docker tag proyecto-db postgres:14

# Subir imágenes
docker push tu-usuario/farmacia-frontend
docker push tu-usuario/farmacia-backend
docker push postgres:14
```


## Colaboradores
- Edson Yanez Villa 
- Santos Machaca Lopez 
- Jorge Arze
- Kevin Paz
- Rene Bruno Vilela

## Problemas Comunes
- Si encuentras errores de conexión, verifica que Docker esté corriendo
- Asegúrate de tener la última versión de las dependencias
- Revisa los logs de Docker para diagnóstico de problemas
