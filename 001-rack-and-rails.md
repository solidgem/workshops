# Цель

* познакомиться с rack, sinatra и rails
* написать hello world rack приложение в одном файле
* написать на Sinatra в модульном стиле hello world приложение
* написать блог на рельсах

# Шаги

## Rack/Sinatra
* прикручиваем bundler
* ставим rspec
* пишем тест(get '/')
* rack приложение HelloWorldApp = ->(env){...}
* пишем config.ru
* подключаем thin
* подключаем sinatra
* заменяем HelloWorldApp на sintara
* запускаем тесты
* прикручиваем http аутентификацию
* пишем middleware которая на get запрос выдает пасхалку случайным образом


