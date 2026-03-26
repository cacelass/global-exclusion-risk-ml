# Country Exclusion Clustering
### Unsupervised Learning for Socioeconomic Risk Analysis

---

## Problema

La desigualdad entre países es un fenómeno complejo y multidimensional. Tradicionalmente, los organismos internacionales clasifican los países en categorías como “desarrollados” o “en desarrollo” basándose en indicadores agregados.

Este enfoque presenta varias limitaciones:

- Depende de criterios predefinidos que pueden introducir sesgos
- Simplifica en exceso la realidad, reduciéndola a categorías rígidas
- No captura situaciones intermedias ni patrones ocultos en los datos

En la práctica, los niveles de desarrollo y riesgo de exclusión no son binarios, sino continuos y heterogéneos.

---

## Objetivo

El objetivo de este proyecto es aplicar técnicas de Machine Learning no supervisado para:

- Identificar patrones ocultos en datos socioeconómicos
- Agrupar países según similitudes reales en sus indicadores
- Detectar niveles de riesgo de exclusión sin imponer etiquetas previas
- Proporcionar una visión más objetiva y basada en datos

---

## Enfoque

Se utiliza un enfoque no supervisado en el que el modelo no recibe etiquetas previas. En lugar de clasificar países según definiciones externas, se permite que los datos revelen su propia estructura.

Este enfoque permite:

- Reducir el sesgo humano
- Detectar agrupaciones no evidentes
- Analizar la desigualdad desde una perspectiva cuantitativa

---

## Dataset

El análisis se basa en indicadores socioeconómicos por país, como:

- PIB per cápita
- Esperanza de vida
- Mortalidad infantil
- Nivel de alfabetización
- Otros indicadores de desarrollo y salud

La calidad del análisis depende directamente de la calidad, cobertura y actualidad de estos datos.

---

## Metodología

### 1. Preprocesamiento
- Limpieza de datos
- Tratamiento de valores nulos
- Escalado de variables (StandardScaler)

### 2. Reducción de dimensionalidad (opcional)
- Análisis de Componentes Principales (PCA) para visualización

### 3. Clustering
- Aplicación de K-Means
- Selección del número óptimo de clusters mediante:
  - Método del codo
  - Silhouette Score

### 4. Análisis de resultados
- Interpretación de los clusters
- Relación entre grupos y niveles de desarrollo

---

## Resultados

El modelo segmenta los países en distintos grupos que reflejan niveles diferenciados de desarrollo y riesgo de exclusión:

- Cluster de alto riesgo: bajos ingresos, peores indicadores de salud y desarrollo
- Cluster intermedio: economías en transición con mejoras parciales
- Cluster bajo riesgo: altos niveles de desarrollo económico y social

Estos resultados permiten una lectura más matizada de la desigualdad global.

---

## Insights

- La desigualdad global es gradual y multidimensional
- Existen países que no encajan en clasificaciones tradicionales
- Algunos indicadores tienen mayor peso en la segmentación de lo esperado
- El clustering permite identificar transiciones entre niveles de desarrollo

---

## Limitaciones

- Los resultados dependen de las variables seleccionadas
- K-Means asume estructuras simples (clusters esféricos)
- No se consideran factores políticos o geopolíticos
- Sensible a valores atípicos

---

## Posibles mejoras

- Incorporar nuevas variables (desigualdad, acceso digital, estabilidad política)
- Probar otros algoritmos (DBSCAN, clustering jerárquico)
- Añadir visualizaciones interactivas
- Integrar el modelo en una aplicación

---

## Tecnologías

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn

---

## Estructura del proyecto

    .
    ├── data
    │   └── paises.csv
    ├── LICENSE
    ├── notebooks
    │   └── Paises en peligro de exclusion.ipynb
    └── README.Md

---

## Ejecución

```bash
git clone https://github.com/tu-usuario/country-exclusion-clustering.git
cd country-exclusion-clustering
pip install -r requirements.txt
jupyter notebook
```

---

## Conclusión

Este proyecto muestra cómo el uso de técnicas de Machine Learning no supervisado permite analizar problemas complejos sin depender de clasificaciones predefinidas, aportando una perspectiva más flexible y basada en datos.