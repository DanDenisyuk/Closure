# Programming Dictionary

## Базовые понятия

- [Абстракция / Abstraction](https://github.com/HowProgrammingWorks/Abstractions)
  - обобщенное (абстрактное) решение задачи, в отличие от конкретного решения, подходящее для широкого круга задач
  - модель реального объекта (или множества объектов), являющаяся приближением к реальности, обобщением
  - множество свойств объекта, относящиеся к определенному его аспекту
  - [Слои абстракций / Abstraction Layer](https://github.com/HowProgrammingWorks/AbstractionLayers)
- Парадигма программирования / Programming Paradigm
- [Переменная / Variable](https://github.com/HowProgrammingWorks/DataTypes)
  - `let cityName = 'Beijing';`
- [Константа / Constant](https://github.com/HowProgrammingWorks/DataTypes)
  - `const cityName = 'Beijing';`
- [Типы данных / Data Types](https://github.com/HowProgrammingWorks/DataTypes)
  - `[5, 'Kiev', true, { city: 'Beijing' }, a => ++a ].map(x => typeof(x));`
- [Скалярные типы / Scalar Types](https://github.com/HowProgrammingWorks/DataTypes)
- [Ссылочные типы / Reference](https://github.com/HowProgrammingWorks/DataTypes)
- [Объект / Object](https://github.com/HowProgrammingWorks/DataTypes)
- Инстанциирование / Instantiation
  - `const rect1 = new Rectangle(-50, -50, 100, 150);`
- Класс / Class
  - `class Point { constructor(x, y) { this.x = x; this.y = y; } }`
- Прототип / Protorype
- [Cтруктуры данных](https://github.com/HowProgrammingWorks/DataStructures)
- Массив / Array
  - `const cities = ['Tehran', 'Yalta', 'Potsdam'];`
- [Функция](https://github.com/HowProgrammingWorks/Function)
  - Объявление функции / Function definition
    - `function max(a, b) { return a + b; }`
  - Функциональное выражение / Function expression
    - Функциональное выражение с именованной функцией / Named function expression
      - `const max = function max(a, b) { return a + b; };`
    - Анонимное функциональное выражение / Anonymous function expression
     - `const max = function(a, b) { return a + b; };`
    - Лямбда функция / Lambda function
      - `const max = (a, b) => { return a + b; };`
    - Лябмда выражение, Функция-стрелка / Lambda expression, Arrow function
      - `const max = (a, b) => (a + b);`
  - [Чистая функция / Pure Function](https://github.com/HowProgrammingWorks/Function)
  - [Замыкание / Closure](https://github.com/HowProgrammingWorks/Closure)
    - `const add = a => b => a + b;`
    - Пример:
```js
const hash = () => {
  const data = {};
  return (key, value) => {
    data[key] = value;
    return data;
  };
};
```
  - [Суперпозиция / Superposition](https://github.com/HowProgrammingWorks/Composition)
    - `const expr2 = add(pow(mul(5, 8), 2), div(inc(sqrt(20)), log(2, 7)));`
  - [Композиция / Composition](https://github.com/HowProgrammingWorks/Composition)
    - `const compose = (f1, f2) => x => f2(f1(x));`
    - `const compose = (...funcs) => (...args) => (funcs.reduce((args, fn) => [fn(...args)], args));`
  - [Частичное применение / Partial application](https://github.com/HowProgrammingWorks/PartialApplication)
    - `const partial = (fn, x) => (...args) => fn(x, ...args);`
  - [Каррирование / Currying](https://github.com/HowProgrammingWorks/PartialApplication)
    - `const result = curry((a, b, c) => (a + b + c))(1, 2)(3);`
    - [Побочные эффекты / Side effects](https://github.com/HowProgrammingWorks/Function)
  - [Функция высшего порядка / Higher-order Function](https://github.com/HowProgrammingWorks/HigherOrderFunction)
    - Если функция только в аргументах, то это колбек
    - Если функция только в результате, то это фабрика функций
    - Если функция в аргументах и в результате, то это обертка
  - Функциональное наследование / Functional Inheritance
- [Метод / Method](https://github.com/HowProgrammingWorks/Function)
  - Пример:
```js
const p1 = {
  x: 10, y: 10,
  quadrant() {
    if (this.x > 0) return this.y > 0 ? 'I' : 'IV';
    return this.y > 0 ? 'II' : 'III';
  }
}
```
- [Контекст](https://github.com/HowProgrammingWorks/Function)
- [Область видимости / Scope](https://github.com/HowProgrammingWorks/Function)
- [Обертка / Wrapper](https://github.com/HowProgrammingWorks/Wrapper)
- Интерфейс / Interface
- Прикладной интерфейс / Application Interface, API
- Синглтон / Singleton
- [Функция обратного вызова, колбек / Callback](https://github.com/HowProgrammingWorks/Callbacks)
- [Событие / Event](https://github.com/HowProgrammingWorks/Callbacks)
- [Лисенер / Listener](https://github.com/HowProgrammingWorks/Callbacks)
- [Дифер / Deferred](https://github.com/HowProgrammingWorks/Callbacks)
- [Промис / Promise](https://github.com/HowProgrammingWorks/Promise)
- [Фьючер / Future](https://github.com/HowProgrammingWorks/Callbacks)
- [Итерирование / Iteration](https://github.com/HowProgrammingWorks/Iteration)
- [Итератор / Iterator](https://github.com/HowProgrammingWorks/Iteration)
- [Цикл / Loop](https://github.com/HowProgrammingWorks/Iteration)
- [Условие / Conditional statements](https://github.com/HowProgrammingWorks/Conditional)
- [Строка / String](https://github.com/HowProgrammingWorks/String)
- [Коллекция / Collection](https://github.com/HowProgrammingWorks/Collections)
- [Множество / Set](https://github.com/HowProgrammingWorks/Set)
- [Ключ-значение, Хешмап / Map, Key-value](https://github.com/HowProgrammingWorks/KeyValue)
- [Список / List](https://github.com/HowProgrammingWorks/LinkedList)
- [Дерево](https://github.com/HowProgrammingWorks/TreeNode)
- [Граф / Graph](https://github.com/HowProgrammingWorks/DirectedGraph)
- [Файл / File](https://github.com/HowProgrammingWorks/Files)
- [Поток, Файловый поток / Stream, File Stream](https://github.com/HowProgrammingWorks/Streams)
- [Буфер / Buffer](https://github.com/HowProgrammingWorks/Buffers)
- [Сокет / Socket](https://github.com/HowProgrammingWorks/Socket)
- [Дескриптор / Descriptor](https://github.com/HowProgrammingWorks/Files)
- Состояние / State
- Кэш, Кэширование / Cache
- Хэш, Хэширование / Hashing
- [Функциональный объект](https://github.com/HowProgrammingWorks/Functor)
  - [Функтор / Functor](https://github.com/HowProgrammingWorks/Functor)
    - Рекурсивное замыкание / Recursive closure
    - Объект функционального типа, хранящий в себе защищенное значение и позволяющий отобразить это значение в другой функтор через функцию
  - [Аппликативный функтор](https://github.com/HowProgrammingWorks/Functor)
  - Монада / Monad
- [Мемоизация / Memoization](https://github.com/HowProgrammingWorks/Memoization)
- [Примесь / Mixin](https://github.com/HowProgrammingWorks/Mixin)
  - Добавление свойств, методов или поведения к объекту после его инстанциирования (создания)
- Декоратор / Decorator
- [Наследование / Inheritance](https://github.com/HowProgrammingWorks/Function)
- Множественное наследование / Multiple Inheritance
- Непрямое наследование / Indirect Inheritance
- [Генератор / Generator](https://github.com/HowProgrammingWorks/Generator)
- [Синхронные операции](https://github.com/HowProgrammingWorks/AsynchronousProgramming)
- [Асинхронные операции](https://github.com/HowProgrammingWorks/AsynchronousProgramming)
- [Ввод/вывод / I/O, Input-output](https://github.com/HowProgrammingWorks/AsynchronousProgramming)
- [EventEmitter](https://github.com/HowProgrammingWorks/EventEmitter)
- [Чеининг / Chaining](https://github.com/HowProgrammingWorks/Chaining)
- [Сериализация / Serialization](https://github.com/HowProgrammingWorks/Serialization)
- [Десериализация / Deserialization](https://github.com/HowProgrammingWorks/Serialization)
- Парсинг / Parsing
- [Регулярные выражения / Regular Expressions](https://github.com/HowProgrammingWorks/RegExp)
- [Модуль, модульность](https://github.com/HowProgrammingWorks/Modularity)
- [Зависимость / Dependency](https://github.com/HowProgrammingWorks/Project)
- [Линтер / Linter](https://github.com/HowProgrammingWorks/Tools)
- Декомпозиция / Decomposition
- [Ленивость / Lazy](https://github.com/HowProgrammingWorks/Lazy)
- [Прокси / Proxy](https://github.com/HowProgrammingWorks/Proxy)
- [Символ / Symbol](https://github.com/HowProgrammingWorks/Symbol)
- [Обработка ошибок / Error handling](https://github.com/HowProgrammingWorks/Errors)
- [Сборка мусора / Garbage Collection](https://github.com/HowProgrammingWorks/GarbageCollection)

## Расширенные понятия

- Неизменяемые данные / Immutable Data
- Изменяемые данные / Mutable Data
- Интроспекция / Introspection
- Рефлексия / Reflection
- Скаффолдинг / Scaffolding
- [Инверсия управления / IoC, Inversion of Control](https://github.com/HowProgrammingWorks/InversionOfControl)
- [Внедрение зависимостей / DI, Dependency Injection](https://github.com/HowProgrammingWorks/DependencyInjection)
- [Межпроцессовое взаимодействие / IPC, Interprocess Communication](https://github.com/HowProgrammingWorks/InterProcessCommunication)
- [Песочница / Sandbox](https://github.com/HowProgrammingWorks/Sandboxes)
- Архитектура / Architecture
- Слой доступа к данным / Data Access Layer
- Курсор / Cursor
- Объектно-реляционное отображение / ORM, Object-relational Mapping
- Сервер приложений / Application Server
- Тонкий клиент
- Толстый клиент
- [Проекция данных / Projection](https://github.com/HowProgrammingWorks/Projection)
- [Измерение производительности / Benchmarking](https://github.com/HowProgrammingWorks/Benchmark)
- [Интерфейс командной строки / CLI, Command Line Interface and Console](https://github.com/HowProgrammingWorks/CommandLine)
- [Мониторинг файловой системы / File System Watching](https://github.com/HowProgrammingWorks/Files)
- Метаданные
- Протокол

## Парадигмы программирования

- [Императивное программирование / Imperative Programming](https://github.com/HowProgrammingWorks/ImperativeProgramming)
  - Неструктурное программирование / Non-structured
  - Структурное программирование / Structured Programming
  - Процедурное программирование / Procedural Programming
  - [Object-oriented programming](https://github.com/HowProgrammingWorks/ObjectOrientedProgramming)
  - [Prototype-oriented programming](https://github.com/HowProgrammingWorks/PrototypeOrientedProgramming)
- [Функциональное программирование / Functional Programming](https://github.com/HowProgrammingWorks/FunctionalProgramming)
- [Логическое программирование / Logical Programming]
- [Декларативное программирование / Declarative Programming]
- [Программирование управляемое данными / Data-driven Programming](https://github.com/HowProgrammingWorks/DataDrivenProgramming)
- Техники программирования
  - [Асинхронное программирование / Asynchronous Programming]
  - [Реактивное программирование / Reactive Programming]
- [Событийное программирование / Event-driven Programming](https://github.com/HowProgrammingWorks/EventDrivenProgramming)
- [Метапрограммирование / Metaprogramming](https://github.com/HowProgrammingWorks/Metaprogramming)
