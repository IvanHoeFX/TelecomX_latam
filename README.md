# 📊 Telecom X - Análisis de Evasión de Clientes (Churn)

## 📌 Descripción del Proyecto
Este proyecto forma parte del **Challenge Telecom X** de **Alura Latam - ONE**, cuyo objetivo es analizar la **evasión de clientes** (*Churn*) en una empresa de telecomunicaciones.  
Se desarrolla un flujo de trabajo **ETL (Extracción, Transformación y Carga)** y un **Análisis Exploratorio de Datos (EDA)**, seguido de la elaboración de un informe profesional con hallazgos y recomendaciones.

Durante el análisis se detectaron **224 valores vacíos en la columna `Churn`** y **11 en `account.Charges.Total`**, los cuales **no fueron eliminados**, ya que representan una oportunidad para desarrollar estrategias específicas orientadas a clientes con datos faltantes o inconsistentes.

---

## 🎯 Objetivos
- **Identificar factores asociados al Churn** mediante análisis exploratorio y visualizaciones.
- **Limpieza y estandarización de datos** para garantizar calidad y consistencia.
- **Proporcionar insights estratégicos** para acciones de retención de clientes.
- **Mantener el esquema original de 21 columnas** según el diccionario de datos.

---

## 📂 Estructura del Proyecto
El notebook sigue la metodología **ETL**:

1. **Extracción**  
   - Carga de datos desde un archivo JSON (API simulada).  
   - Conversión a DataFrame y normalización de datos anidados.

2. **Transformación**  
   - Conversión de tipos de datos (`Int64`, `float`, `object`).  
   - Manejo de valores nulos, duplicados y cadenas vacías.  
   - Estandarización de textos y categorías.  
   - Creación de columnas derivadas como *Cuentas_Diarias*.

3. **Carga y Análisis**  
   - Análisis descriptivo: media, mediana, desviación estándar.  
   - Visualización de distribución de *Churn*.  
   - Comparación de *Churn* con variables categóricas y numéricas.  
   - Identificación de patrones clave.

4. **Informe Final**  
   - Hallazgos principales y su interpretación.  
   - Recomendaciones estratégicas basadas en los resultados.  
   - Posibles próximos pasos para modelado predictivo.

---

## 📊 Diccionario de Datos (21 columnas)
| Columna                     | Descripción |
|-----------------------------|-------------|
| customerID                  | Identificador único del cliente |
| Churn                       | Cliente dejó la empresa (1) o no (0) |
| customer.gender             | Género |
| customer.SeniorCitizen      | ≥65 años (1) o no (0) |
| customer.Partner            | Tiene pareja |
| customer.Dependents         | Tiene dependientes |
| customer.tenure             | Meses de contrato |
| phone.PhoneService          | Servicio telefónico |
| phone.MultipleLines         | Líneas múltiples |
| internet.InternetService    | Tipo de servicio de Internet |
| internet.OnlineSecurity     | Seguridad en línea |
| internet.OnlineBackup       | Respaldo en línea |
| internet.DeviceProtection   | Protección de dispositivo |
| internet.TechSupport        | Soporte técnico |
| internet.StreamingTV        | Streaming de TV |
| internet.StreamingMovies    | Streaming de películas |
| account.Contract            | Tipo de contrato |
| account.PaperlessBilling    | Facturación electrónica |
| account.PaymentMethod       | Método de pago |
| account.Charges.Monthly     | Cargos mensuales |
| account.Charges.Total       | Cargos totales acumulados |

---

## 📈 Resultados Clave
- **71.2%** de clientes permanecen, **25.72%** se dieron de baja y **3.08%** sin dato.  
- **224 valores faltantes en `Churn`** y **11 en `account.Charges.Total`**, conservados para un análisis estratégico posterior.
- Mayor churn en clientes con **contrato mensual** y **facturación electrónica**.  
- Clientes con **tenure bajo** y **cargos mensuales altos** son más propensos a cancelar.  
- Servicios de valor como *OnlineSecurity* y *TechSupport* reducen la probabilidad de churn.

---

## 🛠️ Tecnologías Utilizadas
- **Python** (3.10+)
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Requests** (extracción de datos)
- **Jupyter Notebook**

---

## 🚀 Ejecución del Proyecto

### 1️⃣ Clonar el repositorio
```bash
git clone https://github.com/tu_usuario/tu_repositorio.git
cd tu_repositorio
```

### 2️⃣ Instalar dependencias
```bash
pip install -r requirements.txt
```

### 3️⃣ Ejecutar el notebook
Abrir en Jupyter Notebook o VSCode y ejecutar las celdas en orden.

---

## 📌 Próximos Pasos
- Implementar un **modelo predictivo de Churn**.
- Realizar **análisis de cohortes** para evaluar retención.  
- Implementar **tests A/B** para validar estrategias.

---

## 👨‍💻 Autor
Proyecto desarrollado como parte del **Challenge de Ciencia de Datos - Alura Latam & ONE**.  
Creado por *Walter Alcántara S.* — 2025.
