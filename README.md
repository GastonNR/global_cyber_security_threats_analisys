# Trabajo Práctico N°7 - Análisis de Ciberseguridad con Apache Spark

## Descripción del Proyecto
Análisis comprehensivo de incidentes de ciberseguridad globales (2015-2024) utilizando PySpark, Delta Lake y Databricks para el procesamiento y análisis de datos a gran escala.

## Objetivos del Análisis
- Realizar análisis exploratorio de datos de ciberseguridad globales
- Aplicar transformaciones y limpieza de datos con Apache Spark
- Implementar almacenamiento eficiente con Delta Lake
- Crear visualizaciones interactivas y extraer insights accionables
- Identificar patrones y tendencias en incidentes de seguridad

## Stack Tecnológico
- **Apache Spark 3.5+**: Procesamiento distribuido de datos
- **PySpark**: API de Python para Spark
- **Delta Lake**: Almacenamiento de datos transaccional
- **Unity Catalog**: Gobierno y gestión de metadatos
- **Matplotlib**: Visualización de datos
- **Databricks**: Plataforma de analytics unificada
- **Python 3.11**: Lenguaje de programación principal

## Estructura del Proyecto
~~~
trabajo-practico-7-cybersecurity/
├── notebooks/
│   └── cybersecurity_analysis.ipynb
├── data/
│   └── datasets/
├── docs/
│   └── images/
├── README.md
└── requirements.txt
~~~

## Dataset Analizado
- **Nombre**: `global_cybersecurity_threats_2015_2024`
- **Registros**: 3,000 incidentes de ciberseguridad
- **Período Temporal**: 2015 - 2024
- **Características Principales**:
  - Country: País donde ocurrió el incidente
  - Year: Año del incidente
  - Attack Type: Tipo de ataque cibernético
  - Target Industry: Industria objetivo del ataque
  - Financial Loss (in Million $): Pérdida financiera en millones USD
  - Number of Affected Users: Cantidad de usuarios afectados
  - Attack Source: Fuente/origen del ataque
  - Security Vulnerability Type: Tipo de vulnerabilidad explotada
  - Defense Mechanism Used: Mecanismo de defensa utilizado
  - Incident Resolution Time (in Hours): Tiempo de resolución en horas

## Guía de Ejecución

### Prerrequisitos
- Cuenta en Databricks
- Cluster con Databricks Runtime 13.3 LTS o superior
- Acceso a Unity Catalog
- Permisos para crear tablas y volúmenes

### Pasos de Implementación

#### Configuración del Entorno
~~~python
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName("Cybersecurity-Analysis").getOrCreate()
~~~

#### Carga de Datos
~~~python
df = spark.table("workspace.default.global_cybersecurity_threats_2015_2024")
~~~

#### Ejecución del Análisis
- Ejecutar las celdas del notebook en orden secuencial
- Verificar transformaciones y validaciones
- Revisar visualizaciones generadas

## Metodología de Análisis

### 1. Exploración Inicial
- Análisis de estructura y calidad de datos
- Identificación de valores nulos y duplicados
- Estadísticas descriptivas básicas

### 2. Transformación de Datos
- Limpieza y estandarización de campos de texto
- Creación de columnas calculadas (categorías de severidad)
- Manejo de valores atípicos (outliers)
- Agregaciones y agrupamientos

### 3. Almacenamiento Delta Lake
- Persistencia en formato Delta
- Validación de integridad de datos
- Implementación de características ACID

### 4. Análisis y Visualización
- Consultas SQL avanzadas
- Gráficos de tendencias temporales
- Análisis comparativos por categorías
- Identificación de patrones

## Hallazgos Principales

### Tendencias Temporales
- Evolución de incidentes por año
- Patrones estacionales identificados
- Crecimiento en frecuencia y impacto

### Análisis por Categorías
- **Tipos de Ataque Más Frecuentes**: Phishing, Malware, DDoS
- **Industrias Más Afectadas**: Banca, Salud, Tecnología
- **Países con Mayor Impacto**: Análisis geográfico de incidentes
- **Mecanismos de Defensa Más Efectivos**: Evaluación comparativa

### Impacto Económico
- Pérdidas financieras agregadas por industria
- Costo promedio por incidente
- Relación entre tiempo de resolución y pérdidas

## Visualizaciones Incluidas
1. Evolución Temporal de Incidentes (Gráfico de líneas)
2. Tipos de Ataque Más Frecuentes (Gráfico de barras)
3. Industrias Más Afectadas (Gráfico de barras)
4. Pérdida Financiera Promedio por Año (Gráfico de líneas)
5. Países con Mayor Pérdida Financiera (Gráfico de barras)
6. Tiempo de Resolución por Tipo de Ataque (Gráfico de barras)

## Insights y Recomendaciones

### Para Empresas
- Fortalecer defensas contra tipos de ataques más frecuentes
- Implementar mecanismos de respuesta rápida
- Desarrollar planes de continuidad del negocio

### Para Desarrolladores
- Priorizar parches para vulnerabilidades más explotadas
- Implementar controles de seguridad en etapas tempranas
- Adoptar prácticas de secure coding

### Para Policy Makers
- Desarrollar regulaciones específicas por industria
- Fomentar colaboración público-privada
- Establecer estándares de reporting de incidentes

## Cómo Extender el Análisis

### Análisis Adicionales Posibles
- Predicción de incidentes usando Machine Learning
- Análisis de sentimiento en descripciones de incidentes
- Clusterización de patrones de ataque
- Análisis de red de actores de amenazas

### Integraciones Futuras
- Conexión con feeds de threat intelligence en tiempo real
- Dashboard interactivo con Streamlit o Plotly Dash
- Alertas automáticas basadas en patrones
- API REST para consulta de resultados

## Autor
**Tu Nombre**
- LinkedIn: [Tu perfil de LinkedIn]
- Email: tu.email@dominio.com
- GitHub: [tu-usuario-github]

## Licencia
Este proyecto es desarrollado con fines educativos y de investigación. Los datos utilizados son anónimos y agregados para preservar la confidencialidad.

## Contribuciones
Las contribuciones son bienvenidas. Por favor:
1. Fork el proyecto
2. Crea una rama para tu feature (git checkout -b feature/AmazingFeature)
3. Commit tus cambios (git commit -m 'Add some AmazingFeature')
4. Push a la rama (git push origin feature/AmazingFeature)
5. Abre un Pull Request

## Soporte
Si tienes preguntas o encuentras issues:
- Abre un issue en el repositorio GitHub
- Contacta al autor via email
- Revisa la documentación de Databricks para troubleshooting
