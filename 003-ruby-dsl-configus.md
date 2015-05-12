# Это первая часть

[вторая часть](004-configus.md)

# Цель
Научиться писать DSL, создать gem.

# Прочитать перед тем как начать

* http://nashbridges.me/introducing-ruby-oop
* http://nashbridges.me/procs-and-lambdas
* http://nashbridges.me/blocks-in-ruby

# Теория

* [Предметно-ориентированный язык](https://ru.wikipedia.org/wiki/%D0%9F%D1%80%D0%B5%D0%B4%D0%BC%D0%B5%D1%82%D0%BD%D0%BE-%D0%BE%D1%80%D0%B8%D0%B5%D0%BD%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D1%8B%D0%B9_%D1%8F%D0%B7%D1%8B%D0%BA)
* внешние DSL (SQL, Regexp, configs)
* внутренние DSL (mothod chain, ...)

# Что нужно сделать

1. согдать каркас gem
2. написать библиотеку

# Как это выглядит

```ruby
# :development показывает, что стоим конфиг для development окружения 
Configus.build :development do
  env :production do
    email 'production@email.com'
    house 'White House'
    some_proc -> { 1 + 1 }
  end

  env :development do
    email 'old_login@email.com'
    email 'development@email.com' # переопределяем ключ
  end
end

Configus.config.email #=> 'development@email.com'
```

# Что читать в процессе

## Создание гема
* **команда** `bundle gem configus --test=rspec`
* http://bundler.io/v1.9/bundle_gem.html
* http://www.smashingmagazine.com/2014/04/08/how-to-build-a-ruby-gem-with-bundler-test-driven-development-travis-ci-and-coveralls-oh-my/
* http://stackoverflow.com/questions/4398262/setup-rspec-to-test-a-gem-not-rails
* http://railscasts.com/episodes/245-new-gem-with-bundler

## Метапрограммирование
* http://ruby-doc.org/core-2.1.0/BasicObject.html
* http://ruby-doc.org/core-2.1.0/BasicObject.html#method-i-method_missing
* http://ruby-doc.org/core-2.1.0/BasicObject.html#method-i-instance_exec
* http://ruby-doc.org/core-2.1.0/Object.html#method-i-define_singleton_method

# Интерфейс
* Configus.build
* Configus.config

# Архитектура

```ruby
#lib/configus.rb
module Configus
  class << self
    def build(env, &block)
      @config = Builder.build env, &block
    end
    
    def config
      @config
    end
  end
end

#lib/configus/proxy.rb
module Configus
  class Proxy < BasicObject
    # some code
    
    def method_missing(key, value)
      # код ниже только для примера
      
      # в BasicObject нет метода p, по этому так=)
      Kernel.p key
      Kernel.p value
    end
  end
end
```

```ruby
Configus::Proxy.new.instance_exec do 
  some_method "some value" # напечатает на экран :some_method "some value"
end
```

* контекст исполнения для method_missing: `Configus::Proxy < BasicObject` 
* `Configus.config` возвращает экземпляр `Configus::Config` 

# Требования

* использовать rspec
* использовать TDD

# Книги

* [Предметно-ориентированные языки программирования // Мартин Фаулер](http://www.ozon.ru/context/detail/id/6967089/)

# Благодарности

Мокевнину Кириллу за написание оригинального configus и объяснение как он устроен.
Ссылку осознанно не привожу, что бы не подсматривали ;)
