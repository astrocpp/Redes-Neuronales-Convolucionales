# 🧠 Seminario Práctico: Redes Neuronales Convolucionales (CNN)

> Asignatura: Introducción a las Redes Neuronales | 2do Año Ingeniería Informática  
> 🎯 **Objetivo:** Comprender arquitecturas de redes neuronales, implementar una CNN para clasificación de imágenes (MNIST) y documentar el proceso mediante código ejecutable y presentación académica.

---

## 📚 1. Conceptos Teóricos Fundamentales

###  ¿Qué es una Red Neuronal Artificial?
Modelo computacional bioinspirado que emula el procesamiento del cerebro. Se basa en:
- **Neuronas artificiales**: Unidades que reciben entradas, aplican pesos (`w`), suman un sesgo (`b`) y pasan el resultado por una función de activación.
- **Aprendizaje**: Ajuste iterativo de pesos mediante `backpropagation` y optimizadores (Adam, SGD) para minimizar una función de pérdida.

### 🔹 Funciones de Activación Clave
| Función | Fórmula | Uso | Ventaja |
|---------|---------|-----|---------|
| **ReLU** | `f(x) = max(0, x)` | Capas ocultas | Eficiente, evita gradiente vanishing |
| **Sigmoid** | `1/(1+e^-x)` | Salida binaria | Probabilística (0-1) |
| **Softmax** | `e^xi / Σe^xj` | Salida multi-clase | Distribución de probabilidad |

### 🔹 Arquitecturas Comparadas
| Arquitectura | Tipo de Dato | Memoria | Paralelización | Uso Típico |
|--------------|--------------|---------|----------------|------------|
| **CNN** | Imágenes/Video | No aplica | Alta | Visión por computadora |
| **RNN** | Secuencias cortas | Limitada | Baja | Series temporales |
| **LSTM** | Secuencias largas | Excelente | Baja | NLP, traducción |
| **Transformer** | Secuencias (texto) | Excelente | Muy Alta | Modelos de lenguaje (GPT, BERT) |

### 🔹 ¿Por qué CNN para Imágenes?
Las redes densas tradicionales aplanan la imagen, perdiendo **estructura espacial** y requiriendo millones de parámetros. Las CNN resuelven esto con:
1. **Convolución**: Filtros que detectan bordes/texturas preservando la topología 2D.
2. **Pooling**: Reduce dimensionalidad manteniendo características dominantes.
3. **Compartición de pesos**: El mismo filtro se aplica en toda la imagen → menos parámetros, mayor generalización.

---

## 💻 2. Implementación Práctica (Google Colab)

El archivo `CNN_MNIST_Colab.ipynb` contiene:
✅ Carga y visualización del dataset MNIST  
✅ Preprocesamiento (normalización + canal de color)  
✅ Arquitectura CNN capa por capa con comentarios técnicos  
✅ Entrenamiento, evaluación y gráficas de convergencia  
✅ Visualización de predicciones correctas/incorrectas  
✅ Guardado del modelo `.h5`

**Para ejecutar:**
1. Abre [Google Colab](https://colab.research.google.com)
2. Sube `CNN_MNIST_Colab.ipynb` o copia el contenido celda por celda
3. Ejecuta todo (`Runtime > Run all`)
4. Descarga el notebook ejecutado para subirlo al repo

---

## 📊 3. Presentación PowerPoint

Ejecuta el script para generar la presentación automáticamente:
```bash
pip install python-pptx
python generar_presentacion.py
