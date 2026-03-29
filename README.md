# Computer Vision Template (YOLO)

Минимальная заготовка для быстрого старта с YOLO в формате Jupyter Notebook.

## Состав

- `requirements.txt`
- `notebooks/01_yolo_image_blocks.ipynb`
- `notebooks/02_yolo_video_train_and_detect.ipynb`
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

Пример для ноутбука по изображениям:

```bash
jupyter nbconvert --to html notebooks/01_yolo_image_blocks.ipynb
```

Пример для всех ноутбуков:

```bash
jupyter nbconvert --to html notebooks/*.ipynb
```

## Что есть в ноутбуках

### 1. `01_yolo_image_blocks.ipynb`
- простой и блочный шаблон для изображений
- понятные функции с комментариями
- инференс на одном изображении
- инференс на папке изображений
- разбор детекций в удобную структуру

### 2. `02_yolo_video_train_and_detect.ipynb`
- структура датасета для детекции
- генерация `dataset.yaml`
- дообучение модели на своих данных
- быстрый инференс на видео
- покадровая обработка видео через OpenCV
- сохранение результата в новый видеофайл

### 3. `03_yolo_validation_and_error_analysis.ipynb`
- валидация модели
- просмотр результатов
- базовый разбор ошибок
- анализ confidence / классов / частых промахов

## Полезные замечания

- Для самого быстрого старта обычно подходит `yolov8n.pt`.
- Если GPU нет, можно запускать инференс и короткие тестовые прогоны на CPU.
- Для кастомного датасета важно соблюдать формат YOLO-разметки.
- Для отладки видео полезно сначала ограничивать обработку первыми кадрами.