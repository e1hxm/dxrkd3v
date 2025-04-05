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
  console.log(event); // Покажет все свойства события
});
```

<div class="typed-container">
<span id="typed-2"></span>
<div class="typed-strings" style="display: none;">
<p>👉 Покажет все свойства события</p>
</div>
</div>
<div id="typed-strings" style="display: none;">
</div>