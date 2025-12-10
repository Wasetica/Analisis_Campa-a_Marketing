# Analisis_Campaña_Marketing



📌 Descripción del Proyecto
Análisis de Componentes Principales (PCA) aplicado a datos de clientes de Quantum Retail para reducir dimensionalidad e identificar patrones de comportamiento. Este estudio forma parte del programa de formación "Gestión de datos en modelos de inteligencia artificial" del SENA.

🎯 Objetivo
Reducir la dimensionalidad de un dataset de 10 variables a 4 componentes principales, manteniendo el 80% de la varianza original, para facilitar la segmentación de clientes en campañas de marketing.

🏗️ Estructura del Proyecto
text
AA2_EV01_Campana_Marketing/
│
├── AA2_EV01_Campana_Marketing.ipynb  # Cuaderno Jupyter principal
├── quantum_customer_data.csv         # Dataset generado (1000 clientes)
├── pca_components_results.csv        # Resultados PCA
├── pca_loadings_interpretation.csv   # Loadings de componentes
├── scaled_customer_data.csv          # Datos escalados
├── pca_metadata.json                 # Metadatos del análisis
└── README.md                         # Este archivo
📊 Dataset Generado
El dataset contiene información de 1,000 clientes con las siguientes variables:

Variable	Tipo	Descripción	Rango
CustomerID	String	Identificador único	CUST-0001 a CUST-1000
Age	Entero	Edad del cliente	18-70 años
AnnualIncome	Entero	Ingresos anuales (miles USD)	20-150
SpendingScore	Entero	Puntuación de gasto	1-100
WebVisits	Entero	Visitas al sitio web/año	0-30
DaysSinceLastPurchase	Entero	Días desde última compra	0-365
EmailsOpened	Entero	Correos marketing abiertos	0-100
AdClicks	Entero	Clics en anuncios digitales	0-50
SocialMediaInteractions	Entero	Interacciones en redes	0-200
AvgSessionDuration	Decimal	Duración sesión web (minutos)	1.0-30.0
ItemsInCart	Entero	Artículos en carrito promedio	0-15
🔄 Flujo de Análisis
Paso 1: Generación de Datos
python
np.random.seed(42)  # Para reproducibilidad
# Generación de 1000 clientes con distribución aleatoria controlada
Paso 2: Análisis Exploratorio (EDA)
Estadísticas descriptivas

Distribuciones de variables

Matriz de correlación

Identificación de patrones iniciales

Paso 3: Preparación de Datos
Exclusión de CustomerID (identificador sin valor predictivo)

Estandarización con StandardScaler

Justificación técnica del escalado

Paso 4: Aplicación de PCA
Cálculo de componentes principales

Análisis de varianza explicada

Selección de 4 componentes (80% varianza)

Paso 5: Interpretación
Análisis de loadings

"Bautizo" de componentes con nombres de negocio

Visualización en espacio 2D

📈 Resultados Clave
Componentes Principales Identificados
Componente	Nombre	Varianza	Variables Principales
PC1	Compromiso Digital y Actividad	23.9%	EmailsOpened, AdClicks, SocialMediaInteractions
PC2	Poder Adquisitivo y Frecuencia	21.7%	AnnualIncome, DaysSinceLastPurchase
PC3	Comportamiento de Compra Online	15.8%	SpendingScore, ItemsInCart
PC4	Eficiencia de Navegación	14.0%	Age, AvgSessionDuration
Varianza total explicada: 75.4%

🎯 Implicaciones para Marketing
Segmentación Propuesta
Digitalmente Activos (Alto PC1): Campañas en redes sociales y email

Alto Valor (Alto PC2): Productos premium y programas de fidelización

Compradores Online (Alto PC3): Ofertas y facilitación de checkout

Navegadores Eficientes (Alto PC4): Experiencias mobile-first rápidas

🛠️ Requisitos Técnicos
Dependencias
bash
python>=3.8
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=0.24.0
jupyter>=1.0.0
Instalación
bash
# Clonar repositorio
git clone https://github.com/tuusuario/AA2-EV01-Campana-Marketing.git

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar Jupyter Notebook
jupyter notebook AA2_EV01_Campana_Marketing.ipynb
📋 Checklist de Entregables
Cuaderno Jupyter ejecutable

Dataset generado (quantum_customer_data.csv)

Análisis EDA completo

Aplicación correcta de PCA

Selección justificada de componentes

Interpretación de componentes con nombres de negocio

Visualizaciones claras y etiquetadas

Conclusiones relevantes para marketing

🚀 Próximos Pasos
Este análisis sirve como base para:

AA2-EV02: Aplicación de clustering K-Means

Segmentación de clientes para campaña "Aura Pro"

Desarrollo de estrategias de marketing personalizadas

📚 Referencias Técnicas
Documentación oficial de scikit-learn PCA

"An Introduction to Statistical Learning" - James et al.

Guía de aprendizaje SENA - GFPI-F-135 V04

👥 Autor
Estudiante SENA
Programa: Gestión de datos en modelos de inteligencia artificial
Código: 21710120
Competencia: 220501115 - Integrar datos según procedimiento técnico

📄 Licencia
Este proyecto es parte de un programa educativo del SENA. Uso exclusivo con fines académicos.
