**Исполняемая среда (runtime)** — это совокупность программных механизмов и компонентов, которые предоставляют поддержку для выполнения программы во время её работы. Это инфраструктура, которая обеспечивает выполнение программы, управление памятью, обработку исключений, взаимодействие с операционной системой и выполнение других задач, необходимых для функционирования программы.
### Основные функции исполняемой среды

1. **Управление памятью:**
    
    - Выделение и освобождение памяти.
    - Автоматическая очистка неиспользуемой памяти (сборка мусора).
    - Обеспечение безопасности доступа к памяти (например, предотвращение доступа к неинициализированным данным).
2. **Обработка исключений и ошибок:**
    
    - Перехват и обработка исключений, возникающих во время выполнения.
    - Управление завершением программы при критических ошибках.
3. **Планирование выполнения:**
    
    - Организация выполнения потоков или горутин.
    - Управление многозадачностью и параллельностью.
4. **Взаимодействие с операционной системой:**
    
    - Работа с файловой системой, сетью и другими системными ресурсами.
    - Управление потоками ввода-вывода.
5. **Динамическая компиляция или интерпретация:**
    
    - Некоторые языки (например, Java или Python) используют виртуальные машины, которые компилируют или интерпретируют код во время выполнения.
6. **Отладка и диагностика:**
    
    - Предоставление информации о текущем состоянии программы: стек вызовов, использование памяти и ресурсов.

Исполняемая среда (runtime) имеет аналоги и схожие технологии в контексте разных языков программирования, платформ и инфраструктур. Они предоставляют схожие функции: управление памятью, выполнение кода, взаимодействие с ОС и поддержка параллельных вычислений. Вот некоторые из них:
### 1. **Виртуальные машины (Virtual Machines)**

Эти технологии схожи с runtime, но обычно выполняют код в изолированной среде.

- **Java Virtual Machine (JVM):**
    
    - Выполняет байт-код Java, обеспечивая переносимость программ.
    - Управляет памятью (сборщик мусора), предоставляет планировщик потоков, обработку исключений.
    - Расширяется для других языков (Scala, Kotlin).
- **.NET Common Language Runtime (CLR):**
    
    - Исполняемая среда для платформы .NET.
    - Обеспечивает выполнение кодов на C#, F#, VB.NET и других языках.
    - Включает сборщик мусора, поддержку безопасности, многопоточности и динамической компиляции (Just-In-Time, JIT).
- **Parrot Virtual Machine:**
    
    - Проект для выполнения динамических языков (Perl, Python, Ruby). Хотя проект заброшен, он использовался как пример runtime для мульти-языковых сред.
### 2. **Интерпретаторы**

Исполняемые среды для языков с интерпретацией кода (без предварительной компиляции).

- **Python Interpreter:**
    
    - Выполняет Python-код построчно.
    - Управляет памятью (сборщик мусора) и предоставляет встроенные функции.
- **Ruby MRI (Matz's Ruby Interpreter):**
    
    - Основная реализация языка Ruby.
    - Обеспечивает интерпретацию, управление памятью и взаимодействие с ОС.
- **PHP Runtime:**
    
    - Интерпретирует PHP-код, управляет памятью и взаимодействует с сервером (например, через Apache или Nginx).
### 3. **Среды выполнения для JavaScript**

JavaScript имеет несколько runtime-технологий, каждая из которых предоставляет функции для выполнения кода и взаимодействия с ОС.

- **Node.js:**
    
    - Runtime для выполнения JavaScript вне браузера.
    - Использует движок V8 (Google) для интерпретации и выполнения кода.
    - Обеспечивает асинхронную модель ввода-вывода.
- **Deno:**
    
    - Современный аналог Node.js, разработанный для безопасности и удобства.
    - Поддерживает TypeScript "из коробки".
    - Выполняет JavaScript/TypeScript в изолированной среде.
### 4. **Компиляторы с Just-In-Time (JIT)**

Системы, которые компилируют код во время выполнения, схожи с runtime в функциональности.

- **LLVM (Low Level Virtual Machine):**
    
    - Набор инструментов для создания компиляторов.
    - Используется в Clang, Rust и других языках для оптимизации во время выполнения.
- **Mono Runtime:**
    
    - Реализация .NET Framework с поддержкой JIT-компиляции.
    - Используется для выполнения приложений на C# и других языках .NET.
### 5. **Системы управления потоками и параллелизмом**

Планировщики и библиотеки для параллельного выполнения задач часто дополняют runtime.

- **Erlang VM (BEAM):**
    
    - Высокопроизводительная среда выполнения для Erlang.
    - Поддерживает параллелизм, отказоустойчивость и масштабируемость.
- **GHC Runtime System:**
    
    - Среда выполнения для Haskell.
    - Обеспечивает поддержку функционального программирования и параллелизма.
- **Akka:**
    
    - Фреймворк для работы с акторной моделью параллелизма на JVM.
### 6. **Платформы для работы с контейнерами**

Среды, которые обеспечивают изоляцию и управление средой выполнения.

- **Docker Runtime:**
    
    - Управляет контейнерами, предоставляя изолированную среду для приложений.
    - Использует технологии виртуализации, чтобы обеспечить кросс-платформенность.
- **Kubernetes Runtime (CRI):**
    
    - Интерфейс для управления контейнерами в кластерах Kubernetes.
### 7. **Игровые и графические runtime**

Игровые движки также предоставляют runtime для выполнения логики игры.

- **Unity Runtime:**
    
    - Выполняет игровые скрипты, написанные на C#.
    - Управляет графикой, физикой и пользовательским вводом.
- **Unreal Engine Runtime:**
    
    - Обеспечивает выполнение кода на C++ или Blueprints.
### 8. **Облачные runtime**

Среды выполнения для серверных и облачных приложений.

- **AWS Lambda Runtime:**
    
    - Исполняемая среда для запуска функций в облаке.
    - Поддерживает множество языков, таких как Python, Go, Node.js и Java.
- **Google Cloud Functions Runtime:**
    
    - Среда для выполнения облачных функций с поддержкой динамического масштабирования.
### 9. **Языки с собственным runtime**

Некоторые языки имеют уникальные runtime-механизмы.

- **Go Runtime:**
    - Встроенная поддержка конкурентности через горутины и каналы.
    - Использует сборщик мусора и встроенный планировщик.
- **Rust (с минимальным runtime):**
    - Rust избегает традиционных runtime, полагаясь на низкоуровневую оптимизацию.
    - Управление памятью выполняется вручную или через механизмы безопасности.

### Сравнение

| **Технология**     | **Сборка мусора** | **Поддержка многозадачности**    | **Платформозависимость** |
| ------------------ | ----------------- | -------------------------------- | ------------------------ |
| Go Runtime         | Да                | Горутины                         | Независимая              |
| JVM                | Да                | Потоки                           | Независимая              |
| Python Interpreter | Да                | Потоки (Global Interpreter Lock) | Независимая              |
| Node.js            | Нет               | Асинхронные события              | Независимая              |
| Docker Runtime     | Нет               | Контейнеры                       | Зависимая от ОС          |