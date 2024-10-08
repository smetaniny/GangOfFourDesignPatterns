# Шаблон "Одиночка" (Singleton)

Шаблон "Одиночка" гарантирует, что класс имеет только один экземпляр, и предоставляет глобальную точку доступа к этому
экземпляру. Это полезно, когда необходимо контролировать доступ к ресурсам, которые не должны иметь несколько
экземпляров.

### Пример паттерна на react

https://www.npmjs.com/package/smetaniny-react-singleton

## Что это такое?

Шаблон "Одиночка" используется для создания класса, который может иметь только один экземпляр. Это достигается путем
скрытия конструктора и предоставления статического метода для получения доступа к экземпляру.

## Когда использовать?

- Когда требуется обеспечить единственный экземпляр класса, например, для управления конфигурацией или общими ресурсами.
- Когда необходимо контролировать доступ к какому-либо ресурсу или сервису.
- Когда управление состоянием объекта должно быть централизованным.

## Как это работает?

### Компоненты:

1. **Одиночка:** Класс, который обеспечивает доступ к своему единственному экземпляру через статический метод.
2. **Статический метод:** Метод, который возвращает экземпляр одиночки, создавая его, если он еще не существует.

## Плюсы

- **Контроль над экземпляром:** Гарантирует, что будет создан только один экземпляр класса.
- **Глобальный доступ:** Обеспечивает легкий доступ к экземпляру из разных частей приложения.
- **Упрощение кода:** Убирает необходимость передавать экземпляр через параметры или хранить его в статических
  переменных.

## Минусы

- **Проблемы с тестированием:** Усложняет юнит-тестирование, так как статический доступ к экземпляру может мешать
  изоляции тестов.
- **Глобальное состояние:** Может привести к затруднениям в управлении состоянием, если разные части кода зависят от
  одного экземпляра.
- **Потенциальные проблемы с многопоточностью:** Если не реализован правильно, может привести к созданию нескольких
  экземпляров в многопоточной среде.

## Почему это полезно?

- Позволяет централизовать управление состоянием и ресурсами, обеспечивая легкий доступ к единственному экземпляру.
- Упрощает код, устраняя необходимость в передаче экземпляра между классами.
- Позволяет избежать дублирования ресурсов и снизить вероятность ошибок.

## Участники

- **Singleton** - одиночка. Определяет операцию Instance, которая позволяет клиентам получить доступ к единственному
  экземпляру экземпляру. Instance - это операция класса, то есть метод класса и несет ответственность за создание
  абсолютно уникального экземпляра.

## Структура

![uml](uml.png)


