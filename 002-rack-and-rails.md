# Цель

* познакомиться с rack, sinatra и rails
* написать hello world rack приложение в одном файле
* написать на Sinatra в модульном стиле hello world приложение
* написать блог на рельсах

# Rack/Sinatra

## Теория
* rack // объект с методом call
* bundler
* rspec

## Шаги
* создаем файл application.rb
* прикручиваем bundler http://bundler.io/bundler_setup.html  // Bundler.require(:default)
* ставим rspec // group :test
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
