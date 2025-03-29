+++
date = '2025-03-28T09:00:24+03:00'
title = 'Объект style в JavaScript'
categories = [ "javascript" ]
+++

Объект `style` позволяет изменять CSS-стили элементов прямо через `JavaScript`. С его помощью можно динамически менять цвета, размеры, шрифты и любые другие стили без редактирования CSS-файлов.

Чтобы изменить стили элемента, сначала нужно получить его в `JavaScript`, а затем обратиться к его свойству `style`

```js
let element = document.getElementById('myElement'); 
element.style.color = 'red'; 
// Меняем цвет текста на красный
```

Объект `style` содержит свойства, соответствующие CSS-стилям. Однако названия записываются в `camelCase`, а не через дефис `-` как в обычном `css`


| CSS-свойство     | JavaScript-эквивалент                  |
|------------------|---------------------------------------|
| background-color | element.style.backgroundColor = 'blue' |
| font-size        | element.style.fontSize = '20px'       |
| margin-top       | element.style.marginTop = '10px'      |

<br />

```js
let box = document.querySelector('.box');

box.style.width = '200px';
box.style.height = '100px';
box.style.backgroundColor = 'yellow';
box.style.border = '2px solid black';
```

Чтобы удалить стиль, можно присвоить пустую строку

```js
box.style.backgroundColor = ''; 
// Сбросит цвет фона
```

Объект `style` позволяет динамически изменять внешний вид элементов. Но если нужно задавать много стилей сразу, лучше использовать `classList.add()` и `classList.remove()` для работы с классами.