# 📓 Laboratorio de SQL: NovaMarket Tech (v3)

¡Bienvenidos al "Interrogatorio" de datos! En este espacio usaremos **SQL** para descubrir por qué NovaMarket está perdiendo dinero a pesar de vender récords.

---

## 🛠️ Guía Rápida: Cómo usar este espacio

Tienes dos formas de trabajar: la **Terminal** (rápida y técnica) y las **Extensiones** (visual y cómoda).

### 1. El Camino del Guerrero (Terminal)
Es la forma más directa de hablar con la base de datos. 

*   **¿Dónde ejecuto esto?** En la pestaña "Terminal" de VS Code (asegúrate de que estás en la carpeta `/SQL`).
*   **Comando para entrar:** 
    ```bash
    sqlite3 novamarket_v3.db
    ```
    *(Esto "despierta" al motor de SQLite y le dice que trabaje sobre ese archivo).*

*   **Reglas de Oro en la Terminal:**
    1.  **Comandos de Punto (Internos):** Empiezan con punto y **no** llevan punto y coma.
        *   `.tables`: Muestra qué tablas existen.
        *   `.schema NombreTabla`: Muestra la estructura de esa tabla.
        *   `.exit` o `.quit`: Salir de la base de datos.
    2.  **Sentencias SQL:** **SIEMPRE terminan en punto y coma (`;`)**.
        *   `SELECT * FROM FactVentas;`
        *   *Si olvidas el `;`, la terminal te mostrará `...>` esperando a que lo pongas.*

---

### 2. El Camino del Maestro (Extensiones Visuales)
Esto es lo que viste en tu pantallazo. Aquí está el paso a paso para configurarlo:

#### Configurar SQLTools (Para ejecutar líneas con Cmd+E)
1.  Haz clic en el icono de **SQLTools** en la barra lateral izquierda (parece un cilindro de base de datos).
2.  Haz clic en el botón **"+" (Add Connection)** en la sección de Connections.
3.  Selecciona el proveedor: **SQLite**. 
    *   *(Si no aparece, instala la extensión "SQLTools SQLite/Bun/DuckDB Driver").*
4.  En **Connection Name**, escribe: `NovaMarket`.
5.  En **Database File**, haz clic en "Select from file" y busca el archivo `novamarket_v3.db` en tu carpeta.
6.  Haz clic en **Save Connection** y luego en **Connect**.
7.  **Ahora sí:** Ya puedes ir a tus archivos `.sql`, seleccionar una línea y presionar `Cmd+E` para ver los resultados en una ventana interactiva.

#### Configurar SQLite Viewer (Estilo Excel)
*   **¿Para qué sirve?** Ver la tabla completa de forma gráfica sin escribir código.
*   **¿Cómo se usa?** Haz clic derecho en el archivo `novamarket_v3.db` en el explorador de archivos -> **Open With...** -> **SQLite Viewer**.

---

## 📂 Estructura del Aprendizaje
- `novamarket_v3.db`: El "cerebro" donde viven los datos.
- `S06_El_Contrato/`: Integridad y reglas (Sesión actual).
- `S07_El_Interrogatorio/`: Consultas precisas.
- `S08_El_Arte_Resumir/`: Agregaciones (Confirmando por qué perdemos dinero).
- `S09_El_Puente/`: JOINs (Uniendo datos de varias tablas).

---
> [!TIP]
> **Consejo:** Empieza usando la terminal para los comandos simples (`.tables`) y usa **SQLTools** (Cmd+E) para las consultas largas que estás escribiendo en los archivos `.sql`.
