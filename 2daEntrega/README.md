# Patrones de Siniestralidad Vial Fatal en Conductores de Motocicleta en Argentina (Modelo No Supervisado: K-Modes)

> **ACLARACIÓN INICIAL:**  
> Para una mejor experiencia se recomienda abrir el archivo `.ipynb` directamente en **Google Colab** (enlace disponible en la cabecera del notebook), ya que el script descarga automáticamente el dataset oficial desde los servidores del Ministerio de Seguridad si no se encuentra de forma local y facilita la visualización interactiva de gráficos y matrices.

Este proyecto analiza los microdatos de siniestralidad vial en la República Argentina utilizando técnicas de aprendizaje no supervisado. El objetivo principal es desarrollar un modelo de **clustering categórico (`K-Modes` + comparativa metodológica)** para identificar perfiles y patrones de hechos viales fatales cuyas víctimas sean **conductores de motocicleta**, combinando variables de infraestructura vial, mecánica/contraparte del impacto y contexto horario, junto con **validación externa** sobre edad, género y región geográfica.

---

## 📌 Contexto del Proyecto

Los datos son recopilados a través del **Sistema de Alerta Temprana (SAT)**, perteneciente al **Sistema Nacional de Información Criminal (SNIC)** del Ministerio de Seguridad de la Nación. Corresponden a informes sobre personas fallecidas a causa de hechos de tránsito en Argentina.

- **Fuente de Datos:** [datos.gob.ar - Muertes Viales SAT](https://datos.gob.ar/) / Servidor oficial SNIC (`https://cloud-snic.minseg.gob.ar/Bases/SAT/MV/SAT-MV-BU.csv`)
- **Dataset utilizado:** `SAT-MV-BU.csv` (con descarga automática integrada en el notebook si no está presente localmente)

---

## 🎯 Objetivo y Enfoque Analítico

**Pregunta de Investigación:**  
*¿Qué perfiles o patrones diferenciados de siniestros viales fatales existen entre los conductores de motocicleta en Argentina según la infraestructura vial, la contraparte del impacto y el contexto temporal, y cómo se distribuyen estos grupos según la edad, el género y la región?*

### Hoja de Ruta del Notebook (`Final 2da Entrega.ipynb`)

| Sección | Etapa del Proyecto |
| :--- | :--- |
| **1 – 3** | Carga del dataset (local o vía URL SNIC), limpieza, filtrado de víctimas conductoras de motocicleta y creación de variables derivadas (`contraparte`, `ambito_vial`, `en_interseccion`, `turno`, etc.). |
| **4** | Armado del dataset de modelado con las 6 variables iniciales y análisis exploratorio de sus distribuciones. |
| **5 – 6** | Selección de $K$ (Método del Codo) y entrenamiento del **primer modelo K-Modes ($K=4$)** con las variables originales. Evaluación mediante Silueta de Hamming y proyección PCA 2D. |
| **7** | Diagnóstico de asociación entre variables categóricas mediante **V de Cramér** para detectar redundancias y ruido. |
| **8 – 10** | Evaluación de distintos escenarios de selección de variables (atómicas vs. compuestas) y definición de las variables finales del modelo. |
| **11 – 12** | Barrido de $K$ y comparativa metodológica: `K-Modes (Cao)`, `K-Modes (Huang)`, `OHE + K-Means`, `Consensus Clustering` y `Autoencoder (MLP) + K-Means`, más auditoría con `HistGradientBoostingClassifier`. |
| **13 – 14** | Entrenamiento del **modelo definitivo K-Modes**, análisis de estabilidad (ARI), composición interna de los clusters y **validación externa** (Chi² y V de Cramér sobre edad, género y región). |

---

## 💻 Guía Paso a Paso para Usar este Repositorio

Sigue estos pasos en tu computadora para descargar, configurar y ejecutar el proyecto de manera local (o ábrelo directamente en Google Colab).

### Requisitos Previos
- Tener instalado **Python 3.8+** y **Git**.
- Jupyter Notebook, JupyterLab o VS Code con la extensión de Jupyter.

### 1. Clonar el Repositorio

Abre tu terminal (PowerShell, CMD o Git Bash) y ejecuta:

```bash
git clone [https://github.com/SantyChQu/ProyectoDataScience.git](https://github.com/SantyChQu/ProyectoDataScience.git)
cd ProyectoDataScience
cd 2daEntrega
python main.py