+++
date = '2025-03-31T10:00:24+03:00'
title = 'Свойства событий в JavaScript'
categories = [ "javascript" ]
+++

Каждое событие в `JavaScript` содержит множество свойств, которые предоставляют информацию о том, что произошло. 
Эти свойства позволяют нам понять, какие элементы были вовлечены в событие, какие клавиши были нажаты, где находился курсор и другие детали.

Другими словами свойства событий — это данные, которые содержат информацию о событии, когда оно происходит. Эти свойства доступны внутри обработчиков событий и дают возможность узнать, что именно произошло.

Пример с `event`

```js
document.getElementById('myButton').addEventListener('click', function(event) {
  console.log(event); 
});
// Покажет все свойства события
```

#### Основные свойства событий

1 - `type`

Свойство `type` сообщает, какой тип события произошел (например, `click`, `keydown`, `submit`).

```js
document.getElementById('myButton').addEventListener('click', function(event) {
  console.log(event.type); // "click"
});
```

2 - `target`

Свойство `target` возвращает элемент, на котором произошло событие. Это позволяет узнать, какой именно элемент был вовлечен в событие.

```js
document.getElementById('myButton').addEventListener('click', function(event) {
  console.log(event.target); // Покажет элемент, на который нажали
});
```

3 - `currentTarget`

Свойство `currentTarget` возвращает элемент, к которому был привязан обработчик события, а не тот, на котором событие произошло. Это особенно полезно при делегировании событий.

```js
document.getElementById('parent').addEventListener('click', function(event) {
  console.log(event.currentTarget); // Покажет родительский элемент, на который повешен обработчик
});
```

4 - `clientX` и `clientY`

Эти свойства содержат координаты курсора мыши в момент возникновения события. Значения измеряются относительно области просмотра окна (без учета прокрутки).

```js
document.addEventListener('click', function(event) {
  console.log(`X: ${event.clientX}, Y: ${event.clientY}`);
});
```

5 - `pageX` и `pageY`

Свойства `pageX` и `pageY` дают координаты мыши относительно всей страницы, включая прокрутку. Эти свойства полезны, когда необходимо учитывать прокрученную часть страницы.

```js
document.addEventListener('click', function(event) {
  console.log(`Page X: ${event.pageX}, Page Y: ${event.pageY}`);
});
```

6 - `keyCode` и `code`

Свойства `keyCode` и code используются для событий клавиатуры. `keyCode` возвращает числовой код клавиши, а code — физический код клавиши, независимо от того, какая клавиша была нажата (например, `Enter`, `Space`, `ArrowUp`).

```js
document.addEventListener('keydown', function(event) {
  console.log(`keyCode: ${event.keyCode}, code: ${event.code}`);
});
```

7 - `button`

Свойство `button` указывает, какая кнопка мыши была нажата. Для правой кнопки мыши, это значение будет равно `2`, для средней — `1`, а для левой — `0`.

```js
document.addEventListener('mousedown', function(event) {
  console.log(`Button: ${event.button}`); // Покажет номер кнопки мыши
});
```

8 - `detail`

Свойство `detail` хранит количество кликов мыши в событиях `click`. Это свойство полезно при отслеживании двойных кликов.

```js
document.addEventListener('click', function(event) {
  console.log(`Количество кликов: ${event.detail}`);
});
```

Свойства событий предоставляют возможности для получения подробной информации о том, что произошло на странице. Использование этих свойств позволяет более гибко и точно обрабатывать различные события, обеспечивая более эффективное взаимодействие с пользователем.