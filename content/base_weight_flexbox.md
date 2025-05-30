+++
date = '2024-12-24T06:29:24+03:00'
title = 'Исходные базовые размеры flex-элементов'
categories = [ "css", "flexbox" ]
+++
Алгоритм расчёта размеров флекс-элементов и их распределения внутри флекс-контейнера включает три последовательных этапа. Этот процесс значительно сложнее, чем в традиционной блочной модели.

### Первый шаг - Определение исходных базовых размеров флекс-элементов

Базовый размер — это размер элемента, измеряемый вдоль основной оси.

Исходный базовый размер — это размер, который флекс-элемент принимает без использования дополнительных функций флекс-модели. Он определяется стандартными свойствами блочной модели (например, `width`, `height`, `padding`, `border`) и содержимым элемента.

Если основная ось расположена горизонтально, то на исходный базовый размер влияют:

- свойство `width` или, если оно не задано, ширина содержимого (например, длина самого длинного слова)

- горизонтальные отступы `padding`

- горизонтальные границы `border`

Если основная ось направлена вертикально, то на исходный базовый размер влияют:

- свойство `height` или, если оно не задано, высота содержимого например, количество текстовых строк

- вертикальные отступы `padding`

- вертикальные границы `border`

С отступами и границами всё достаточно логично: в зависимости от направления основной оси в исходном размере учитываются либо вертикальные, либо горизонтальные компоненты отступов или границ.

Что касается ширины и высоты содержимого, то есть свойств `width` или `height`, ситуация оказалась не столь однозначной. Основная ось направлена горизонтально — используем одно свойство, повернули ось вертикально — применяем другое. В связи с этим было введено дополнительное свойство — `flex-basis`.

Оно определяет размер области содержимого вдоль основной оси, независимо от её направления. Свойство `flex-basis` имеет приоритет над `width` и `height`, переопределяя их, если они заданы одновременно на одном флекс-элементе. 

Можно использовать `width`/`height` без применения `flex-basis`, и наоборот — это также допустимо. Важно помнить о поведении этих свойств и направлении основной оси.

![Определение исходных базовых размеров флекс-элементов](/images/base_weight.png)

Исходный базовый размер флекс-элемента определяется следующим образом:

Шаг первый:
- Если задано свойство `flex-basis` (и его значение отличается от `auto`), то в качестве размера области содержимого используется значение `flex-basis`, и далее переходим к шагу 5. В противном случае переходим к шагу 2.

Шаг второй:
- Если основная ось направлена горизонтально и задано свойство `width` (его значение отличается от `auto`), то в качестве размера области содержимого используется значение `width`, и далее переходим к шагу 5. В противном случае переходим к шагу 3.

Шаг третий:
- Если основная ось направлена вертикально и задано свойство `height` (его значение отличается от `auto`), то в качестве размера области содержимого используется значение `height`, и далее переходим к шагу 5. В противном случае переходим к шагу 4.

Шаг четвертый:
- Размер области содержимого определяется исходя из размера самого содержимого флекс-элемента вдоль соответствующей оси. Этот процесс может быть нетривиальным, поэтому при создании сеток лучше избегать таких ситуаций, чтобы сохранить контроль над размерами элементов. Переходим к шагу 5.

Шаг пятый:
- К размеру области содержимого добавляем отступы и границы вдоль соответствующего направления основной оси, чтобы получить исходный базовый размер.

Важное правило: при создании сеток всегда следует задавать либо `flex-basis`, либо `width`/`height`.

После определения исходного базового размера всех флекс-элементов браузер вычисляет, сколько свободного места остаётся во флекс-контейнере. Если есть свободное место или, наоборот, его недостаточно, начинает работать «гибкость» флекс-элементов. Это уже второй этап.