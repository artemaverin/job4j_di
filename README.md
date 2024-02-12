# Проект job4j_di

### Описание:

Чтобы упростить создание таких объектов, программисты придумали концепцию "внедрение зависимостей" с английского DI - dependency injection.

Идея DI.

1. Есть хранилище объектов. В нем мы будем регистрировать классы, объекты которых хотим иметь в проекте.

В нашем примере мы зарегистрируем там Tracker, StartUI, ConsoleInput.

2. Хранилище в рамках DI называется Context, то есть объекты относящиеся к предметной области нашего проекта.

3. После регистрации классов Context начинает инициализацию объектов. Он строит дерево зависимостей. Сначала он создает объекты без зависимостей.

А потом создаем объекты с зависимостями.

4. После инициализации программист может получить нужный объект из Context.

Давайте мы сделаем свою реализацию DI.

Для реализации DI используется два подхода: мета программирование, рефлексия.

В этом примере мы будем использовать рефлексию. Рефлексия позволяет узнать какие элементы имеет класс в процессе выполнения программы.
