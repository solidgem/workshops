* es6
 * [обзор нововведений](https://babeljs.io/docs/learn-es2015/)
 * модули
 * сравнение с [coffee-script](http://coffeescript.org/)
 * обзор транспиллеров: [babel](https://babeljs.io), [traceur](https://github.com/google/traceur-compiler)
* менеджеры пакетов
 * [webpack](http://webpack.github.io/)
 * [browserify](http://browserify.org/)
 * [jspm](http://jspm.io/)
* системы сборки
 * [gulp](http://gulpjs.com/)
 * [broccoli](https://github.com/broccolijs/broccoli) [классная статья на хабре](http://habrahabr.ru/post/216715/)
* подробнее про jspm, system.js
* [react.js](https://facebook.github.io/react/)
* [функционалное программирование в браузере](http://tonsky.me/talks/2015-frontendconf/)
 * нарисовать диаграмму(из модели получаем DOM, сами переводим модель из одного состояния в другое, бибилиотека применяет изменения в DOM)
 * clojure
 * атомы [js-atom](https://github.com/cjohansen/js-atom)
 * иммутабельность
 * персистентные структуры данных
 * [immutable.js](https://facebook.github.io/immutable-js/)
* практика
 * написать простой TODO на jspm, react.js, immutable.js

Диаграмма из [доклада Никиты Прокопова](http://tonsky.me/talks/2015-frontendconf/)
![диаграмма @tonsky](http://tonsky.me/talks/2015-frontendconf/0130%20model-model-dom-dom.png)
 
# Видео 
 
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/NpMnRifyGyw/0.jpg)](http://www.youtube.com/watch?v=NpMnRifyGyw)
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/szJjsduHBQQ/0.jpg)](http://www.youtube.com/watch?v=szJjsduHBQQ)
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/I7IdS-PbEgI/0.jpg)](http://www.youtube.com/watch?v=I7IdS-PbEgI)


# Достоинства

* легко тестировать(чистые функции)
* можно не рендерить целые поддеревья
* можно рендерить по таймеру, в случае очнь частого изменения данных
* легко сделать историю изменений
* можно по таймеру скидывать в бэкенд изменения


моя реализация https://github.com/darkleaf/react-immutable-todo
