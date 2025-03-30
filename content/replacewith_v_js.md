+++
date = '2025-03-08T00:53:24+03:00'
title = 'Метод replaceWith() в Javascript'
categories = [ "javascript" ]
+++

Метод `replaceWith()` позволяет заменить существующий элемент другим элементом или текстом, полностью удаляя старый узел из `DOM`.

```js
element.replaceWith(newElement);
```

Тут `newElement` это новый элемент, текст или несколько узлов, которые заменят старый элемент

Пример с заменой 

```js
let oldItem = document.getElementById('old');
let newItem = document.createElement('div');
newItem.textContent = 'Я новый элемент!';
oldItem.replaceWith(newItem);
```

Пример с заменой элемента на текст

```js
document.getElementById('title').replaceWith('Тут был Dxrkd3v');
```

Метод `replaceWith()` инструмент для замены элементов без изменения родительской структуры. Он идеально подходит, когда нужно подменить компонент без удаления или модификации других элементов.