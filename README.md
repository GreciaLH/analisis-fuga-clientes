# 📊 Análisis de Fuga de Clientes (Customer Churn Analysis)

Un análisis completo de fuga de clientes para una empresa de telecomunicaciones utilizando técnicas de Machine Learning y visualización de datos.

## 🎯 Objetivo del Proyecto

Este proyecto tiene como objetivo identificar los factores que contribuyen a la fuga de clientes en una empresa de telecomunicaciones y desarrollar un modelo predictivo que permita:

- **Identificar clientes en riesgo** de abandonar el servicio
- **Descubrir patrones y causas** principales de la fuga
- **Proporcionar insights accionables** para estrategias de retención
- **Cuantificar el impacto** de diferentes factores en la decisión de abandono

## 📈 Resultados Clave

### Magnitud del Problema
- **Tasa de fuga actual: 26.54%** (1,869 de 7,043 clientes)
- Uno de cada cuatro clientes abandonó la compañía en el período analizado

### Principales Hallazgos

#### 🔥 Factores Críticos que Impulsan la Fuga:
1. **Tipo de Contrato**: Clientes con contratos mes a mes tienen una tasa de fuga dramáticamente mayor
2. **Configuración del Servicio**: Clientes con fibra óptica sin servicios adicionales (seguridad, soporte) son altamente propensos a irse
3. **Método de Pago**: El cheque electrónico genera mayor fricción y abandono
4. **Antigüedad**: Los primeros 12 meses son críticos - clientes nuevos tienen mayor riesgo

#### 🛡️ Factores que Promueven la Retención:
1. **Contratos a largo plazo** (1-2 años)
2. **Servicios adicionales** (seguridad online, soporte técnico)
3. **Métodos de pago automáticos** (tarjeta de crédito, transferencia bancaria)
4. **Relación establecida** (clientes con más de 48 meses)

## 🔧 Tecnologías Utilizadas

```python
# Librerías principales
pandas          # Manipulación de datos
numpy           # Operaciones numéricas
matplotlib       # Visualización básica
seaborn         # Visualización estadística
scikit-learn     # Machine Learning
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

# Instalar dependencias
pip install pandas numpy matplotlib seaborn scikit-learn

# Ejecutar Jupyter Notebook
jupyter notebook eda.ipynb
```

### Ejecución
1. Abrir `eda.ipynb` en Jupyter Notebook
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

### Rendimiento
- **Precisión general**: ~80%
- **Identificación de churn**: Alto recall para clientes en riesgo
- **Interpretabilidad**: Coeficientes claros para cada factor de riesgo

### Factores más Influyentes (según el modelo)
1. Contrato mes a mes vs. contratos largos
2. Servicios de seguridad y soporte técnico
3. Método de pago electrónico
4. Antigüedad del cliente
5. Tipo de servicio de internet

## 💡 Recomendaciones de Negocio

### Acciones Inmediatas
1. **Incentivos para contratos largos**: Descuentos o beneficios para contratos anuales
2. **Mejora del onboarding**: Programa especial para primeros 12 meses
3. **Promoción de servicios adicionales**: Bundles atractivos con seguridad y soporte
4. **Optimización de pagos**: Migrar usuarios de cheque electrónico a métodos automáticos

### Estrategias a Medio Plazo
1. **Segmentación proactiva**: Identificar clientes en riesgo antes de que se vayan
2. **Programa de retención**: Contacto proactivo con clientes de alto riesgo
3. **Mejora de experiencia**: Especial atención a clientes con fibra óptica
4. **Análisis de competencia**: Entender por qué se van los clientes premium

## 👨‍💻 Autor

**Tu Nombre**
- LinkedIn: [tu-perfil]
- Email: [tu-email]
- GitHub: [tu-github]

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para detalles.

---

**Nota**: Este análisis es con fines educativos y de demostración. Los datos utilizados son de dominio público y no contienen información sensible real de clientes.
