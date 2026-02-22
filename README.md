from pypandoc import convert_text

readme_md = """
# 📊 Predicción de Churn – Desafío Data Science g-115
**Autor:** Ignacio Robles  
**Programa:** Data Science – Generación g-115  
**Bootcamp:** Desafío Latam  

---

## 🎯 Descripción del Proyecto

En la industria de las telecomunicaciones, la retención de clientes es un desafío estratégico clave. 
La fuga de clientes (Churn) puede impactar directamente en los ingresos y la estabilidad del negocio.

El objetivo de este proyecto es desarrollar modelos de Machine Learning capaces de predecir la 
probabilidad de abandono de clientes utilizando el dataset **Telco Customer Churn**, aplicando un 
flujo completo de ciencia de datos desde el análisis exploratorio hasta la evaluación comparativa 
de modelos.

---

## 🧠 Objetivos del Desafío

- Comprender la estructura y comportamiento del dataset
- Realizar análisis exploratorio de datos (EDA)
- Preprocesar variables categóricas y numéricas
- Entrenar múltiples modelos de clasificación
- Evaluar el rendimiento mediante métricas relevantes
- Analizar el impacto del desbalance de clases en la predicción de churn

---

## 🗂️ Estructura del Proyecto

```
├── Cuaderno_Desafio_Churn_Ignacio_Robles.ipynb
├── Telco-Customer-Churn.xlsx
└── README.md
```

---

## 🔍 Metodología

El desarrollo del proyecto sigue un enfoque estructurado de Machine Learning:

1. Análisis Exploratorio de Datos (EDA)  
2. Limpieza y Preprocesamiento  
3. Escalado de variables (StandardScaler)  
4. División de datos (Train/Test Split)  
5. Entrenamiento de modelos de clasificación  
6. Evaluación y comparación de resultados  

---

## 🤖 Modelos Implementados

- K-Nearest Neighbors (KNN)  
- Árbol de Decisión  
- Gaussian Naive Bayes  

Se utilizó escalado de variables para garantizar un desempeño adecuado en modelos sensibles a la distancia como KNN.

---

## 📊 Métricas de Evaluación

Para evaluar el rendimiento de los modelos se utilizaron:

- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Matriz de Confusión  

Dado el desbalance del dataset, se puso especial énfasis en el Recall de la clase Churn.

---

## 📈 Principales Hallazgos

- El dataset presenta desbalance de clases, afectando la detección de churn.
- KNN mostró el mejor equilibrio general de rendimiento.
- El Árbol de Decisión aportó interpretabilidad en las variables clave.
- Gaussian Naive Bayes destacó en la detección de clientes en riesgo (alto Recall en Churn).
- El desbalance impacta directamente la capacidad predictiva en la clase minoritaria.

---

## ⚙️ Tecnologías Utilizadas

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

---

## 🚀 Posibles Mejoras Futuras

- Aplicación de técnicas de balanceo de clases (SMOTE o class_weight)
- Optimización avanzada de hiperparámetros
- Implementación de modelos ensemble (Random Forest, Gradient Boosting)
- Validación cruzada (Cross Validation)

---

## 🙌 Agradecimientos

Proyecto desarrollado en el contexto del desafío académico del bootcamp de Data Science de Desafío Latam, 
con el objetivo de aplicar técnicas de aprendizaje supervisado en un caso real de predicción de churn.
"""

output_path = "/mnt/data/README_Desafio_Churn_Ignacio_Robles.md"
convert_text(readme_md, 'md', format='md', outputfile=output_path, extra_args=['--standalone'])
output_path