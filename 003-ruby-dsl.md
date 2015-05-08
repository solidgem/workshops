# Цель
Научиться писать DSL, создать gem.


# Теория

* [Предметно-ориентированный язык](https://ru.wikipedia.org/wiki/%D0%9F%D1%80%D0%B5%D0%B4%D0%BC%D0%B5%D1%82%D0%BD%D0%BE-%D0%BE%D1%80%D0%B8%D0%B5%D0%BD%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D1%8B%D0%B9_%D1%8F%D0%B7%D1%8B%D0%BA)

# Что нужно сделать

1. согдать каркас gem
2. написать библиотеку

# Как это выглядит

```ruby
Configus.build :development do
  env :production do
    email 'production@email.com'
    house 'White House'
    cool_hash one: 1
    some_proc -> { 1 + 1 }
  end

  env :development, parent: :production do
    email 'development@email.com'
    settings do
      server 'cool.serv.com'
    end
  end
end

Configus.config.email #=> 'development@email.com'
Configus.config.settings.server #=> 'cool.serv.com'
```


# Книги

* [Предметно-ориентированные языки программирования // Мартин Фаулер](http://www.ozon.ru/context/detail/id/6967089/)

# Благодарности

Мокевнину Кириллу за написание первой версии и объяснению как как это делать.
