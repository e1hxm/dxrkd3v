+++
date = '2025-03-29T10:00:24+03:00'
title = 'Метод createElement в JavaScript'
categories = [ "javascript" ]
+++

Метод `document.createElement()` позволяет создавать новые HTML-элементы прямо в `JavaScript`. Это основной способ динамического добавления контента на страницу.

Синтаксис метода

```js
let element = document.createElement(tagName);
```

В момент вызова метода, следует подставить значение `HTML-тега` например `div`, `p`, `h1` и так далее.

Для примера я создам `div` и встрою его в конце `body`

```js
let newDiv = document.createElement('div'); 
newDiv.textContent = 'Тут был Dxrkd3v =)';
document.body.appendChild(newDiv); 
// Добавляет div в конец body
```

Пример с добавлением `CSS-стилей` и классов

```js
let button = document.createElement('button');
button.textContent = 'Я кнопка';
button.classList.add('btn');
button.style.background = 'black';
document.body.appendChild(button);
```

Встраивание тегов в определенном месте с помощью метода `insertBefore()`

```js
let list = document.getElementById('myList'); 
let newItem = document.createElement('li');
newItem.textContent = 'Новый пункт';
list.insertBefore(newItem, list.firstChild); 
// Втыкаем в начало списка
// Новый элемент
```

`document.createElement()` главный инструмент, который позволяет строить динамический интерфейс без постоянных перерисовок. Это особенно полезно при работе с интерактивными списками, динамическим контентом и реактивными UI-компонентами наподобие `React` на котором я мечтаю начать верстать =)