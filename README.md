# 📊 Análisis de Fuga de Clientes (Customer Churn Analysis)

Un análisis completo de fuga de clientes para una empresa de telecomunicaciones utilizando técnicas de Machine Learning y visualización de datos.

## 🎯 Objetivo del Proyecto

Este proyecto tiene como objetivo identificar los factores que contribuyen a la fuga de clientes en una empresa de telecomunicaciones y desarrollar un modelo predictivo que permita:

- **Identificar clientes en riesgo** de abandonar el servicio
- **Descubrir patrones y causas** principales de la fuga
- **Proporcionar insights accionables** para estrategias de retención
- **Cuantificar el impacto** de diferentes factores en la decisión de abandono


## 🔧 Tecnologías Utilizadas

```python
# Librerías principales
pandas          # Manipulación de datos
numpy           # Operaciones numéricas
matplotlib      # Visualización básica
seaborn         # Visualización estadística
scikit-learn    # Machine Learning

# Librerías especializadas
imbalanced-learn # Técnicas de balanceo (SMOTE)
collections     # Análisis de distribuciones
warnings        # Manejo de alertas
```

## 📁 Estructura del Proyecto

```
analisis-fuga-clientes/
│
├── customer_churn.ipynb                    # Notebook principal con análisis completo
├── README.md                    # Documentación del proyecto
├── Telco-Customer-Churn.csv     # Dataset original
└── requirements.txt             # Dependencias (opcional)
```

## 🚀 Cómo Ejecutar el Proyecto

### Prerrequisitos
- Python 3.8 o superior
- Jupyter Notebook o JupyterLab
- Las librerías especificadas en la sección de tecnologías

### Instalación
```bash
# Clonar o descargar el proyecto
cd analisis-fuga-clientes

# Instalar dependencias básicas
pip install pandas numpy matplotlib seaborn scikit-learn

# Instalar dependencias adicionales para balanceo
pip install imbalanced-learn

# Ejecutar Jupyter Notebook
jupyter notebook customer_churn.ipynb
```

### Ejecución
1. Abrir `customer_churn.ipynb` en Jupyter Notebook
2. Ejecutar todas las celdas secuencialmente
3. El análisis está organizado en secciones lógicas para fácil seguimiento

## 📊 Dataset

### Descripción
- **Fuente**: Telco Customer Churn Dataset (Kaggle)
- **Tamaño**: 7,043 clientes con 21 características
- **Período**: Datos históricos de clientes de telecomunicaciones

### Variables Principales
- **Demográficas**: Género, edad (senior citizen), dependientes
- **Servicios**: Tipo de internet, servicios adicionales, tipo de contrato
- **Facturación**: Cargos mensuales, cargos totales, método de pago
- **Objetivo**: Churn (Si/No - cliente se fue o se quedó)

## 🧪 Metodología

### 1. Análisis Exploratorio de Datos (EDA)
- Calidad y limpieza de datos
- Análisis de distribuciones
- Identificación de patrones en variables categóricas y numéricas
- Visualizaciones comparativas por segmento de churn

### 2. Ingeniería de Características
- **TenureGroup**: Categorización de antigüedad (Nuevo/Estable/Leal)
- **NumAdditionalServices**: Contador de servicios adicionales contratados
- **One-Hot Encoding**: Conversión de variables categóricas

### 3. Modelado Predictivo
- **Algoritmo**: Regresión Logística (por interpretabilidad)
- **División**: 80% entrenamiento, 20% prueba
- **Preprocesamiento**: Escalado estándar de variables numéricas
- **Evaluación**: Métricas de precisión, recall, F1-score

## 📋 Resultados del Modelo

### Técnicas de Balanceo Evaluadas
El proyecto abordó el **problema crítico del desbalanceo de clases** (73% No Churn vs 27% Churn) implementando y comparando:

1. **SMOTE**: Sobremuestreo sintético de la clase minoritaria
2. **Class Weight Balancing**: Ajuste automático de pesos por clase
3. **Threshold Tuning**: Optimización del umbral de decisión ✅ **GANADOR**

### Rendimiento Final (Threshold Tuning)
- **Accuracy**: 80.4% - Precisión general excelente
- **Precision**: 50.4% - Balance aceptable de falsos positivos  
- **Recall**: 79.4% - **Detecta casi 8 de cada 10 clientes que se van**
- **F1-Score**: 0.617 - Mejor balance general entre métricas
- **Umbral optimizado**: 25% (vs 50% default)

### Mejora vs Modelo Base
- **Recall original**: 49.2% → **Recall final**: 79.4%
- **Mejora**: **+61.4%** en detección de clientes en riesgo
- **Impacto**: +113 clientes adicionales identificables para retención

### Factores más Influyentes (según el modelo)
1. **Contratos mes a mes** - Factor de riesgo #1
2. **Servicios de seguridad/soporte técnico** - Ausencia aumenta riesgo
3. **Método de pago electrónico** - Genera fricción y abandono
4. **Antigüedad del cliente** - Primeros 12 meses críticos
5. **Configuración fibra óptica** - Sin servicios adicionales problemática




## 📄 Licencia

Este proyecto está bajo la Licencia MIT.

---

**Nota**: Este análisis es con fines educativos y de demostración. Los datos utilizados son de dominio público y no contienen información sensible real de clientes.
