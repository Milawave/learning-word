# Учу слово/Vocabulary Learning System 

## Описание проекта
Система предназначена для изучения иностранных слов учениками языковой школы.
Пользователь добавляет слова в активный словарь, повторяет их и отслеживает прогресс обучения.
Выученные слова могут быть перенесены в архив.

## Основные функции
- выбор и изменение языка обучения
- получение списка доступных языков
- добавление слов в активный словарь
- получение перевода слова
- интервальное повторение слов
- перенос слов в архив
- очистка архива

## Диаграммы

### Диаграмма классов
![Class Diagram](uml/class-diagram.png)

### Диаграмма вариантов использования
![Use Case Diagram](uml/use-case-diagram.png)

## API (Swagger)

API системы описан с использованием стандарта OpenAPI 3.0.

[Swagger UI](https://app.swaggerhub.com/apis/MILAMIHEEVA/LearningWord/1.0.0)
[OpenAPI спецификация](swagger/Api.yaml)

### Основные эндпоинты

**Языки**
- `GET /Language` — получить текущий язык
- `PUT /Language/{code}` — изменить язык
- `GET /Languages` — получить список языков

**Словари**
- `GET /ActiveDictionary` — получить список изучаемых слов
- `GET /ActiveDictionary/word` — получить перевод слова
- `POST /ActiveDictionary/word` — добавить слово
- `PATCH /ActiveDictionary/word` — перенести слово в архив

**Архив**
- `DELETE /Archive` — очистить архив

## Документы

[Спецификация системы](specification.docx)

## Структура проекта


vocabulary-learning-system/
│
├── README.md
├── specification.docx
│
├── uml/
│ ├── class-diagram.png
│ ├── class-diagram.drawio
│ ├── use-case-diagram.png
│ └── use-case-diagram.drawio
│
├── swagger/
│ └── api-spec.yaml
## Примечание

Swagger API представляет упрощённую модель взаимодействия с системой и может не полностью отражать внутреннюю структуру классов, представленную на UML-диаграмме.