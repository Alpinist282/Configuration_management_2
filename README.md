# Git Commit Visualizer
Git Commit Visualizer — это утилита командной строки на Python, которая позволяет визуализировать зависимости между коммитами в Git-репозиториях с помощью PlantUML. Этот инструмент создает текстовый код PlantUML и соответствующее изображение, показывающее связи между коммитами.

## Особенности
Поддерживает русский язык.
Генерирует PlantUML-код для создания графа зависимостей коммитов.
Визуализация представлена в виде диаграммы, созданной с использованием PlantUML.
Код PlantUML выводится в консоли и сохраняется в файл.
## Требования
Python версии 3.6 или новее.
Установленный Git.
PlantUML и Java для генерации диаграмм.
## Установка
Клонируйте репозиторий:
```
git clone https://github.com/your-username/git-commit-visualizer.git
cd git-commit-visualizer
```

Установите необходимые зависимости (при необходимости):

```pip install -r requirements.txt```
## Использование

Для запуска инструмента выполните следующую команду:


``` visualizer.py --viz_tool_path "/path/to/plantuml.jar" --repo_path "/path/to/git-repo" --output_path "/path/to/output.puml" --date "YYYY-MM-DD"```
## Аргументы командной строки
```--viz_tool_path```: Путь до файла plantuml.jar.
```--repo_path```: Путь до анализируемого Git-репозитория.
```--output_path```: Путь для сохранения файла с кодом PlantUML.
```--date```: Ограничение по дате для коммитов в формате YYYY-MM-DD.

## Пример использования

```python visualizer.py --viz_tool_path "/usr/local/bin/plantuml.jar" --repo_path "/Users/user/my-repo" --output_path "./output.puml" --date "2024-01-01"```
## Пример вывода
Утилита выведет сгенерированный код PlantUML:
```
@startuml
rectangle "commit (f4555e7)" as f4555e7
rectangle "Начало работы (2d33b8c)" as 2d33b8c
f4555e7 --> 2d33b8c
...
@enduml
```
Также будет создано изображение диаграммы по указанному пути ```output.puml```.
