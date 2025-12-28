# NLP-tasks: Financial Sentiment Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Models-orange)](https://huggingface.co/models)

Данный репозиторий посвящен исследованию и реализации классификации тональности финансовых текстов (Sentiment Analysis). Основная цель — сравнение эффективности базовой модели **BERT** и специализированной модели **FinBERT** на специфичных данных финансового сектора.

## 📌 Описание проекта

Проект решает задачу мультиклассовой классификации: **positive** (положительный), **negative** (отрицательный) и **neutral** (нейтральный) контекст в финансовых новостях и отчетах. 

### Основные этапы:
* **Data Pipeline:** Загрузка, предобработка и токенизация датасета.
* **Model Training:** Тонкая настройка (Fine-tuning) предобученных моделей через Hugging Face `Trainer` API.
* **Evaluation:** Сравнение моделей по метрикам Accuracy, Precision, Recall и F1-score.

## 📊 Результаты сравнения моделей

Экспериментальные данные, полученные в ходе обучения на тестовой выборке:

| Модель | Accuracy | Precision | Recall | F1-Score | Eval Loss |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **BERT (base-uncased)** | **0.70** | **0.728** | **0.699** | **0.696** | 0.8589 |
| **FinBERT (tone)** | 0.61 | 0.607 | 0.609 | 0.574 | **0.8018** |

*Примечание: В данных тестах базовая модель BERT показала более высокую точность, однако FinBERT продемонстрировал более низкое значение функции потерь (loss).*

## 🛠 Установка

Склонируйте репозиторий:
```bash
git clone [https://github.com/Maksimonk/NLP-tasks.git](https://github.com/Maksimonk/NLP-tasks.git)
cd NLP-tasks
```