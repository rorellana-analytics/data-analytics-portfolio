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
> **Nota de origen y transparencia de datos:** Las tablas utilizadas (`events.csv`, `products.csv` y `countries.csv`) corresponden a un conjunto de datos ficticio / simulado desarrollado y trabajado en el marco de un curso realizado en la institución Kodree, y no a registros comerciales o contables de una empresa real. Los importes elevados y las escalas de las métricas reflejan la estructura del ejercicio de práctica y no deben interpretarse como estados financieros auditados.

- **Objetivo:** Limpiar, integrar y analizar un conjunto de datos ficticio / simulado (procedente de una práctica formativa en Kodree) sobre operaciones en canales físicos (`Offline`) y digitales (`Online`), evaluando rentabilidad, clasificación Pareto / ABC, dispersión logística y dinámica temporal con fines demostrativos de portafolio.
- **Arquitectura de Datos:** Integración relacional (`left join` / `merge`) de 3 archivos ficticios de curso:
  - `events.csv` (1,330 transacciones en Python frente a 1,328 en la depuración sin vacíos de hojas de cálculo).
  - `products.csv` (catálogo de 12 categorías de productos).
  - `countries.csv` (base geográfica de territorios y regiones).
- **Proceso Técnico Aplicado:**
  - Conservación del código ISO alpha-2 `'NA'` de Namibia (`keep_default_na=False`) para evitar que se interprete como valor nulo (`NaN`).
  - Auditoría de caracteres no ASCII / posibles homógrafos cirílicos, limpieza de espacios y mayúsculas/minúsculas (`"online"` → `"Online"`), y validación de fechas y costos unitarios.
  - Tratamiento de 82 registros (6.17 %) sin `Country Code` etiquetados como `'Unknown'` en las métricas globales y excluidos en los cortes geográficos (`df_geo`), junto con la imputación de 2 nulos (0.15 %) en `Units Sold` por mediana de `Product ID` (conservando los 1,330 pedidos).
  - Cálculo de KPIs globales, clasificación Pareto / ABC, análisis de correlación lineal y varianza explicada ($r \approx 0.0607$, $r^2 < 1\%$) y visualizaciones (`barplot`, `boxplot`, `regplot`, series temporales y `heatmap`).
- **Principales Hallazgos y Alcance (Dataset Simulado):**
  - **Cobertura y Escala:** 1,330 pedidos y 45 países identificados en `df_geo` (con concentración en Europa y Asia); las cifras exactas de ingresos, costos, beneficio neto, margen y ticket promedio se leen directamente desde las salidas calculadas en el cuaderno.
  - **Rentabilidad, Volumen y Pareto / ABC:** `Cosmetics`, `Office Supplies` y `Household` encabezan el beneficio neto y concentran cerca del **48.6 %** del beneficio total (sin seguir una regla 80/20 estricta). Al analizar categorías de alto volumen como `Beverages` o `Fruits`, conviene distinguir entre precio unitario / volumen y margen porcentual.
  - **Canales:** Reparto cercano al **50 % / 50 %** entre `Offline` y `Online`.
  - **Logística y Beneficio:** Promedio de envío cercano a **24.78 días** (rango de 0 a 50 días) y correlación lineal baja con el beneficio por pedido ($r \approx 0.0607$, con alta dispersión y sin observar variables operativas externas como cancelaciones, devoluciones o satisfacción). Dado que cada `Order ID` corresponde a un solo ítem, no se plantean recomendaciones de venta cruzada sobre canastas.

[![Abrir en Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1G6EeJQ4nEm3jKe3V5VHWfRaPCTXqF5gU?usp=sharing)

---

📂 Estructura del Repositorio
├── Data/                                   # Archivos fuente (CSV de eventos, productos y países)
├── images/                                   # Gráficos y visualizaciones exportadas del análisis
├── Analisis_Ventas_Globales_Python.ipynb   # Cuaderno principal con código, gráficos e informe ejecutivo
├── requirements.txt                        # Dependencias y librerías del proyecto
├── LICENSE                                 # Licencia MIT
└── README.md                               # Documentación del portafolio
