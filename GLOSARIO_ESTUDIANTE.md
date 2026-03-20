# 📙 GLOSARIO: Conceptos Básicos de SQL (NovaMarket)

Este documento es una "hoja de ruta" para que los estudiantes entiendan qué está pasando bajo el capó.

---

## 1. El Entorno de Trabajo

### ¿Qué es la Terminal?
Es la ventana de texto (la línea de comandos) donde "hablamos" directamente con el sistema operativo. En este laboratorio, la usamos para ejecutar el motor de base de datos.

### ¿Qué es SQLite / SQLite3?
Es el **Motor de Base de Datos**. A diferencia de otros (como MySQL o Oracle), SQLite no necesita un servidor complejo; toda la base de datos es un simple archivo en tu computadora.
*   `sqlite3`: Es el comando que activa el motor en la terminal.

### ¿Qué es el archivo `.db` (`novamarket_v3.db`)?
Es el **Contenedor**. Aquí es donde vive toda la información (ventas, productos, ciudades). Si borras este archivo, borras todo el negocio.

### ¿Qué es un archivo `.sql`?
Es un **Guion (Script)**. Es una lista de instrucciones que ya escribiste en un editor (como VS Code) para no tener que teclearlas una por una en la terminal cada vez.

---

## 2. Los Comandos de Poder

| Comando | Tipo | ¿Para qué sirve? |
| :--- | :--- | :--- |
| `sqlite3 archivo.db` | Terminal | Abre la base de datos y activa el motor. |
| `.tables` | Punto | Muestra un índice de todas las tablas en la base de datos. |
| `.schema Tabla` | Punto | Te enseña "cómo fue construida" la tabla (sus columnas). |
| `.exit` | Punto | Cierra la conexión y vuelve a la terminal normal de Mac. |
| `SELECT ...;` | SQL | La pregunta mágica. Sirve para extraer datos específicos. |
| `PRAGMA ...;` | SQL | Comandos especiales de SQLite para consultar metadatos técnicos. |

---

## 3. ¿Qué significan estos nombres raros?

### `sqlite_master` 📖
Es la **Tabla Mestra**. Es el "libro de registro" secreto que SQLite usa para acordarse de qué tablas has creado. Si le preguntas a esta tabla, ella te dirá todo lo que sabe sobre la estructura de tu proyecto.

### `PRAGMA table_info('MiTabla');` 🔍
Es como hacerle una "radiografía" a una tabla. Nos dice:
1.  Qué columnas tiene.
2.  Qué tipo de dato acepta (Número, Texto, Fecha).
3.  Si es obligatorio llenar ese dato (`NOT NULL`).

---

## 4. Diferencia entre Terminal y Extensiones (VS Code)

*   **En la Terminal:** Es el camino puro. Ves los datos como texto plano. Perfecto para rapidez y diagnóstico.
*   **En las Extensiones (SQLTools / SQLite Viewer):** Es el camino visual. Ves los datos en tablas bonitas (como Excel) y puedes ejecutar el código con un clic (`Cmd + E`).

> [!TIP]
> **Para el estudiante:** Aprende primero en la terminal para entender la lógica, y luego usa las extensiones para aumentar tu productividad.
