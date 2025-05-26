Detector de Fake News 🎯




Descripción

Este proyecto implementa un pipeline completo para la clasificación de titulares de noticias en reales (REAL) o falsas (FAKE). Incluye preprocesamiento de texto, extracción de características con TF-IDF y embeddings preentrenados, comparación de modelos de machine learning, evaluación con métricas clave y un boceto básico para desplegar una app con Streamlit.

Características principales

Preprocesamiento de texto: limpieza, eliminación de HTML, URLs, puntuación, tokenización, eliminación de stopwords y lematización.

Extracción de características:

Vectorización con TF-IDF.

Embeddings semánticos usando sentence-transformers (all-MiniLM-L6-v2).

Modelos comparativos:

Regresión logística.

Random Forest.

Evaluación de resultados:

Classification report (precisión, recall, F1-score).

Matriz de confusión.

ROC-AUC.

Análisis de sentimiento (opcional): uso de VADER para extraer polaridades de los titulares.

Boceto de app con Streamlit para interactuar de forma sencilla.

Tecnologías utilizadas

Python 3.8+

pandas, numpy

scikit-learn

nltk (stopwords, lematización, VADER)

sentence-transformers

(opcional) streamlit

Requisitos previos

Asegúrate de tener Python 3.8 o superior y pip instalados.

Instalación

# Clona este repositorio
git clone https://github.com/usuario/DetectorFakeNews.git
cd DetectorFakeNews

# Crea un entorno virtual (opcional)
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate   # Windows

# Instala las dependencias
pip install -r requirements.txt

Uso

Coloca los archivos de datos training_data.csv y testing_data.csv (separados por tabulador) en la raíz del proyecto.

Ejecuta el notebook o el script principal:

jupyter notebook DetectorFakeNews.ipynb
# o como script si lo adaptas:
python DetectorFakeNews.py

Consulta en la salida las métricas de evaluación:

classification_report

confusion_matrix

roc_auc_score

Análisis de sentimiento

Para realizar un análisis de sentimiento sobre los titulares de prueba:

from DetectorFakeNews import sentiment_scores
scores = sentiment_scores(X_test)
print(scores[:5])

Roadmap



Contribuciones

¡Las contribuciones son bienvenidas! Abre un issue o envía un pull request para mejorar cualquier aspecto del proyecto!

Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.



