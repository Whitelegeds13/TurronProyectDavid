# Sistema de Ventas con Python Flask

Este es un sistema completo de gestión de ventas desarrollado con Python Flask que incluye autenticación y todas las funcionalidades necesarias para administrar un negocio.

## Características

### 🔐 Autenticación
- ✅ Sistema de registro de usuarios
- ✅ Sistema de login/logout
- ✅ Dashboard protegido
- ✅ Seguridad con hash de contraseñas

### 🏪 Gestión de Negocio
- ✅ **Productos**: Gestión completa con categorías y stock
- ✅ **Categorías**: Organización de productos
- ✅ **Clientes**: Base de datos de clientes
- ✅ **Tiendas**: Gestión de sucursales
- ✅ **Ventas**: Sistema completo de ventas con descuentos
- ✅ **Stock**: Control automático de inventario

### 🎨 Interfaz
- ✅ Interfaz moderna con Bootstrap
- ✅ Dashboard con estadísticas
- ✅ Formularios intuitivos
- ✅ Mensajes flash informativos

## Instalación

1. Instala las dependencias:
```bash
pip install -r requirements.txt
```

2. Ejecuta la aplicación:
```bash
python app.py
```

3. Abre tu navegador en: http://127.0.0.1:5000

## Uso

1. Ve a la página de registro para crear una cuenta
2. Inicia sesión con tus credenciales
3. Accede al dashboard una vez autenticado
4. Cierra sesión cuando termines

## Estructura del Proyecto

```
v1.0/
├── app.py                 # Aplicación principal Flask
├── requirements.txt       # Dependencias del proyecto
├── README.md             # Este archivo
└── templates/            # Plantillas HTML
    ├── base.html         # Plantilla base
    ├── login.html        # Página de login
    ├── register.html     # Página de registro
    ├── dashboard.html    # Dashboard principal
    ├── productos.html    # Lista de productos
    ├── nuevo_producto.html # Formulario nuevo producto
    ├── categorias.html   # Lista de categorías
    ├── nueva_categoria.html # Formulario nueva categoría
    ├── clientes.html     # Lista de clientes
    ├── nuevo_cliente.html # Formulario nuevo cliente
    ├── tiendas.html      # Lista de tiendas
    ├── nueva_tienda.html # Formulario nueva tienda
    ├── ventas.html       # Lista de ventas
    └── nueva_venta.html  # Formulario nueva venta
```

## Base de Datos

La aplicación crea automáticamente una base de datos SQLite (`sistema_ventas.db`) con las siguientes tablas:

- **usuarios**: Información de usuarios del sistema
- **categorias**: Categorías de productos
- **productos**: Productos con relación a categorías
- **stock**: Control de inventario por producto
- **clientes**: Base de datos de clientes
- **tiendas**: Información de sucursales
- **descuentos**: Descuentos disponibles
- **ventas**: Registro de ventas (entidad central)
- **venta_producto**: Relación muchos a muchos entre ventas y productos

## Flujo de Trabajo

1. **Configuración inicial**: Crear categorías y tiendas
2. **Productos**: Agregar productos con stock inicial
3. **Clientes**: Registrar clientes
4. **Ventas**: Procesar ventas que actualizan automáticamente el stock

## Seguridad

- Las contraseñas se almacenan con hash usando Werkzeug
- Las sesiones están protegidas con Flask-Login
- Validación de formularios en el servidor
- Control de stock automático en las ventas
