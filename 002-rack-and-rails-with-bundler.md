# Цель

* познакомиться с rack, sinatra и rails
* познакомиться с gem, bundler
* написать hello world rack приложение в одном файле
* написать на Sinatra в модульном стиле hello world приложение
* написать блог на рельсах

# Домашнее чтение

* [Gem глазами потребителя](http://nashbridges.me/gem-for-end-user)
* [Быстрое вступление в rack](http://habrahabr.ru/post/131429/)

# Rack

* gem install rack
* однострочное прилодение через лямбду в config.ru
* rackup config.ru

# Rack/Sinatra через тесты

## Теория
* rack // объект с методом call
* bundler
* rspec

## Шаги
* создаем файл application.rb
* прикручиваем bundler http://bundler.io/bundler_setup.html  // Bundler.require(:default)
* ставим rspec // group :test // Bundler.require(:default, :test) //переменные окружения
* пишем тест(get '/') http://www.sinatrarb.com/testing.html
* rack приложение // HelloWorldApp = ->(env){...}
* пишем config.ru
* подключаем thin
* подключаем sinatra
* заменяем HelloWorldApp на sintara
* запускаем тесты
* пишем middleware которая на get запрос выдает пасхалку случайным образом

# Rails

## Теория
* rails - набор фреймворков
* active support
* MVC
* рассказать про структуру проекта
* автолоадинг

## Шаги
* генерируем рельсовое приложение с rspec, sqlite
* REST
* пишем request тест на /posts
* иерархия контроллеров
* root to: 'posts'
* делаем Web::PostsController#index
* делаем вьюху c текстом hello world
* прикручиваем factory_girl
* пишем CRUD через тесты
* валидации
* gem haml / gem slim
* gem simpleform
* gem responders

# Ссылки

* [bundler](http://bundler.io/)
* [rack](http://rack.github.io/)
* [sinatra](http://www.sinatrarb.com/)
* [rails](http://rubyonrails.org/)
* [rails getting_started](http://guides.rubyonrails.org/getting_started.html)  // собственнно, это я и буду рассказывать во второй части занятия
