# 📱 Mi Agenda de Contactos

¡Hola! Este es mi proyecto de una agenda de contactos web. Es una aplicación simple pero funcional donde puedes guardar, ver, editar y eliminar contactos de forma fácil.

## ¿Qué hace esta aplicación?

- � **Agregar contactos** - Guarda nombres y emails
- 👀 **Ver contactos** - Muestra todos tus contactos en una tabla
- ✏️ **Editar contactos** - Cambia la información cuando quieras
- �️ **Eliminar contactos** - Borra contactos que ya no necesites

## ¿Qué tecnologías usé?

- **Python** - Para la lógica del servidor
- **web.py** - Un framework web sencillo
- **SQLite** - Para guardar los datos
- **HTML y CSS** - Para que se vea bonito

## � Archivos del proyecto

```
Agenda/
├── app.py                 # Aquí está toda la lógica
├── agenda.db             # Base de datos con los contactos
├── agenda.sql            # Script para crear la base de datos
├── templates/            # Las páginas web
│   ├── personas.html     # Página principal
│   ├── detalle.html      # Ver un contacto
│   ├── editar.html       # Editar un contacto
│   └── borrar.html       # Confirmar eliminación
└── README.md             # Este archivo
```

## � ¿Cómo usar el proyecto?

### Paso 1: Instalar Python
Necesitas tener Python instalado en tu computadora.

### Paso 2: Instalar web.py
```bash
pip install web.py
```

### Paso 3: Ejecutar la aplicación
```bash
python app.py
```

### Paso 4: Abrir en el navegador
Ve a: `http://localhost:8080`

¡Y listo! Ya puedes usar tu agenda de contactos.

## 💻 ¿Cómo funciona?

### Página Principal
Aquí puedes ver todos tus contactos en una tabla y agregar nuevos contactos con un formulario simple.

### Ver Contacto
Haz clic en "Ver" para ver toda la información de un contacto.

### Editar Contacto
Haz clic en "Editar" para cambiar el nombre o email de un contacto.

### Eliminar Contacto
Haz clic en "Eliminar" y confirma si realmente quieres borrarlo.

## 🎨 ¿Cómo se ve?

El diseño es simple y limpio:
- Colores azules y grises
- Tablas organizadas
- Botones claros para cada acción
- Se adapta a celulares y computadoras

## 🔧 Detalles técnicos

### Base de datos
```sql
CREATE TABLE personas (
    id_persona INTEGER PRIMARY KEY AUTOINCREMENT,
    nombre TEXT NOT NULL,
    email TEXT NOT NULL UNIQUE
);
```

### Páginas disponibles
- `/` - Página principal con la lista
- `/detalle/1` - Ver contacto con ID 1
- `/editar/1` - Editar contacto con ID 1
- `/borrar/1` - Eliminar contacto con ID 1

## 🤝 ¿Quieres contribuir?

Si tienes ideas para mejorar el proyecto:
1. Haz un fork del repositorio
2. Crea una nueva rama
3. Haz tus cambios
4. Envía un pull request

¡Gracias por ver mi proyecto! 😊


