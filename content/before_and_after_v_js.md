+++
date = '2025-03-30T8:03:24+03:00'
title = 'Методы before() и after() в JavaScript'
categories = [ "javascript" ]
+++

Методы `before()` и `after()` позволяют добавлять новые элементы или текст до или после существующего элемента. В отличие от `append()` и `prepend()`, они работают не внутри, а рядом с целевым элементом.

### element.before() — вставка перед элементом

Метод before() добавляет новый контент перед указанным элементом.

```js
let heading = document.getElementById('title'); 
let newText = document.createElement('p'); 
newText.textContent = 'Тут был Dxrkd3v =)';
heading.before(newText); 
// Теперь <p> появится перед <title>
```

### element.after() — вставка после элемента

Метод `after()` добавляет контент после указанного элемента.

```js
let button = document.getElementById('submitBtn'); 
let note = document.createElement('span'); 
note.textContent = ' (Это важно!)';
button.after(note); // Теперь <span> появится сразу после кнопки
```

Методы `before()` и `after()` помогают добавить элементы перед или после других без сложных манипуляций с родительскими контейнерами. Они делают код чище и проще, особенно при динамической модификации интерфейса.