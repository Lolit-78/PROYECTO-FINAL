### Proyecto 5 
## Chatbot Conversacional Multimodal para Servicio al Cliente (Banco Digital)

## Problema: 
Alto volumen de consultas repetitivas (~80%) y necesidad de atención 24/7.
## Solución: 
Chatbot inteligente con NLU (BERT + clasificación de intenciones + extracción de entidades), gestión de diálogo basada en Transformer con memoria, pipeline multimodal (texto + OCR de imágenes), API + interfaz web (Gradio) y sistema de evaluación.

## Datasets: Banking77

## Análisis Detallado de los Resultados, métricas principales:
### Métrica	Validación	Test
Accuracy	84.42%	84.58%
Macro-F1	83.45%	84.38%
### Interpretación:
Consistencia excelente entre validación y test (diferencia < 0.5%)
F1 cercano al accuracy sugiere buen balance entre precisión y recall
Resultados sobresalientes para un problema multiclase con 77 etiquetas

## Plataformas utilizadas
- Google Colab: ejecutar este notebook (GPU opcional para BERT).
- Hugging Face datasets y transformers para NLU (Banking77 + BERT).
- Scikit‑learn para baseline TF‑IDF + LogisticRegression.
- FastAPI + Uvicorn + pyngrok para exponer la API y obtener una URL pública temporal.
- Gradio para la interfaz web.
- pytesseract para OCR (pipeline multimodal).

## Problemas Detectados
- Rendimiento Lento (0.16 it/s)
- Un conjunto de datos de imágenes pequeño y no diverso.
- Preprocesamiento de imágenes más avanzado.
- Posiblemente técnicas de OCR más sofisticadas o modelos de clasificación más complejos.

#### Causas posibles:
- Hardware insuficiente (¿estás usando GPU?)
- Batch size muy pequeño
- Código no optimizado
