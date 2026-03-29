# Computer Vision Template (YOLO)

Минимальная заготовка для быстрого старта с YOLO в формате Jupyter Notebook.

## Состав

- `requirements.txt`
- `notebooks/01_yolo_quickstart_inference.ipynb`
- `notebooks/02_yolo_custom_dataset_prep_and_train.ipynb`
- `notebooks/03_yolo_validation_and_error_analysis.ipynb`

## Быстрый старт

### 1. Создать и активировать виртуальное окружение

**Windows (cmd):**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**Windows (PowerShell):**

```bash
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### 2. Установить зависимости

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 3. Зарегистрировать ядро для Jupyter

```bash
python -m ipykernel install --user --name cv-yolo-template --display-name "Python (cv-yolo-template)"
```

### 4. Запустить Jupyter

```bash
jupyter lab
```

или

```bash
jupyter notebook
```

## Экспорт ноутбука в HTML

Пример для первого ноутбука:

```bash
jupyter nbconvert --to html notebooks/01_yolo_quickstart_inference.ipynb
```

Пример для всех ноутбуков:

```bash
jupyter nbconvert --to html notebooks/*.ipynb
```

HTML-файлы будут созданы рядом с исходными ноутбуками.

## Что есть в ноутбуках

### 1. `01_yolo_quickstart_inference.ipynb`
- быстрый запуск YOLO
- инференс на изображениях
- инференс на папке
- сохранение результатов
- визуализация предсказаний

### 2. `02_yolo_custom_dataset_prep_and_train.ipynb`
- структура датасета для YOLO
- генерация `dataset.yaml`
- проверка разметки
- команды обучения
- рекомендации по выбору модели и гиперпараметров

### 3. `03_yolo_validation_and_error_analysis.ipynb`
- валидация модели
- просмотр результатов
- базовый разбор ошибок
- анализ confidence / классов / частых промахов

## Полезные замечания

- Для самого быстрого старта обычно подходит `yolov8n.pt`.
- Если GPU нет, можно всё равно запускать инференс и небольшой тренировочный прогон на CPU, но обучение будет медленным.
- Для кастомного датасета важно строго соблюдать формат YOLO-разметки.
- Для воспроизводимости полезно сохранять `runs/` и итоговый `best.pt`.
