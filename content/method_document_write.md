+++
date = '2025-01-08T18:55:24+03:00'
title = 'Метод document.write в JavaScript'
categories = [ "javascript" ]
+++

Метод `document.write` – один из наиболее старых методов 
добавления текста на страницу.

Метод `document.write(str)` функционирует исключительно в момент загрузки HTML-страницы. Он добавляет текст в текущее место HTML-документа до того, как браузер завершит формирование DOM-дерева.

После рендера, HTML-документ будет содержать числа **1 2 3**.

```html
<body>
  1
  <script>
    document.write(2);
  </script>
  3
</body>
```

Метод `document.write` не накладывает ограничений на содержимое, которое может быть записано. Он просто добавляет строку в HTML-документ, как если бы она изначально была частью кода, без проверки корректности структуры тегов.

Например:
```html
<script>
  document.write("<p>Этот текст будет добавлен в документ.</p>");
  document.write("<div>Даже если теги не закрыты, например, <span>этот текст</div>");
</script>
```
В этом примере, несмотря на некорректную структуру (тег `<span>` не закрыт), текст будет добавлен в документ без ошибок. Однако это может привести к проблемам с отображением или работой страницы.