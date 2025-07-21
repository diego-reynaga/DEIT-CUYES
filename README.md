# Sistema de Gestión y Venta de Cuyes - INIA Andahuaylas

Sistema web desarrollado en Flask para la gestión integral de cuyes en el Instituto Nacional de Innovación Agraria (INIA) de Andahuaylas.

## Características Principales

- **Gestión de Cuyes**: Control completo del inventario de cuyes
- **Sistema de Ventas**: Plataforma de venta en línea
- **Control Sanitario**: Seguimiento de tratamientos y controles de salud
- **Gestión de Usuarios**: Sistema de roles (administrador, empleado, cliente)
- **Reportes**: Generación de reportes en PDF y Excel
- **Interfaz Moderna**: Diseño minimalista y responsivo

## Requisitos del Sistema

- Python 3.8+
- MySQL 8.0+
- Navegador web moderno

## Instalación

1. **Clonar el repositorio**
```bash
git clone <repo-url>
cd DEIT-CUYES
```

2. **Crear entorno virtual**
```bash
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Linux/Mac
```

3. **Instalar dependencias**
```bash
pip install -r requirements.txt
```

4. **Configurar base de datos**
```bash
# Crear base de datos MySQL
mysql -u root -p
CREATE DATABASE cuyes_db;
```

5. **Configurar variables de entorno**
```bash
# Crear archivo .env
cp .env.example .env
# Editar .env con tus configuraciones
```

6. **Inicializar base de datos**
```bash
flask db init
flask db migrate -m "Initial migration"
flask db upgrade
```

7. **Crear usuario administrador**
```bash
python create_admin.py
```

## Ejecutar la Aplicación

```bash
flask run
```

La aplicación estará disponible en: http://localhost:5000

## Estructura del Proyecto

```
DEIT-CUYES/
├── app/
│   ├── __init__.py
│   ├── models/
│   ├── views/
│   ├── forms/
│   ├── static/
│   └── templates/
├── migrations/
├── config.py
├── run.py
└── requirements.txt
```

## Funcionalidades

### Para Administradores
- Gestión completa de cuyes
- Control de usuarios y roles
- Generación de reportes
- Configuración del sistema

### Para Empleados
- Registro de controles sanitarios
- Gestión de tratamientos
- Consulta de inventario

### Para Clientes
- Catálogo de cuyes disponibles
- Proceso de compra
- Historial de pedidos

## Tecnologías Utilizadas

- **Backend**: Flask, SQLAlchemy
- **Frontend**: HTML5, CSS3, JavaScript, Bootstrap
- **Base de Datos**: MySQL
- **Reportes**: ReportLab (PDF), OpenPyXL (Excel)
- **Autenticación**: Flask-Login, Flask-Bcrypt

## Licencia

Este proyecto está desarrollado para el INIA Andahuaylas.
