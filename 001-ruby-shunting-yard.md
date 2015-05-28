# Цель

Изучить базовый ruby синтаксис, научиться работать с массивами, стеком, очередью.

# Общая теория

* [quickstart](https://www.ruby-lang.org/ru/documentation/quickstart/)
* [ruby-from-other-languages](https://www.ruby-lang.org/ru/documentation/ruby-from-other-languages/)
* [to-ruby-from-php](https://www.ruby-lang.org/ru/documentation/ruby-from-other-languages/to-ruby-from-php/)

# Задание

Реализовать на языке ruby калькулятор выражений со скобками, используя обратную польскую запись.
Например, вычисляем выражения:

```
5 * (1 + 2)
1 + 6 * 20
```

# Требования

* использовать обратную польскую запись
* только натуральные числа и ноль (0, 1, 2, ...)
* бинарные операторы: +, -, *, /
* `*, /` приоритетнее `+, -`

# Разработка 

* парное программирование
* весь код в одном файле
* разрабатываем через TDD
* в качестве тестов используем печать на экран: выводим выражение, результат и ожидаемый результат
* rspec не используем

# Полезные ссылки

* [обратная польская запись](https://ru.wikipedia.org/wiki/%D0%9E%D0%B1%D1%80%D0%B0%D1%82%D0%BD%D0%B0%D1%8F_%D0%BF%D0%BE%D0%BB%D1%8C%D1%81%D0%BA%D0%B0%D1%8F_%D0%B7%D0%B0%D0%BF%D0%B8%D1%81%D1%8C)
* [алгоритм сортировочной станции](https://ru.wikipedia.org/wiki/%D0%90%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC_%D1%81%D0%BE%D1%80%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%BE%D1%87%D0%BD%D0%BE%D0%B9_%D1%81%D1%82%D0%B0%D0%BD%D1%86%D0%B8%D0%B8)
* [ruby документация](http://ruby-doc.org/)
* [String](http://ruby-doc.org/core-2.2.0/String.html)
* [Array](http://ruby-doc.org/core-2.2.0/Array.html)
* [Hash](http://ruby-doc.org/core-2.2.0/Hash.html)
* [Enumerable](http://ruby-doc.org/core-2.2.0/Enumerable.html)
* [Regexp](http://ruby-doc.org/core-2.2.0/Regexp.html)

# Полезные методы

* String#scan
* String#empty?
* Array#push
* Array#pop
* Enumerable#map
* Enumerable#reduce

# Книги

* [Программирование на языке Ruby](http://www.ozon.ru/context/detail/id/3411405/)
