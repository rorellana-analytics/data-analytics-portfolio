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

### 1. Análisis Integral de Ventas Globales y Rentabilidad (`Analisis_Ventas_Globales_Python.ipynb`)
* **Objetivo:** Limpiar, integrar y analizar las operaciones comerciales de una empresa global que opera en canales físicos (`Offline`) y digitales (`Online`), evaluando rentabilidad, eficiencia logística y estacionalidad.
* **Arquitectura de Datos:** Integración relacional (`merge`) de 3 fuentes de datos:
  * `events.csv` (1,330 transacciones históricas).
  * `products.csv` (catálogo de 12 categorías de productos).
  * `countries.csv` (base geográfica de 249 países y regiones).
* **Proceso Técnico Aplicado:**
  * Auditoría y tratamiento de valores nulos (`6.17%` sin código de país etiquetados como `Unknown` e imputación por mediana en unidades vendidas).
  * Estandarización de categorías (`"online"` → `"Online"`), restauración del código ISO de Namibia (`NA`) y validación de integridad temporal (`0` fechas invertidas).
  * Cálculo de KPIs financieros, análisis de correlación y visualizaciones multidimensionales (`barplots`, `boxplots`, `regplots`, series temporales y mapas de calor).
* **Principales Hallazgos de Negocio:**
  * **Resultados Globales:** **\$1,704.56M USD** en ingresos totales y **\$501.83M USD** de beneficio neto (**margen global del 29.44%**) a través de **45 países**.
  * **Rentabilidad vs. Volumen:** *Cosmetics* (\$92.72M USD), *Office Supplies* (\$77.98M USD) y *Household* (\$72.96M USD) concentran casi la mitad de las ganancias totales, mientras que categorías de altísima rotación como *Beverages* o *Fruits* aportan márgenes reducidos.
  * **Omnicanalidad:** Participación equilibrada entre ventas *Offline* (`50.2%`) y *Online* (`49.8%`).
  * **Independencia Logística:** Correlación prácticamente nula ($r = 0.0607$) entre los días de envío (promedio de `24.78 días`) y el beneficio neto por pedido.
[![Abrir en Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rorellanagnez64-debug/data-analytics-portfolio/blob/main/Analisis_Ventas_Globales_Python.ipynb)

---

📂 Estructura del Repositorio
├── Data/                                   # Archivos fuente (CSV de eventos, productos y países)
├── images/                                   # Gráficos y visualizaciones exportadas del análisis
├── Analisis_Ventas_Globales_Python.ipynb   # Cuaderno principal con código, gráficos e informe ejecutivo
├── requirements.txt                        # Dependencias y librerías del proyecto
├── LICENSE                                 # Licencia MIT
└── README.md                               # Documentación del portafolio
