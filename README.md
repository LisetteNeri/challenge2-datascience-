
#  Análisis de Evasión de Clientes - Telecom X

Este proyecto aplica habilidades de **Data Science** para resolver un escenario de negocio real: la pérdida de clientes (Churn) en una empresa de telecomunicaciones. A través de la extracción, limpieza y análisis exploratorio de datos, se identifican patrones críticos que permiten formular estrategias de retención.

##  Estructura del Proyecto

* `TelecomX_Data.json`: Dataset original con información demográfica, de servicios y facturación.
* `TelecomX_LATAM.ipynb`: Notebook principal con todo el flujo de trabajo (Extracción, Transformación, EDA e Informe).
* `TelecomX_diccionario.md`: Diccionario de datos para entender las variables del dataset.

##  Tecnologías Utilizadas

* **Lenguaje:** Python 3.13.5
* **Librerías principales:**
    * `Pandas`: Manipulación y limpieza de datos.
    * `Matplotlib` & `Seaborn`: Visualización de datos estadísticos.
    * `JSON`: Procesamiento de la fuente original.

##  Pasos Realizados

### 1. Extracción y Carga
Importación de datos desde una API local/formato JSON y conversión a un DataFrame de Pandas utilizando `json_normalize` para manejar estructuras anidadas.

### 2. Limpieza de Datos (Data Wrangling)
* Conversión de la columna `account.Charges.Total` a tipo numérico (float).
* Tratamiento de valores nulos: Eliminación de registros con `Churn` desconocido y llenado de cargos totales con 0.
* Estandarización de nombres de columnas y eliminación de espacios en blanco.

### 3. Análisis Exploratorio de Datos (EDA)
* **Tasa de Churn:** Identificación de una tasa de evasión del **26.5%**.
* **Análisis Categórico:** Se descubrió que los contratos "Month-to-month" y los pagos con "Electronic Check" son los mayores focos de riesgo.
* **Análisis Numérico:** Se detectó que los clientes con cargos mensuales altos ($>70) y baja antigüedad (<12 meses) tienen una mayor probabilidad de fuga.

## 📈 Hallazgos Clave e Insights

1. **Sensibilidad al Precio:** Los clientes que se van pagan en promedio **$13 más** mensualmente que los que se quedan.
2. **Falta de Compromiso:** El 88% de la evasión proviene de contratos mensuales sin cláusulas de permanencia.
3. **Falla en el Servicio Premium:** La fibra óptica presenta más evasión que el DSL, sugiriendo una oportunidad de mejora en calidad o precio del servicio.

##  Cómo ejecutar el proyecto

1. Clona este repositorio:
   ```bash
   git clone  https://github.com/LisetteNeri/challenge2-datascience-.git

```

2. Instala las dependencias necesarias:
```bash
pip install pandas matplotlib seaborn
```
3. Abre el archivo `TelecomX_LATAM.ipynb` en VS Code y ejecuta todas las celdas.
---

**Desarrollado por Lisette Neri** *Proyecto realizado como parte del Challenge de Data Science de Alura Latam.*

```
