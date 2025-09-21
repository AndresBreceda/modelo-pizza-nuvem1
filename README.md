# modelo-pizza-nuvem1

# Clasificador de Imágenes: Pizza vs. Nube 🌤️🍕

Este proyecto implementa un modelo de **Machine Learning con Transfer Learning** para clasificar imágenes en dos categorías: **pizza** y **nube**.  
El desarrollo se realiza en **Google Colab**, utilizando **TensorFlow/Keras** y un modelo base preentrenado (**MobileNetV2**) sobre el dataset **ImageNet**.  

---

## 📂 Estructura del Dataset
El dataset está organizado en carpetas dentro de Google Drive:
/imagenes/pizza
/imagenes/nube


---

## 🔄 Flujo del Proyecto
1. **Montaje de Google Drive** → conexión de Colab con Drive para acceder al dataset.  
2. **Carga y preprocesamiento** → uso de `image_dataset_from_directory`, `preprocess_input` y **data augmentation** (rotaciones, flips, zoom).  
3. **Transfer Learning con MobileNetV2** → reutilización de pesos preentrenados en ImageNet.  
   - Fase 1: se congela el modelo base y se entrena una nueva capa de clasificación binaria.  
   - Fase 2: se realiza *fine-tuning* descongelando las últimas capas para ajustar al dataset específico.  
4. **Entrenamiento y evaluación** → el modelo se entrena con `binary_crossentropy` y se mide exactitud en validación.  
5. **Predicción** → se prueban imágenes nuevas y el modelo devuelve la clase (**pizza** o **nube**) junto con la probabilidad estimada.  

Ejemplo de salida:
Predicción: Pizza (0.87)


---

## 🎯 Objetivo
El objetivo es demostrar cómo aplicar **redes neuronales convolucionales (CNNs)** y **transfer learning** en un problema de clasificación binaria con un dataset pequeño y personalizado.  

Este proyecto puede servir como base para crear clasificadores en otros dominios (comida, paisajes, objetos, etc.) siguiendo la misma metodología.  

---


