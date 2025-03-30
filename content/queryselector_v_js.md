+++
date = '2025-03-22T12:00:24+03:00'
title = 'Метод querySelector() в JavaScript'
categories = [ "javascript" ]
+++

Метод `querySelector` является одним из самых популярных и мощных инструментов для поиска элементов в DOM (Document Object Model) в JavaScript. Он позволяет найти первый элемент на странице, который соответствует заданному CSS-селектору. Этот метод значительно упрощает работу с DOM по сравнению с устаревшими методами поиска элементов, такими как `getElementById`, `getElementsByClassName` и другими.

```js
document.querySelector(selector);
```

Тут `selector` это строка, представляющая CSS-селектор например, `#id`, `.class`, `div`

Метод `querySelector` возвращает первый элемент, который соответствует переданному селектору. Если такой элемент не найден, возвращается null. Важно помнить, что `querySelector` находит только первый подходящий элемент. Если на странице несколько элементов, которые соответствуют селектору, он выберет лишь первый из них.

Пример поиска элемента на странице по `id`

```js
let element = document.querySelector('#myElement');
console.log(element); 
// Вернёт элемент с id="myElement"
```

Пример поиска элемента на странице по классу

```js
let element = document.querySelector('.myClass');
console.log(element); 
// Вернёт первый элемент с классом 'myClass'
```

Запуск поиска по тегу

```js
let element = document.querySelector('div');
console.log(element); 
// Вернёт первый <div> на странице
```

Метод `querySelector` позволяет легко и быстро находить элементы для дальнейших манипуляций с ними, таких как изменение стилей, добавление событий или других действий.