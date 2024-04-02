# Supervised Learning: Computer Vision

## **Imágenes Histológicas**

Notebook Created by:

- **V. D. Betancourt**




## 📑 Introducción

<details>
    <summary> Expandir </summary>

La presente actividad se enmarca en el ámbito del Aprendizaje Supervisado y la Visión por Computadora, con el propósito de analizar **imágenes histológicas** a través de distintos procesos computacionales.

Se estudiarán las características de 2 imágenes histológicas, dadas como inputs:

*  **`histo_1.jpg`**

    ![](https://github.com/vbleal/05MIAR/blob/main/P1/histo_1.jpg)
   

*  **`histo_2.jpg`**

    ![](https://github.com/vbleal/05MIAR/blob/main/P1/histo_2.jpg)

Las instrucciones (sin solución) se pueden consultar en el Notebook:

* [Actividad_C1_P1_prob.ipynb](https://github.com/vbleal/SL_ComputerVision/blob/main/P1/Actividad_C1_P1_prob.ipynb)


</details>

----------------




## 💡 Principales Ideas

<details>
    <summary> Expandir </summary>

### Carga

Comenzaremos con la carga de una imagen histológica, utilizando la biblioteca **`skimage.io`** para leerla en formato RGB y normalizar sus valores de píxeles al rango [0, 1], facilitando su procesamiento y visualización posterior. Esta etapa inicial es crucial para preparar la imagen para análisis más profundos, permitiendo una manipulación más precisa de sus componentes (Van der Walt et al., 2014).

### Color

Posteriormente, se realizará una transformación de color para convertir la imagen al espacio de color CMYK, enfocándonos en la extracción de la componente magenta que resalta las regiones tisulares. La visualización de esta componente específica permite una mejor identificación de los elementos de interés dentro de la muestra histológica (Plataniotis y Venetsanopoulos, 2000). Seguido de esto, se empleará un proceso de umbralización con el método de Otsu, tras aplicar un filtro gaussiano, para diferenciar claramente entre el fondo y la región tisular, una técnica que mejora la segmentación de imágenes mediante la reducción de ruido y la identificación óptima del umbral.

### Limpieza

La limpieza de la imagen se realizará mediante la eliminación de artefactos de lumen que puedan confundirse con lúmenes reales, utilizando herramientas específicas de morfología de skimage.morphology. Este paso es esencial para asegurar que la segmentación posterior sea lo más precisa posible, eliminando elementos que podrían afectar negativamente la interpretación de los datos.

### Segmentación

Avanzaremos hacia la segmentación específica de lúmenes mediante el algoritmo de expansión a partir de semillas, y posteriormente, rellenaremos estos objetos para facilitar su identificación y análisis. Este enfoque permite un estudio detallado de estructuras específicas dentro de la imagen, proporcionando una base sólida para la detección y el análisis cuantitativo de lúmenes.

### Lumen

Finalmente, se enfocará en la identificación y análisis cuantitativo del lumen más grande, extrayendo características geométricas que permitan su caracterización detallada. Esta fase es crucial para entender las propiedades físicas de los lúmenes, ofreciendo insights valiosos para aplicaciones biomédicas y de investigación.


</details>

----------------




## ㊙️ **Código**

<details>
    <summary> Expandir </summary>

Véase el Notebook:

- [GH_SL_CV_Hist_Actividad_C1_P1_sol.ipynb](https://github.com/vbleal/SL_ComputerVision/blob/main/P1/GH_SL_CV_Hist_Actividad_C1_P1_sol.ipynb)

</details>

----------------







## 📚 **Bibliografía**

<details>
    <summary> Expandir </summary>

*   Kapur, Saurabh (2017). ***Computer Vision with Python 3. Image Classification, Object Detection, Video Processing, and More***. Packt Publishing.

*   Van der Walt S, Schönberger JL, Nunez-Iglesias J, Boulogne F, Warner JD, Yager N, Gouillart E, Yu T. (2014). ***Scikit-image: image processing in Python***. PeerJ 2:e453 https://doi.org/10.7717/peerj.453



</details>

----------------
