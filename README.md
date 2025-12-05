<h1 align="center">📘 Modelo de simulación para analizar los efectos del RIGI</h1>

Notebook en Python – Simulación microeconómica

Este repositorio contiene el notebook rigi.ipynb, donde se implementa un modelo microeconómico para simular posibles efectos del Régimen de Incentivos a Grandes Inversiones (RIGI) sobre el excedente del consumidor y el bienestar social, utilizando herramientas de teoría de juegos y resolución numérica.

El notebook reproduce el modelo planteado en el trabajo teórico original, implementando funciones de ingreso, costos, condiciones de primer orden y comparación entre escenarios estratégicos.

<h2 align="center">🎯 Objetivo del notebook</h2>

Construir y resolver numéricamente un modelo simplificado donde:

Dos empresas compiten en cantidades.

Los costos dependen de parámetros estructurales (a0, a1, a2, a3).

Se comparan escenarios con nuevos incentivos a la inversión (tipo RIGI) frente a escenarios base.

Se calcula el excedente del consumidor y la diferencia de bienestar.

Se generan gráficos y heatmaps que muestran cómo cambia el bienestar según los parámetros del modelo.

<h2 align="center">🧰 Contenido del código</h2>

El notebook incluye:

✔ Definición simbólica del modelo
q, b, a3, n = sp.symbols('q b a3 n')
qi, qj = sp.symbols('qi qj')
a, a0, a1, a2 = 150, 2.5, 2.5, 1.5

✔ Funciones de ingreso y costo
ingreso_C_2 = (a - b*(qi + qj)) * qi
costo_C_2   = a3*qi**3 + a2*qi**2 + a1*qi + a0

✔ Resolución numérica

Uso de fsolve y sympy.solve para obtener cantidades de equilibrio bajo distintos supuestos.

✔ Simulaciones

Variación de parámetros como:

b: pendiente de la demanda

a3: parámetro de costo marginal creciente

n: cantidad de empresas o nivel de inversión

✔ Visualización

Generación de:

Gráficos 3D (Axes3D)

Heatmaps (seaborn)

Gráficos comparativos de excedente del consumidor

Todo esto permite visualizar cómo cambia el bienestar social cuando se modifica la estructura de costos (por inversión inducida por el RIGI).

<h2 align="center">📂 Estructura del repositorio</h2>

/
├── rigi.ipynb     # Notebook con el modelo completo
└── README.md      # Descripción del proyecto

<h2 align="center">🛠 Tecnologías utilizadas</h2>

Python

SymPy (modelación simbólica)

SciPy (fsolve)

NumPy

Pandas

Matplotlib / Seaborn

Google Colab (versión original)

<h2 align="center">📈 ¿Qué permite hacer el notebook?</h2>

Resolver un modelo no lineal que no tiene solución analítica.

Analizar cómo cambios en costos afectan cantidades y bienestar.

Simular escenarios alternativos con parámetros económicos modificados.

Visualizar el impacto en el bienestar social mediante gráficos.

<h2 align="center">⚠️ Notas</h2>

El notebook no representa el texto completo de la tesis, sino únicamente la implementación computacional del modelo matemático utilizado para el análisis.

<h2 align="center">🧑‍💻 Autores</h2>

Rafael Barchiesi, Camila Marcó, Marina Pallucchini.
Notebook desarrollado como parte de un análisis académico del RIGI.
