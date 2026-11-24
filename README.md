# data-analytics-portfolio
Analisis_Ventas_Globales_Python.ipynb

# 📊 Portafolio de Análisis de Datos — Rafael Ernesto Orellana Giménez

Bienvenido a mi repositorio de proyectos de **Análisis de Datos y Visualización**. Aquí documento casos prácticos de extremo a extremo (limpieza de datos, modelado relacional, análisis exploratorio, visualización y recomendaciones de lógica de negocio) desarrollados en **Python**.

---

## 🛠️ Stack Tecnológico y Herramientas
* **Lenguaje:** Python 3
* **Manipulación y Limpieza de Datos:** Pandas, NumPy
* **Visualización de Datos:** Matplotlib, Seaborn
* **Entornos de Desarrollo:** Google Colab, Jupyter Notebook, VS Code, Git / GitHub

---

## 🚀 Proyectos Destacados

### 1. Análisis Integral de Ventas Globales y Rentabilidad (`Analisis_Ventas_Globales_Python.ipynb`) — Ejercicio de Práctica con Datos Ficticios
- **Objetivo:** Limpiar, integrar y analizar un conjunto de datos ficticio / simulado (procedente de un curso finalizado) sobre operaciones en canales físicos (`Offline`) y digitales (`Online`), evaluando rentabilidad, clasificación Pareto / ABC, eficiencia logística y estacionalidad con fines demostrativos de portafolio.
- **Arquitectura de Datos:** Integración relacional (`merge`) de 3 archivos ficticios de curso:
  - `events.csv` (1,330 transacciones en Python frente a 1,328 en la depuración sin vacíos de hojas de cálculo).
  - `products.csv` (catálogo de productos y categorías).
  - `countries.csv` (base geográfica de 249 países y regiones).
- **Proceso Técnico Aplicado:**
  - Auditoría y tratamiento de valores faltantes (82 registros / 6.17 % sin `Country Code` etiquetados como `Unknown` e imputación de 2 nulos / 0.15 % en `Units Sold` por mediana de `Product ID`).
  - Estandarización de categorías (`"online"` → `"Online"`), preservación del código ISO de Namibia (`NA`), neutralización de homógrafos cirílicos y validación de integridad de fechas y costos.
  - Cálculo de KPIs, curva Pareto / ABC, análisis de correlación (`r ≈ 0.0607`) y visualizaciones multidimensionales (`barplot`, `boxplot`, `regplot`, series temporales y `heatmap`).
- **Principales Hallazgos (Dataset Simulado):**
  - **Métricas Globales del Ejercicio:** `\$1,704.56M USD` en ingresos y `\$501.83M USD` de beneficio neto (margen del **29.44 %**) en 45 países identificados (`df_geo`).
  - **Rentabilidad vs. Volumen:** `Cosmetics` (`\$92.72M USD`), `Office Supplies` (`\$77.98M USD`) y `Household` (`\$72.96M USD`) concentran cerca del **48.6 %** del beneficio total, mientras que líneas de alto volumen como `Beverages` o `Fruits` muestran menor margen relativo.
  - **Canales:** Participación equilibrada entre `Offline` (**50.2 %**) y `Online` (**49.8 %**).
  - **Logística y Beneficio:** Correlación lineal baja (`r ≈ 0.0607`) entre días de envío (promedio de **24.78 días**) y beneficio neto por pedido.
[![Abrir en Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1G6EeJQ4nEm3jKe3V5VHWfRaPCTXqF5gU?usp=sharing)

---

📂 Estructura del Repositorio
├── Data/                                   # Archivos fuente (CSV de eventos, productos y países)
├── images/                                   # Gráficos y visualizaciones exportadas del análisis
├── Analisis_Ventas_Globales_Python.ipynb   # Cuaderno principal con código, gráficos e informe ejecutivo
├── requirements.txt                        # Dependencias y librerías del proyecto
├── LICENSE                                 # Licencia MIT
└── README.md                               # Documentación del portafolio
