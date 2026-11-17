# Análisis y Modelado de Siniestralidad Vial en Argentina (2017–2024)

Este repositorio contiene el desarrollo de un proyecto de **Data Science** enfocado en el análisis de microdatos de siniestralidad vial fatal en la República Argentina. A través de dos entregas complementarias (aprendizaje supervisado y no supervisado), se estudian los factores contextuales, temporales, demográficos y de infraestructura asociados a los hechos de tránsito.

---

## 📌 Fuente de Datos y Documentación Base

Los análisis se basan en los registros oficiales del **Sistema de Alerta Temprana (SAT)**, perteneciente al **Sistema Nacional de Información Criminal (SNIC)** del Ministerio de Seguridad de la Nación (`SAT-MV-BU.csv`)[cite: 2].

- **Portal oficial:** [datos.gob.ar - Muertes Viales SAT](https://datos.gob.ar/)
- **Diccionario de variables:** Incluido en la raíz del proyecto como `Manual de usuario Base SAT-MV_2024.pdf`[cite: 2].

---

## 📂 Estructura del Repositorio

El proyecto está organizado en dos carpetas principales correspondientes a cada entrega, junto con el dataset compartido, el manual de usuario y los archivos de configuración en la raíz[cite: 2]:

```text
ProyectoDataScienceCodigo/
├── 1raEntrega/                                           # Aprendizaje Supervisado (Clasificación)
│   ├── Informe DS Proyecto Siniestralidad Vial...pdf     # Informe detallado de la primera etapa
│   ├── ProyectoDS.ipynb                                  # Notebook de análisis y modelado
│   ├── main.py                                           # Script ejecutable
│   ├── README.md                                         # Instrucciones específicas de la 1ra Entrega
│   └── requirements.txt                                  # Dependencias de la 1ra Entrega
│
├── 2daEntrega/                                           # Aprendizaje No Supervisado (Clustering K-Modes)
│   ├── Final_2da_Entrega.ipynb                           # Notebook de clustering y validación externa
│   ├── Informe Proyecto Siniestros Viales Mo...docx      # Informe detallado de la segunda etapa
│   ├── main.py                                           # Script ejecutable
│   └── README.md                                         # Instrucciones específicas de la 2da Entrega
│
├── .gitignore                                            # Archivos excluidos del control de versiones
├── Manual de usuario Base SAT-MV_2024.pdf                # Documentación oficial de las variables del dataset
├── README.md                                             # Información general del repositorio
├── requirements.txt                                      # Dependencias generales del proyecto
└── SAT-MV-BU.csv                                         # Dataset principal utilizado en ambas entregas