# 📡 Proyecto ETL TelecomX

## 🎯 Descripción del Proyecto

Este proyecto desarrolla un pipeline completo de **ETL (Extract, Transform, Load)** para el análisis de datos de telecomunicaciones de la empresa TelecomX. El objetivo principal es extraer, limpiar, transformar y analizar datos de clientes para obtener insights valiosos sobre el comportamiento del usuario, patrones de churn y métricas de negocio.

## 🚀 Características Principales

### 📌 **Extracción de Datos (Extract)**
- Simulación de API REST de telecomunicaciones
- Generación de 1,000 registros de clientes con datos realistas
- Introducción controlada de valores nulos para simular datos del mundo real
- Estructura de datos típica del sector telecomunicaciones

### 🔧 **Transformación de Datos (Transform)**
- **Limpieza de datos**: Manejo inteligente de valores nulos
- **Validación de tipos**: Corrección y normalización de formatos
- **Feature Engineering**: Creación de variables derivadas
- **Control de calidad**: Eliminación de outliers y valores inconsistentes

### 📊 **Carga y Análisis (Load)**
- Análisis exploratorio de datos (EDA)
- Visualizaciones interactivas con matplotlib y seaborn
- Cálculo de KPIs de negocio
- Exportación de datos procesados
- Dashboard de métricas clave

### 📄 **Reporting**
- Informe ejecutivo automatizado
- Análisis de churn por segmentos
- Recomendaciones estratégicas basadas en datos
- Identificación de oportunidades de negocio

## 🛠️ Tecnologías Implementadas

```python
# Librerías principales
- pandas: Manipulación y análisis de datos
- numpy: Operaciones numéricas y estadísticas
- matplotlib: Visualizaciones estáticas
- seaborn: Visualizaciones estadísticas avanzadas
- requests: Simulación de API calls
- json: Manejo de datos JSON
- datetime: Manejo de fechas y tiempo
```

## 📁 Estructura del Proyecto

```
TelecomX-ETL/
│
├── TelecomX_LATAM.ipynb       # Notebook principal con pipeline ETL
├── README.md                  # Documentación del proyecto
├── telecom_data_processed.csv # Datos procesados (generado)
└── requirements.txt           # Dependencias del proyecto
```

## 🔍 Variables del Dataset

| Variable | Descripción | Tipo |
|----------|-------------|------|
| `customer_id` | ID único del cliente | Integer |
| `plan_type` | Tipo de plan (Básico, Premium, Enterprise) | String |
| `monthly_charges` | Cargo mensual en USD | Float |
| `total_charges` | Cargo total histórico | Float |
| `tenure_months` | Meses de antigüedad | Integer |
| `data_usage_gb` | Uso de datos en GB | Float |
| `voice_minutes` | Minutos de voz utilizados | Integer |
| `sms_count` | Cantidad de SMS enviados | Integer |
| `region` | Región geográfica | String |
| `churn` | Indicador de abandono (0/1) | Binary |
| `signup_date` | Fecha de registro | Date |

## 📈 Variables Creadas (Feature Engineering)

| Variable | Descripción | Fórmula |
|----------|-------------|---------|
| `revenue_per_month` | Ingreso promedio por mes | total_charges / tenure_months |
| `signup_year` | Año de registro | extract(year from signup_date) |
| `customer_segment` | Segmento por gasto | cut(monthly_charges, bins=3) |

## 🚦 Instalación y Uso

### **Prerrequisitos**
- Python 3.7 o superior
- Jupyter Notebook o Google Colab

### **Instalación**

1. **Clona o descarga el proyecto:**
```bash
# Si tienes git instalado
git clone [URL_DEL_REPOSITORIO]
cd TelecomX-ETL
```

2. **Instala las dependencias:**
```bash
pip install pandas numpy matplotlib seaborn jupyter requests
```

### **Ejecución**

1. **Abre el notebook:**
```bash
jupyter notebook TelecomX_LATAM.ipynb
```

2. **Ejecuta las celdas secuencialmente:**
   - Cada sección está claramente marcada con emojis
   - Sigue el flujo: Extracción → Transformación → Análisis → Informe

3. **Resultados generados:**
   - Visualizaciones interactivas en el notebook
   - Archivo CSV con datos procesados
   - Métricas de KPIs impresas en consola
   - Informe ejecutivo completo

## 📊 Resultados y Métricas

### **KPIs Principales**
- 👥 **Total de clientes**: 1,000 registros
- 💰 **Ingreso promedio mensual**: ~$45 USD
- ⚠️ **Tasa de churn**: ~20%
- 📱 **Uso promedio de datos**: ~10 GB
- ⏱️ **Antigüedad promedio**: ~36 meses

### **Visualizaciones Incluidas**
1. **Distribución por tipo de plan**: Gráfico de barras
2. **Tasa de churn por región**: Análisis comparativo
3. **Relación antigüedad vs cargo**: Scatter plot
4. **Distribución de uso de datos**: Histograma

## 🎯 Insights de Negocio

### **Principales Hallazgos**
- Identificación de regiones con mayor riesgo de churn
- Análisis de rentabilidad por tipo de plan
- Patrones de uso de datos por segmento
- Correlación entre antigüedad y valor del cliente

### **Recomendaciones Estratégicas**
1. **Retención**: Programas específicos para regiones de alto churn
2. **Upselling**: Estrategias basadas en uso de datos
3. **Segmentación**: Ofertas diferenciadas por tipo de plan
4. **Fidelización**: Incentivos para clientes de larga duración

## 🔮 Próximos Pasos

- [ ] **Machine Learning**: Modelos predictivos de churn
- [ ] **Automatización**: Pipeline ETL en producción
- [ ] **Dashboard**: Visualizaciones en tiempo real
- [ ] **Integración**: Conexión con APIs reales
- [ ] **Escalabilidad**: Procesamiento de big data

## 📝 Notas Técnicas

### **Manejo de Datos Faltantes**
- `total_charges`: Imputación por mediana según plan_type
- `data_usage_gb`: Imputación por media general
- Estrategia conservadora para mantener distribuciones originales

### **Control de Calidad**
- Eliminación de valores negativos
- Validación de rangos lógicos
- Verificación de consistencia entre variables

### **Reproducibilidad**
- Seed fijo (42) para generación de datos
- Código documentado y modular
- Resultados consistentes en múltiples ejecuciones


## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

---

⭐ **¡Si este proyecto te fue útil, no olvides darle una estrella!** ⭐

