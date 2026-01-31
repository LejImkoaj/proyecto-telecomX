# proyecto-telecomX
📁 Estructura del Notebook

El notebook está organizado en tres secciones principales:
1. 📌 Extracción

    Carga del archivo TelecomX_Data.json.

    Normalización de columnas anidadas (customer, phone, internet, account) con pd.json_normalize().

    Creación de un DataFrame final con todas las columnas normalizadas.

2. 🔧 Transformación

    Normalización de nombres de columnas (minúsculas, sin espacios).

    Renombrado de columnas para mayor claridad.

    Detección y eliminación de valores vacíos en la columna churn.

    Conversión de tipos de datos (total_charges a float).

    Mapeo de valores categóricos (Yes/No) a binarios (1/0).

    Manejo de valores nulos en total_charges (asignación de 0 para clientes con tenure = 0).

    Creación de la columna cuentas_diarias = monthly_charges / 30.

3. 📊 Carga y Análisis

    Carga de datos limpios desde una API pública (GitHub).

    Análisis descriptivo con .describe().

    Visualización de la distribución de churn con matplotlib y seaborn.

    Cálculo de la tasa de churn y porcentajes.

🛠️ Tecnologías Utilizadas

    Python 3

    Pandas – Manipulación de datos

    Matplotlib / Seaborn – Visualización

    Requests – Consumo de API

    Jupyter Notebook – Entorno de desarrollo

📈 Resultados Clave

    Tasa de churn: 26.5% (1,869 clientes abandonaron de un total de 7,043).

    Clientes fieles: 73.5% (5,174 clientes).

    Valores nulos en total_charges: 11 registros, todos correspondientes a clientes con tenure = 0 (clientes nuevos sin cargos generados).

    Columna creada: cuentas_diarias para un análisis más granular del gasto de clientes.

📂 Archivos Generados

    TelecomX_Data.json – Datos originales.

    telecomX_normalizado_original.json – Datos normalizados (opcional).

    telecomX_ready_for_analysis.json – Dataset limpio y listo para análisis.

🚀 Instrucciones de Ejecución

    Clonar o descargar el notebook TelecomX_LATAM.ipynb.

    Asegurarse de tener el archivo TelecomX_Data.json en la ruta /content/ (si se usa Google Colab) o ajustar la ruta según el entorno local.

    Instalar dependencias:

bash

pip install pandas matplotlib seaborn requests

    Ejecutar las celdas en orden para reproducir el proceso ETL y análisis.

📌 Notas Adicionales

    Se eliminaron 224 registros con valores vacíos en churn (3.08% del total), considerando un impacto bajo en el análisis.

    Los valores nulos en total_charges se asociaron a clientes con tenure = 0 y se rellenaron con 0.

    El dataset final contiene 21 columnas y 7,043 filas después de la limpieza.

📄 Licencia

Este proyecto es de uso educativo y analítico. Los datos son ficticios o anonimizados, y el código puede reutilizarse bajo los términos de la licencia MIT.
✍️ Autor

Proyecto desarrollado como parte de un análisis de datos aplicado al sector telecomunicaciones en LATAM.

🔗 Enlace al dataset limpio:
https://raw.githubusercontent.com/LejImkoaj/proyecto-telecomX/refs/heads/main/json-files/telecomX_ready_for_analysis.json
