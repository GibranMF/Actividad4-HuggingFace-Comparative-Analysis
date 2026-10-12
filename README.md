# Análisis Comparativo de Modelos NLP usando Hugging Face

## Descripción del proyecto

Este proyecto presenta un análisis comparativo de tres modelos de Procesamiento de Lenguaje Natural (NLP) utilizando el dataset **AG News** y la plataforma **Hugging Face**.

## Modelos evaluados

- Facebook BART Large MNLI
- DeBERTa V3 Zero-Shot
- ModernBERT Large Zero-Shot

## Dataset

### AG News

**Categorías:**

- World
- Sports
- Business
- Sci/Tech

## Entorno de ejecución

### Hardware

- Google Colab
- GPU NVIDIA Tesla T4

### Software

- Python 3
- Transformers
- Hugging Face Hub
- Datasets
- Scikit-Learn
- Pandas
- PyTorch

## Pasos de ejecución

1. Instalar dependencias.
2. Autenticarse en Hugging Face Hub.
3. Cargar el dataset AG News.
4. Cargar los modelos.
5. Ejecutar el pipeline de inferencia.
6. Calcular Accuracy, Precision, Recall y F1-Score.
7. Medir latencia.
8. Comparar resultados.

## Resultados

### Métricas de desempeño

| Modelo | Accuracy | Precision | Recall | F1 Score |
|----------|----------:|----------:|----------:|----------:|
| BART Large MNLI | 0.6767 | 0.6840 | 0.6767 | 0.6763 |
| DeBERTa V3 | 0.8400 | 0.8437 | 0.8400 | 0.8365 |
| ModernBERT | 0.8067 | 0.8223 | 0.8067 | 0.7988 |

### Latencia

| Modelo | Tiempo Total (s) | Latencia Promedio (s) |
|----------|----------:|----------:|
| BART Large MNLI | 32.235 | 0.107 |
| DeBERTa V3 | 43.151 | 0.144 |
| ModernBERT | 47.571 | 0.159 |

## Conclusiones

DeBERTa V3 obtuvo el mejor desempeño general en las métricas de **Accuracy**, **Precision**, **Recall** y **F1 Score**, alcanzando una exactitud de **84.0%**. Por otro lado, BART Large MNLI presentó la menor latencia de inferencia, con un promedio de **0.107 segundos por predicción**.

Considerando tanto el rendimiento predictivo como la eficiencia computacional, **DeBERTa V3 representa la mejor alternativa para tareas de clasificación de noticias sobre el dataset AG News**, ya que ofrece el mejor equilibrio entre precisión y tiempo de respuesta. En escenarios donde la velocidad de inferencia sea el principal requisito, **BART Large MNLI** puede ser una opción adecuada debido a su menor latencia.
