
# Clasificación de muestras tumorales con Machine Learning

**Autor:** Álvaro Orta Toscano
**Universidad:** Universidad de Sevilla
**Área:** Bioinformática, Machine Learning aplicado a Biomedicina

---

## Descripción del Proyecto

Este proyecto presenta un flujo completo de Machine Learning en Python para clasificar muestras de tejido mamario como **"benigno"** o **"maligno"**, usando características celulares del conocido **Breast Cancer Dataset** (scikit-learn), con 569 muestras y 30 variables.

El objetivo principal es desarrollar y evaluar un modelo predictivo robusto y optimizado que pueda identificar con precisión tumores malignos basándose en datos biomédicos.

---

## Estructura del proyecto

```
/clasificacion-muestras-python
│
├── clasificacion_muestras.ipynb   # Notebook completo con explicaciones detalladas
├── datos_muestras.csv             # CSV de datos de ejemplo (uso alternativo)
└── README.md                      # Este documento
```

---

## Tecnología y Herramientas utilizadas

* **Python 3.8+**
* **Jupyter Notebook**
* Librerías principales:

  * `pandas`
  * `numpy`
  * `scikit-learn`
  * `matplotlib`
  * `seaborn`

### Instalación de Dependencias

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

---

## Pasos realizados en el análisis

### 1. Carga y preparación de datos

* Dataset: Breast Cancer de scikit-learn.
* Preprocesado y conversión a formato DataFrame de pandas.

### 2. División entrenamiento/prueba

* División de datos: 70% entrenamiento, 30% prueba.
* Estratificación por clase para preservar proporciones.

### 3. Entrenamiento del modelo

* Modelo utilizado: **RandomForestClassifier**.
* 100 árboles (`n_estimators=100`) para robustez y precisión.

### 4. Evaluación del modelo

* Métricas empleadas:

  * **Accuracy** (precisión global)
  * **Matriz de confusión**
  * **Reporte de clasificación** (precision, recall, f1-score)

### 5. Importancia de características

* Identificación y visualización de las 10 variables más importantes.
* Interpretación biológica de la relevancia de estas características.

### 6. Visualización comparativa (Boxplots)

* Distribuciones clave visualizadas:

  * `worst area`
  * `mean concave points`
* Separación clara entre clases benignas y malignas.

### 7. Optimización de hiperparámetros

* Optimización con **GridSearchCV**.
* Búsqueda en espacio de parámetros:

  * `n_estimators`: \[50, 100, 200]
  * `max_depth`: \[None, 3, 5, 7]
  * `min_samples_leaf`: \[1, 2, 4]
* Selección del mejor modelo basado en validación cruzada de 5-fold.

---

## Resultados principales

* **Precisión promedio (Cross-validation)**: ≥ 95%
* **Precisión en test**: 100%

### Mejores hiperparámetros identificados:

```json
{
  "n_estimators": 200,
  "max_depth": 7,
  "min_samples_leaf": 2
}
```

---

## Interpretación y Conclusiones

* Las características relacionadas con el tamaño y la forma celular (especialmente "worst area" y "mean concave points") son altamente predictivas para la malignidad del tumor.
* El modelo optimizado alcanza un desempeño excelente (100% precisión en test), manteniendo una generalización robusta.
* Este proyecto demuestra la efectividad del Machine Learning para asistir en el diagnóstico clínico del cáncer de mama, facilitando la identificación temprana y precisa de tumores malignos.

---

## Uso del proyecto

Para utilizar el proyecto:

1. Descarga el archivo "Clasificacion_550muestras.ipynb"

2. Abre el notebook en Jupyter

3. Ejecuta celda a celda siguiendo las instrucciones y análisis detallados.

---

## Referencias útiles

* [RandomForestClassifier - scikit-learn documentation](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
* [GridSearchCV - scikit-learn documentation](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
* [Breast Cancer Wisconsin Dataset - scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)

---

## Contacto

Álvaro Orta Toscano
Correo: [alvaroortatoscano2006@gmail.com](mailto:alvaroortatoscano2006@gmail.com)
GitHub: [AlvaroOrtaToscano](https://github.com/AlvaroOrtaToscano)
Linkdln: (www.linkedin.com/in/álvaro-orta-toscano-295b87372)
