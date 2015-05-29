* explain
 * рассказать как читать
 * explain analyze
* [оконные функции](http://www.postgresql.org/docs/9.4/static/tutorial-window.html)
* типы данных [документация](http://www.postgresql.org/docs/8.4/static/datatype.html)
 * [функции над данными](http://www.postgresql.org/docs/9.4/static/functions.html)  
 * enum 
  * [doc](http://www.postgresql.org/docs/9.4/static/datatype-enum.html) 
  * [functions](http://www.postgresql.org/docs/9.4/static/functions-enum.html)
 * hstore
  * rails store_accessor 
 * array 
  * [doc](http://www.postgresql.org/docs/9.4/static/arrays.html) 
  * [functions](http://www.postgresql.org/docs/9.4/static/functions-array.html)    
  * [Rails has_many + array: has_array_of](https://github.com/marshall-lee/has_array_of)
 * [full-text search](http://www.postgresql.org/docs/9.4/static/textsearch.html)
 * jsonb
 * geometric 
  * [doc](http://www.postgresql.org/docs/9.4/static/datatype-geometric.html)
  * [functions](http://www.postgresql.org/docs/9.4/static/functions-geometry.html)  
 * [Composite Types](http://www.postgresql.org/docs/9.4/static/rowtypes.html)
* индексы
 * b-tree
 * GIN
 * GiST
 * ...
* [contrib](http://www.postgresql.org/docs/9.4/static/contrib.html)
 * [ltree](http://www.postgresql.org/docs/9.4/static/ltree.html) 
 * [trigram](http://www.postgresql.org/docs/9.4/static/pgtrgm.html)
 * [cube](http://www.postgresql.org/docs/9.4/static/cube.html)
* views
 * autoupdatable views
 * materialized views
* [pup-sub](http://www.postgresql.org/docs/9.4/static/sql-notify.html)
* получение случайной записи [пример](http://habrahabr.ru/post/242999/)

# Заметки

* нужна обзорная лекция
* нужна простая практика на кошечках и собачках, что-то типа [такого](http://www.percolator.io/posts/2-vvedenie-v-strong-elasticsearch-strong)
* лучше это все разбить на 2-3 блока: теория-практика, теория-практика
* кто-то мне говорил, что индексы для полнотекста жрут кучу оперативки и вытесняют другие индексы
