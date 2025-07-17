# Detección y Clasificación con YOLO en Condiciones de Baja Iluminación

Este proyecto se centra en la detección y clasificación de objetos en condiciones de baja iluminación utilizando diferentes versiones del modelo YOLO (You Only Look Once). Se realiza un preprocesado de imágenes, entrenamiento, fine-tuning y una comparativa exhaustiva del rendimiento de los modelos YOLOv5, YOLOv8, YOLOv9, YOLOv10 y YOLOv11.

## Orden de Ejecución de los Ficheros

Para replicar el proyecto, se recomienda seguir el siguiente orden de ejecución:

1.  **Preprocesado de Datos (`preprocesado/preprocesado.ipynb`)**:
    -   Este notebook se encarga de preparar el conjunto de datos `ExDark`. Realiza la división en conjuntos de entrenamiento, validación y prueba, y ajusta las anotaciones al formato requerido por YOLO.

2.  **Entrenamiento y Fine-Tuning (`benchMarkModelos/entrenados/`)**:
    -   `entrenamiento_de_0.ipynb`: Script para entrenar los modelos desde cero.
    -   `entrenamiento20_epocas-comparativa.ipynb`: Entrenamiento y comparación de los modelos durante 20 épocas.
    -   `entrenamiento200_epocas.ipynb`: Entrenamiento de los modelos durante 200 épocas para un análisis más profundo.
    -   `fine_tunning.ipynb`: Notebook para realizar el ajuste fino (fine-tuning) de los modelos pre-entrenados con el conjunto de datos específico.

3.  **Evaluación y Comparativa (`benchMarkModelos/`)**:
    -   `base/modelos_1epoc.ipynb`: Benchmark inicial de los modelos base con solo una época de entrenamiento.
    -   `entrenados/comparatativa200_epoc_y9-y10-y11.ipynb`: Notebook para comparar específicamente las versiones 9, 10 y 11 de YOLO tras 200 épocas de entrenamiento.

4.  **Pruebas en Tiempo Real (`webCam/`)**:
    -   `testWebCam-YOLObase.py`: Script para probar los modelos base con una cámara web.
    -   `procesarIMG.ipynb`: Notebook para procesar imágenes estáticas con los modelos entrenados.

## Resultados

A continuación se muestran algunas de las métricas y resultados obtenidos durante el entrenamiento y la evaluación de los modelos.

### Curvas de Pérdida (Loss)

**20 Épocas**
![Loss 20 épocas](benchMarkModelos/entrenados/graficas%20resultados/loss20epocas.png)

**200 Épocas**
![Loss 200 épocas](benchMarkModelos/entrenados/graficas%20resultados/loss200epocas.png)

### Métricas de Rendimiento

**mAP (mean Average Precision) en Validación (200 épocas)**
![mAP Validación 200 épocas](benchMarkModelos/entrenados/graficas%20resultados/mAPvalidacion200epocas.png)

**Métricas en Test (200 épocas)**
![Métricas en Test 200 épocas](benchMarkModelos/entrenados/graficas%20resultados/metricas200epocasTEST.png)

### Matriz de Confusión

![Matriz de Confusión](benchMarkModelos/entrenados/graficas%20resultados/Confusion_matrix_vs.png)

## Conclusiones

A partir de los resultados obtenidos, se puede concluir que los modelos más recientes de YOLO, como YOLOv9, YOLOv10 y YOLOv11, muestran un rendimiento superior en la detección de objetos en condiciones de baja iluminación después de un entrenamiento extensivo (200 épocas). El proceso de fine-tuning también demuestra ser crucial para adaptar los modelos a las características específicas del conjunto de datos `ExDark`, mejorando significativamente la precisión y el mAP en comparación con los modelos base.

## Estructura del Directorio

- `benchMarkModelos/`: Contiene notebooks y modelos para realizar benchmarks de las distintas versiones de YOLO.
  - `base/`: Modelos base sin re-entrenamiento.
  - `entrenados/`: Modelos re-entrenados y fine-tunning.
- `data/`: Contiene el conjunto de datos utilizado para el entrenamiento y la validación, dividido en imágenes y etiquetas.
- `entrenamiento/`: Notebooks y scripts para el entrenamiento de los modelos YOLO.
- `preprocesado/`: Scripts para el preprocesado de los datos, incluyendo la preparación de imágenes y anotaciones.
- `webCam/`: Scripts para probar los modelos en tiempo real utilizando una cámara web.
- `data_collab.yaml`: Fichero de configuración para el conjunto de datos.
- `ficheros_importantes_memoria.ipynb`: Notebook con información relevante sobre el proyecto.

## Uso

1.  **Instalación de dependencias:**
    ```bash
    pip install -r requirements.txt
    ```
2.  **Ejecutar los notebooks y scripts** en el orden descrito anteriormente.

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir los cambios propuestos.
