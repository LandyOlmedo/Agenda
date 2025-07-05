# 📱 Agenda de Contactos Web

Una aplicación web completa para gestionar contactos desarrollada con Python y web.py, implementando operaciones CRUD con base de datos SQLite.

## 🚀 Características

- ✅ **CRUD Completo**: Crear, leer, actualizar y eliminar contactos
- 📊 **Base de Datos**: SQLite para persistencia de datos
- 🎨 **Interfaz Moderna**: Diseño responsivo con HTML5 y CSS3
- 🔍 **Navegación Intuitiva**: Enlaces directos entre vistas
- 📱 **Diseño Responsivo**: Compatible con dispositivos móviles y desktop

## 🛠️ Tecnologías Utilizadas

### Backend
- **Python 3.12+** - Lenguaje de programación principal
- **web.py** - Framework web minimalista
- **SQLite3** - Base de datos ligera

### Frontend
- **HTML5** - Estructura de las páginas
- **CSS3** - Estilos y diseño visual
- **Motor de plantillas web.py** - Renderizado dinámico

## 📁 Estructura del Proyecto

```
Agenda/
├── app.py                 # Aplicación principal
├── agenda.db             # Base de datos SQLite
├── agenda.sql            # Script SQL inicial
├── server.log            # Logs del servidor
├── templates/            # Plantillas HTML
│   ├── personas.html     # Lista principal y formulario
│   ├── detalle.html      # Vista detallada de contacto
│   ├── editar.html       # Formulario de edición
│   └── borrar.html       # Confirmación de eliminación
└── README.md             # Este archivo
```

## 🔧 Instalación y Configuración

### Prerrequisitos
```bash
# Python 3.12 o superior
python --version

# Verificar pip
pip --version
```

### Paso 1: Clonar el repositorio
```bash
git clone <tu-repositorio>
cd Agenda
```

### Paso 2: Instalar dependencias
```bash
pip install web.py
```

### Paso 3: Configurar la base de datos
```bash
# Crear la base de datos con el script SQL
sqlite3 agenda.db < agenda.sql
```

### Paso 4: Ejecutar la aplicación
```bash
python app.py
```

La aplicación estará disponible en: `http://localhost:8080`

## 💻 Uso de la Aplicación

### Página Principal (`/`)
- **Vista**: Lista de todos los contactos
- **Funcionalidad**: Formulario para agregar nuevos contactos
- **Acciones**: Ver, Editar, Eliminar contactos

### Ver Contacto (`/detalle/<id>`)
- **Vista**: Información detallada del contacto
- **Funcionalidad**: Visualización completa de datos
- **Navegación**: Enlaces a editar y eliminar

### Editar Contacto (`/editar/<id>`)
- **Vista**: Formulario de edición pre-poblado
- **Funcionalidad**: Actualizar información del contacto
- **Validación**: Campos requeridos y tipos de datos

### Eliminar Contacto (`/borrar/<id>`)
- **Vista**: Confirmación antes de eliminar
- **Funcionalidad**: Eliminación segura con confirmación
- **Seguridad**: Prevención de eliminaciones accidentales

## 🗄️ Esquema de Base de Datos

```sql
CREATE TABLE personas (
    id_persona INTEGER PRIMARY KEY AUTOINCREMENT,
    nombre TEXT NOT NULL,
    email TEXT NOT NULL UNIQUE
);
```

## 🚦 Rutas de la API

| Método | Ruta | Descripción |
|--------|------|-------------|
| GET | `/` | Lista todos los contactos |
| POST | `/` | Crea un nuevo contacto |
| GET | `/detalle/<id>` | Muestra detalles del contacto |
| GET | `/editar/<id>` | Formulario de edición |
| POST | `/editar/<id>` | Actualiza el contacto |
| GET | `/borrar/<id>` | Confirmación de eliminación |
| POST | `/borrar/<id>` | Elimina el contacto |

## 📝 Código Principal

### Configuración de Rutas
```python
urls = (
    "/", "Personas",
    "/detalle/(.*)", "Detalle",
    "/editar/(.*)", "Editar",
    "/borrar/(.*)", "Borrar"
)
```

### Clase Principal (Ejemplo)
```python
class Personas:
    def GET(self):
        # Obtener y mostrar contactos
        return render.personas(personas)
    
    def POST(self):
        # Crear nuevo contacto
        form = web.input()
        # Insertar en base de datos
        raise web.seeother("/")
```

## 🎨 Características de Diseño

- **Colores**: Paleta moderna con azules y grises
- **Tipografía**: Arial, sans-serif para legibilidad
- **Componentes**: Botones con estados hover
- **Layout**: Contenedor centrado con sombras
- **Responsive**: Adaptable a diferentes tamaños de pantalla

## 🔍 Funcionalidades Implementadas

### ✅ Operaciones CRUD
- [x] **Create**: Agregar nuevos contactos
- [x] **Read**: Listar y ver contactos
- [x] **Update**: Editar contactos existentes
- [x] **Delete**: Eliminar contactos

### ✅ Validaciones
- [x] Campos obligatorios
- [x] Validación de email
- [x] Manejo de errores
- [x] Confirmación de eliminación

### ✅ Navegación
- [x] Enlaces entre páginas
- [x] Botones de acción
- [x] Redirección después de operaciones
- [x] Botones de cancelar

## 🚀 Despliegue

### Desarrollo Local
```bash
python app.py
```

### Producción (Ejemplo con Gunicorn)
```bash
pip install gunicorn
gunicorn -w 4 -b 0.0.0.0:8080 app:app
```

## 📊 Capturas de Pantalla

### Página Principal
- Lista de contactos con formulario de agregar
- Tabla responsive con acciones

### Vista de Detalle
- Información completa del contacto
- Navegación clara

### Formulario de Edición
- Campos pre-poblados
- Validación en tiempo real

## 🤝 Contribuciones

Si deseas contribuir al proyecto:

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -am 'Agrega nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.


