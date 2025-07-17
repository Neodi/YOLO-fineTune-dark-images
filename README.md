# Proyecto de Detección de Objetos con YOLO

Este proyecto se centra en la detección de objetos utilizando diferentes versiones del modelo YOLO (You Only Look Once). Se exploran, entrenan y comparan varios modelos YOLO para evaluar su rendimiento en un conjunto de datos personalizado.

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

## Modelos Utilizados

Se han utilizado y comparado las siguientes versiones de YOLO:
- YOLOv5
- YOLOv8
- YOLOv9
- YOLOv10
- YOLOv11

## Uso

1.  **Instalación de dependencias:**
    ```bash
    pip install -r requirements.txt
    ```
2.  **Preprocesado de datos:**
    Ejecutar los notebooks en la carpeta `preprocesado/` para preparar el conjunto de datos.
3.  **Entrenamiento:**
    Utilizar los scripts y notebooks de la carpeta `entrenamiento/` para entrenar los modelos.
4.  **Evaluación:**
    Los notebooks en `benchMarkModelos/` permiten evaluar y comparar el rendimiento de los diferentes modelos.
5.  **Prueba con Webcam:**
    Ejecutar el script `webcam.py` en la carpeta `webCam/` para una demostración en tiempo real.

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir los cambios propuestos.
