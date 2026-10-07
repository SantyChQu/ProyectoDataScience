Predictor y Análisis de Siniestralidad Vial en Argentina (2017–2024)

Este proyecto analiza los microdatos de siniestralidad vial en la República Argentina entre los años 2017 y 2024. El objetivo principal es construir un modelo de Clasificación en Data Science para predecir la modalidad o tipo de un hecho vial en función de variables contextuales como el clima, la franja horaria y el tipo de lugar.

📌 Contexto del Proyecto

Los datos son recopilados a través del Sistema de Alerta Temprana (SAT), perteneciente al Sistema Nacional de Información Criminal (SNIC) del Ministerio de Seguridad. Corresponden a informes sobre personas fallecidas a causa de hechos de tránsito.

Fuente de Datos: datos.gob.ar - Muertes Viales SAT

Dataset utilizado: SAT-MV-BU.xlsx

🎯 Objetivo y Pregunta del Negocio

Pregunta del Negocio

¿Qué tipo de siniestro podemos esperar según las condiciones observadas (clima, franja horaria y tipo de lugar), permitiendo analizar los resultados por provincia y a lo largo de los años 2017–2024?

💻 Guía Paso a Paso para Usar este Repositorio

Sigue estos pasos en tu computadora para descargar, configurar y ejecutar el script.

Requisitos Previos:

Tener instalado Python 3.8+ y Git.

1. Clonar el Repositorio

Abre tu terminal (PowerShell, CMD o Git Bash) y ejecuta:

git clone https://github.com/TU_USUARIO/TU_REPOSITORIO.git
cd TU_REPOSITORIO

2. Crear y Activar un Entorno Virtual

El entorno virtual aísla las librerías para evitar conflictos con otras versiones de tu sistema.

En Windows:

python -m venv venv
.\venv\Scripts\activate

(Verás que aparece (venv) al inicio de la línea de tu terminal)

En macOS / Linux:

python3 -m venv venv
source venv/bin/activate

3. Instalar las Dependencias Necesarias

Instala todas las librerías requeridas (pandas, openpyxl, scikit-learn, etc.) usando el archivo requirements.txt:

pip install -r requirements.txt

Nota: Si no posees el archivo requirements.txt, puedes instalar manualmente las librerías principales ejecutando:

pip install pandas numpy matplotlib seaborn openpyxl scikit-learn

4. Ejecutar el Script de Python

Una vez instaladas las dependencias, corre tu script .py principal:

python main.py

🛠️ Estructura del Proyecto

.
├── .gitignore # Archivos excluidos del control de versiones (venv, cache, etc.)
├── README.md # Instrucciones e información del proyecto
├── requirements.txt # Librerías necesarias para ejecutar el proyecto
├── SAT-MV-BU.xlsx # Dataset (Asegurarse de agregarlo localmente)
└── main.py # Código fuente principal extraído de Colab

👥 Contribuciones

Si vas a realizar cambios en el análisis o en el modelo:

Crea una nueva rama (git checkout -b mi-rama).

Haz tus cambios y confirmalos (git commit -m "Descripción de los cambios").

Sube la rama (git push origin mi-rama).

Abre un Pull Request para revisarlo con el equipo.
