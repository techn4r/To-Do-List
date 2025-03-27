# To Do List Manager

Это простая программа на C++ для управления задачами в формате "To Do List". Программа позволяет пользователям создавать задачи, редактировать их, отмечать как выполненные, добавлять подзадачи, а также фильтровать, сортировать, сохранять и загружать задачи из файла. Кроме того, поддерживается функциональность повторяющихся задач и напоминаний, которые проверяются в отдельном потоке.

## Основные возможности

- **Добавление задач:**  
  Пользователь может создать новую задачу, задав её описание, срок выполнения (в формате YYYY-MM-DD), приоритет (от 1 до 5) и категорию. Также можно установить повторение задачи (ежедневно, еженедельно или ежемесячно) и время напоминания.

- **Редактирование задач:**  
  Возможность изменить описание, срок выполнения, приоритет и категорию выбранной задачи.

- **Удаление задач:**  
  Удаление задачи по её уникальному идентификатору (ID).

- **Отметка задач как выполненных:**  
  После отметки задачи как выполненной, если она является повторяющейся, автоматически создаётся новая задача с обновлённой датой.

- **Подзадачи:**  
  Пользователь может добавлять подзадачи к уже существующим задачам.

- **Фильтрация задач:**  
  Задачи можно фильтровать по категории или по статусу (выполненные/не выполненные).

- **Сортировка задач:**  
  Возможность сортировки задач по приоритету или по сроку выполнения.

- **Сохранение и загрузка:**  
  Сохранение текущего списка задач в файл и последующая загрузка задач из файла для восстановления списка.

- **Напоминания:**  
  Фоновый поток каждые 60 секунд проверяет, не наступило ли время напоминания для задачи или подзадачи, и выводит соответствующее сообщение.

## Технологии и инструменты

- **Язык программирования:** C++
- **Стандарт C++:** Программа использует стандартные библиотеки C++ (например, `<iostream>`, `<vector>`, `<string>`, `<fstream>`, `<chrono>`, `<thread>` и т.д.).
- **Многопоточность:** Использование библиотеки `<thread>` для проверки напоминаний в отдельном потоке.

## Сборка и запуск

1. **Компиляция:**

   Используйте компилятор, поддерживающий C++11 или выше. Например, для компиляции с помощью `g++`:
   ```bash
   g++ -std=c++11 -pthread to_do_list.cpp -o todo

Флаг `-pthread` необходим для работы с потоками.

# Запуск программы

После успешной компиляции запустите программу:

```bash
./todo
