# Sesión 07 | Laboratorio Antigravity
## Guía de Ejecución Local (SQLite)

Esta guía te explica cómo realizar el "Interrogatorio" de datos (SELECT y WHERE) usando la base de datos completa de NovaMarket en VS Code.

---

## 1. Conexión a la Base de Datos
Ya hemos preparado una base de datos con 500 transacciones reales para ti.

1.  **Ubicación:** Entra a la carpeta `02_Sesion_07` desde tu explorador de VS Code.
2.  **Archivo:** Localiza el archivo **`novamarket_s07.db`**.
3.  **Configurar SQLTools:** 
    - Ve al cilindro de SQLTools.
    - Crea una nueva conexión (Add New Connection).
    - Nombre: `NovaMarket_S07`.
    - Database File: Selecciona `02_Sesion_07/novamarket_s07.db`.
    - Haz clic en **CONNECT**.

---

## 2. Ejecutar las Consultas (Laboratorio)

1.  Abre el archivo **`03_Laboratorio_S07.sql`**.
2.  **Verificación Inicial:** Copia y ejecuta este bloque para confirmar que tienes los 500 registros:
    ```sql
    SELECT 'DimProducto' AS Tabla, COUNT(*) AS Registros FROM DimProducto
    UNION ALL SELECT 'DimCiudad',  COUNT(*) FROM DimCiudad
    UNION ALL SELECT 'DimFecha',   COUNT(*) FROM DimFecha
    UNION ALL SELECT 'FactVentas', COUNT(*) FROM FactVentas;
    ```
3.  **Exploración (Bloque A):** Ejecuta las primeras líneas para ver las 500 ventas:
    ```sql
    SELECT * FROM FactVentas LIMIT 10;
    ```
4.  **Filtros con WHERE (Bloques B y C):** Sigue los ejemplos de la guía conceptual y aplícalos en tu archivo de laboratorio.

---

## 3. Desafíos Autónomos

Al final de tu archivo SQL encontrarás desafíos. Resuélvelos usando lo aprendido.

---

## 4. Proceso de Carga (Excel a BD)
Para este laboratorio, seguimos un flujo de ingeniería de datos estándar:

1.  **Limpieza (Power Query):** Los datos originales fueron procesados en Excel usando Power Query para eliminar nulos y estandarizar formatos (visto en `S03_Ventas_Datos_Limpios_Power_Query.xlsx`).
2.  **Modelado:** Creamos un modelo relacional con 3 dimensiones (`DimProducto`, `DimCiudad`, `DimFecha`) y una tabla de hechos (`FactVentas`).
3.  **Carga SQL:** Los 500 registros limpios se convirtieron en sentencias `INSERT` dentro del script `05_Script_Carga_DB_S07.sql`.
4.  **Validación:** Hemos verificado que la base de datos `00_Base_Datos_S07.db` contiene exactamente los mismos 500 registros que el archivo Excel procesado.

> [!TIP]
> **Pide ayuda a Antigravity:** Si no sabes cómo filtrar por un rango de fechas, utiliza el chat y pregunta: *"@antigravity, ¿cómo uso BETWEEN para filtrar el mes de noviembre de 2023?"*

---
*Sesión 07 | Antigravity Lab | NovaMarket Tech*
