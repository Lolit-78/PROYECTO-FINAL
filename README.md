# Proyecto 5
## Chatbot Conversacional Multimodal para Servicio al Cliente (Banco Digital)
### Problema: Alto volumen de consultas repetitivas (~80%) y necesidad de atención 24/7.

### Solución:
Chatbot inteligente con NLU (BERT + clasificación de intenciones + extracción de entidades), gestión de diálogo basada en Transformer con memoria, pipeline multimodal (texto + OCR de imágenes), API + interfaz web (Gradio) y sistema de evaluación.

### Conjuntos de datos: Banking77
Análisis Detallado de los Resultados, métricas principales:
Prueba de validación métrica
Precisión 84,42% 84,58% Macro-F1 83,45% 84,38%

### Interpretación:
Consistencia excelente entre validación y prueba (diferencia < 0.5%) 
F1 cercano al exactitud sugiere buen equilibrio entre precisión y recuperación 
Resultados sobresalientes para un problema multiclase con 77 etiquetas

### Plataformas utilizadas
- Google Colab: ejecuta este notebook (GPU opcional para BERT).
- Conjuntos de datos de Hugging Face y transformadores para NLU (Banking77 + BERT).
- Scikit‑learn para línea base TF‑IDF + Regresión logística.
- FastAPI + Uvicorn + pyngrok para exponer la API y obtener una URL pública temporal.
- Grado para la interfaz web.
- pytesseract para OCR (tubería multimodal).
### Problemas detectados
- Rendimiento lento (0,16 it/s)
- Un conjunto de datos de imágenes pequeño y no diverso.
- Preprocesamiento de imágenes más avanzado.
- Posiblemente técnicas de OCR más sofisticadas o modelos de clasificación más complejos.
### Causas posibles:
- Hardware insuficiente
- Tamaño de lote muy pequeño
- Código no optimizado
