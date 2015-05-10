# Цель
Научиться писать DSL, создать gem.

# Домашнее чтение

* http://nashbridges.me/introducing-ruby-oop
* http://nashbridges.me/procs-and-lambdas

# Теория

* [Предметно-ориентированный язык](https://ru.wikipedia.org/wiki/%D0%9F%D1%80%D0%B5%D0%B4%D0%BC%D0%B5%D1%82%D0%BD%D0%BE-%D0%BE%D1%80%D0%B8%D0%B5%D0%BD%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D1%8B%D0%B9_%D1%8F%D0%B7%D1%8B%D0%BA)
* внешние DSL (SQL, Regexp, configs)
* внутренние DSL (mothod chain, ...)

# Что нужно сделать

1. согдать каркас gem
2. написать библиотеку

# Как это выглядит

```ruby
Configus.build :development do
  env :production do
    email 'production@email.com'
    house 'White House'
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
Configus.config.settings.to_h #=> { server: 'cool.serv.com' }
```

# Что читать в процессе

## Создание гема
* http://bundler.io/v1.9/bundle_gem.html
* http://www.smashingmagazine.com/2014/04/08/how-to-build-a-ruby-gem-with-bundler-test-driven-development-travis-ci-and-coveralls-oh-my/
* http://stackoverflow.com/questions/4398262/setup-rspec-to-test-a-gem-not-rails
* http://railscasts.com/episodes/245-new-gem-with-bundler

## Ruby syntax
* http://nashbridges.me/blocks-in-ruby

## Метапрограммирование
* http://ruby-doc.org/core-2.1.0/BasicObject.html
* http://ruby-doc.org/core-2.1.0/BasicObject.html#method-i-method_missing
* http://ruby-doc.org/core-2.1.0/BasicObject.html#method-i-instance_eval
* http://ruby-doc.org/core-2.1.0/Object.html#method-i-define_singleton_method

# Интерфейс
* Configus.build
* Configus.config

# Архитектура
* `Configus.build` вызывает `Configus::Builder.build`
* контекст исполнения: `Configus::Proxy < BasicObject` 
* `Configus.config` возвращает экземпляр `Configus::Config` 

# Требования

* использовать rspec
* использовать TDD

# Книги

* [Предметно-ориентированные языки программирования // Мартин Фаулер](http://www.ozon.ru/context/detail/id/6967089/)

# Благодарности

Мокевнину Кириллу за написание оригинального configus и объяснение как он устроен.
Ссылку осознанно не привожу, что бы не подсматривали ;)
