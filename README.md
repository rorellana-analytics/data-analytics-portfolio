# 📊 Portafolio de Análisis de Datos — Rafael Ernesto Orellana Giménez

Repositorio de proyectos de análisis de datos y visualización en Python: limpieza, modelado relacional, análisis exploratorio, visualización y recomendaciones de negocio.

[GitHub](https://github.com/rorellana-analytics) · [LinkedIn](https://www.linkedin.com/in/rafael-ernesto-orellana-gim%C3%A9nez-700346264)

## 🛠️ Stack
- **Lenguaje:** Python 3
- **Datos:** Pandas, NumPy, SciPy
- **Visualización:** Matplotlib, Seaborn
- **Entornos:** Google Colab, Jupyter Notebook, VS Code, Git / GitHub

## 🚀 Proyecto 1: Ventas en Europa y Asia (2010–2017)
Archivo: `Analisis_Ventas_Globales_Python.ipynb`. El nombre conserva «Globales» por exigencia de la evaluación; el análisis **no es global**.

**Pregunta:** ¿Qué categorías y países aportan más beneficio y dónde conviene concentrar esfuerzo?

> **Origen de los datos:** `events.csv`, `products.csv` y `countries.csv` son un conjunto ficticio, trabajado en el curso *Google Sheets* de la plataforma Kodree. No son registros de una empresa real.

**Datos:** 1,328 pedidos, 12 categorías y 45 países de 2 regiones, de enero de 2010 a julio de 2017.

**Proceso:**
- Se conserva el código ISO `'NA'` de Namibia (`keep_default_na=False`).
- Se normalizan canal, prioridad y códigos de país, y se validan fechas y costos.
- Se eliminan 2 pedidos sin `Units Sold`. No se imputan.
- 82 pedidos (6.2 %) sin país se etiquetan «Sin asignar» y se excluyen de los cortes geográficos.
- Pruebas estadísticas con α = 0.05 (Kruskal-Wallis, Mann-Whitney, Pearson, Spearman, chi-cuadrado).

**Hallazgos:**
1. **La categoría decide el beneficio.** Cosmetics, Office Supplies, Household y Baby Food suman 59.4 %. Personal Care, Beverages y Fruits suman 5.0 %. No hay una regla 80/20. Beverages tiene margen de 33 %, pero su precio unitario es bajo.
2. **Los países no se diferencian.** Beneficio por pedido entre países: p = 0.974.
3. **Canal, envío y día de la semana no explican el beneficio.** Reparto casi 50/50 entre Offline y Online (p = 0.664). Envío vs beneficio: r = 0.060 (r² = 0.36 %). Envío promedio: 24.8 días.

**Recomendación:** priorizar por categoría y revisar los precios de las de menor aporte.

**Limitaciones:** datos simulados con precio y costo fijos por producto, solo 2 regiones, un solo producto por pedido (sin venta cruzada) y 2017 parcial.

**Uso:** abre el notebook en Colab y ejecuta todas las celdas. Los gráficos se guardan en `Images/`.

## 📂 Estructura
├── Data/ # CSV fuente (eventos, productos y países)
├── Images/ # Gráficos exportados
├── Analisis_Ventas_Globales_Python.ipynb # Cuaderno principal
├── requirements.txt # Dependencias
├── LICENSE # MIT (aplica al código, no a los datos)
└── README.md # Documentación

*Los datos pertenecen a su fuente (Kodree).*
