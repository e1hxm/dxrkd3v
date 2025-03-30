+++
date = '2025-03-30T7:00:24+03:00'
title = 'Методы append и prepend в JavaScript'
categories = [ "javascript" ]
+++

Методы `append()` и `prepend()` позволяют добавлять элементы или текст в начало или конец другого элемента. Они делают код чище и удобнее по сравнению с `appendChild()`.

### element.append() — добавление в конец

Метод `append()` вставляет содержимое в конец элемента. Он принимает не только элементы, но и строки

```js
let container = document.getElementById('box');
let newDiv = document.createElement('div');
newDiv.textContent = 'Новый элемент';
container.append(newDiv, ' А это просто текст');
```

### element.prepend() — добавление в начало

Метод `prepend()` вставляет содержимое в начало элемента.

```js
let list = document.getElementById('myList');
let newItem = document.createElement('li');
newItem.textContent = 'Новый первый пункт';
list.prepend(newItem);
```

`append()` и `prepend()` — лаконичные методы, позволяющие добавлять элементы в `DOM`. Они заменяют `appendChild()`, делают код компактнее и позволяют вставлять сразу несколько значений.
