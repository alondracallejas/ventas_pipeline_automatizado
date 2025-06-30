# Proyecto: Trazabilidad y Automatización de Ventas 

Consolidar las ventas mensuales a partir de archivos pivoteados entregados por contabilidad. 
- Corregir problemas históricos de inconsistencias y falta de trazabilidad entre meses.
- Automatizar la transformación, limpieza y carga de datos a una base consolidada.
- Preparar los datos para modelos de predicción de churn y visualizaciones en Power BI / Streamlit.
- Aprender y documentar buenas prácticas de trabajo de datos en proyectos reales.

## 📁 Estructura del Proyecto 

'''text
proyecto_trazabilidad_ventas/
│
├── datos_mensuales/ # Archivos CSV mensuales de ventas (raw)
│ ├── ventas_enero.csv
│ ├── ventas_febrero.csv
│ └── ...
│
├── scripts/ # Código Python
│ └── consolidar_ventas.py # Script que transforma y consolida los datos
│
├── ventas_consolidadas.csv # Base consolidada en formato largo
│
├── dashboards/ # Dashboards y visualizaciones
│ ├── power_bi/ # Archivos de Power BI (.pbix)
│ └── streamlit/ # App de visualización interactiva
│
├── modelos/ # Modelos de churn y notebooks de análisis
│ └── churn_model.ipynb
│
└── README.md # Documentación del proyecto

⚙ Requisitos - Python 3.9+ - Pandas - (opcional) MySQL o SQLite local para persistencia de datos - Streamlit (para dashboard) - Power BI Desktop (para visualización) Instalar dependencias básicas: ```bash pip install pandas streamlit 

🧠 Lógica del Script de Consolidación

Cada archivo mensual:

Está pivoteado (una columna por mes)

Incluye datos acumulados de varios meses

Puede sobrescribir meses anteriores si contabilidad los modifica

Por lo tanto, el script:

Lee todos los archivos de datos_mensuales/

Convierte cada archivo a formato largo (cliente, fecha, monto)

Detecta el mes más reciente del archivo

Reemplaza ese mes en la base consolidada

Guarda el resultado final en ventas_consolidadas.csv

🚀 Próximos pasos

Añadir carga automática a SQL local

Entrenar un modelo de churn con la base consolidada

Visualizar resultados del modelo en Streamlit

Publicar un dashboard ejecutivo en Power BI

✍️ Autor

Este proyecto fue inspirado por experiencias reales en operaciones de datos.
Es un ejercicio para mejorar procesos, corregir errores comunes y construir flujos de datos confiables.

