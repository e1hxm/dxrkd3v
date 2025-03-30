+++
date = '2025-03-30T8:00:24+03:00'
title = 'Создание текстовых узлов с помощью createTextNode в JavaScript'
categories = [ "javascript" ]
+++

Метод `document.createTextNode()` создаёт текстовый узел без оборачивающего `HTML-тега`. Полезная вещь когда нужно добавить чистый текст в элемент, не затрагивая его структуру.

```js
let textNode = document.createTextNode('Тут был Dxrkd3v');
```

Пример встраивания текста в параграф, на чистом `JS` не редактируя `HTML`

```js
let p = document.createElement('p');  
let t = document.createTextNode('Привет, Cxd3!');  

p.appendChild(t);  
document.body.appendChild(p); 
```

Также метод позволяет менять текст на лету

```js
let div = document.getElementById('h1');  
div.appendChild(document.createTextNode('New h1!'));  
```

`createTextNode()` прикольный способ добавить текст без изменения структуры документа. Он позволяет точно управлять контентом, не нарушая существующий `HTML`. 