+++
date = '2025-03-09T00:53:24+03:00'
title = 'Метод remove() в Javascript'
categories = [ "javascript" ]
+++

Метод `remove()` позволяет удалить элемент со страницы без необходимости обращаться к его родителю. Это самый удобный способ удаления элементов в современном `JavaScript`.

```js
element.remove();
```

Удаление элемента со страницы по id

```js
let element = document.getElementById('box');
element.remove(); 
// Полностью убираем элемент с id "box"
```

Удаление элемента по классу

```js
document.querySelector('.item').remove();
```

Удаление всех элементов списка, с помощью комбинации с `forEach()`

```js
document.querySelectorAll('.list-item').forEach(item => item.remove());
```

Удаление элементов со страницы, после событий, например при клине на чем либо

```js
document.getElementById('deleteBtn').addEventListener('click', function () {
  this.remove(); 
  // Кнопка удалит саму себя
});
```

Метод `remove()` помогает с удалением элементов из DOM. Он избавляет от лишнего кода и делает работу с динамическими интерфейсами удобнее.