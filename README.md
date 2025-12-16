# Tesis – SEGUIMIENTO DE POSE EN VIDEO USANDO TÉCNICAS DE DEEP LEARNING PARA PROYECCIÓN TRIDIMENSIONAL EN APLICACIONES DE REALIDAD VIRTUAL

Este repositorio contiene los notebooks utilizados en mi trabajo de grado sobre **estimación de pose 3D en video** y comparación de distintos modelos (VIBE, MediaPipe BlazePose, etc.) para aplicaciones de realidad virtual.

## Estructura

- `Pose_Mediapipe_Descarga_Mk1_version.ipynb`  
  Genera las poses 3D de MediaPipe a partir de secuencias de imágenes y guarda `poses3d_all.npy`.

- `vibe_demo_Mk5.ipynb`  
  Ejecuta VIBE sobre un video de entrada y genera `vibe_output.pkl` con las poses 3D.

- `Visualizar_npy_Mediapipe.ipynb`  
  Inspección y visualización de `poses3d_all.npy` (MediaPipe), comparación visual MP vs VIBE.

- `3DPW.ipynb`  
  Procesamiento de datos del dataset 3DPW y generación de archivos `.npy` con el esqueleto de 14 articulaciones.

- `GenerarJSON.ipynb`  
  Unifica los datos de GT, VIBE y MediaPipe en un solo archivo `dataset_3models_fix.json` con 14 articulaciones comunes.

- `VisualizarJSON.ipynb`  
  Visualización de las poses desde el JSON unificado y cálculo de métricas (MPJPE, PCK) a nivel de secuencia.

- `Postprocesamiento_2.ipynb`  
  Normalización (centrado + escalado), cálculo de métricas finales (MPJPE/PCK) y generación de tablas y figuras usadas en la tesis.

## Requisitos y ejecución

Los notebooks están pensados para ejecutarse en **Google Colab**:

1. Clonar o descargar este repositorio.
2. Subir el notebook a Colab.
3. Ajustar las rutas de los archivos de entrada (videos, NPY, JSON) según el entorno.
4. Ejecutar celda por celda siguiendo los comentarios dentro de cada notebook.

> Los datasets originales (por ejemplo 3DPW) **no se incluyen** en este repositorio por temas de licencia. El usuario debe obtenerlos desde sus fuentes oficiales.
