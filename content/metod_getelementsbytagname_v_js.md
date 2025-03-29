+++
date = '2025-03-26T09:00:24+03:00'
title = 'Метод getElementsByTagName в JavaScript'
categories = [ "javascript" ]
+++

Метод `getElementsByTagName` в `JavaScript` позволяет находить элементы на странице по названию их тега. Это очень удобно, если нужно работать с группой однотипных элементов, например, всеми `<p>`, `<div>`, `<input>` и так далее.

```js
document.getElementsByTagName('div');
//вернет все дивки со страницы
```

Метод возвращает `HTMLCollection` — живую коллекцию элементов, которые соответствуют указанному тегу. Если элементы добавятся или удалятся из `DOM`, коллекция автоматически обновится.

Если таких элементов на странице нет, метод вернёт пустую коллекцию.

Запуск поиска всех параграфов на странице:

```js
let paragraphs = document.getElementsByTagName('p');
console.log(paragraphs); // Выведет коллекцию всех <p>
```
Замена стилей для всех кнопок на странице:

```js
let buttons = document.getElementsByTagName('button');
for (let button of buttons) {
  button.style.background = 'gray'; // Все кнопки станут серыми
}
```

Достучимся до первого `<h1>` тега на странице:

```js
let heading = document.getElementsByTagName('h1')[0]; 
heading.textContent = 'Новый заголовок!';
```

Метод `getElementsByTagName` прекрасно подойдет если  нужно быстро получить все элементы определённого тега. Однако если требуется статичный список или сложные селекторы, лучше использовать `querySelectorAll`