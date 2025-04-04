+++
date = '2024-12-25T01:29:24+03:00'
title = 'Приминение гибких размеров flexbox'
categories = [ "css", "flexbox" ]
+++
Алгоритм расчёта размеров флекс-элементов и их распределения внутри флекс-контейнера включает три последовательных этапа. Этот процесс значительно сложнее, чем в традиционной блочной модели.

### Шаг второй - Применение гибких размеров

Начнём с примера. Ширина флекс-контейнера составляет 500px. Внутри него находятся три флекс-элемента, каждый из которых имеет исходный базовый размер 100px. Отступы `padding` отсутствуют. Таким образом, во флекс-контейнере остаётся 500px - 300px = 200px свободного места.

![Применение гибких размеров](/images/base_weight_flex2.png)

В стандартной блочной модели эти 200px остались бы неиспользованными, так как размеры элементов определяются за один проход. Во флексбоксе же размеры элементов пересчитываются несколько раз. На втором этапе происходит перераспределение свободного пространства, но только для «гибких» элементов. При этом «гибкость» может быть двух типов: на растяжение и на сжатие.

Свойство `flex-grow` отвечает за гибкость на растяжение, то есть за способность флекс-элемента занимать дополнительное свободное пространство. Оно может принимать числовые значения и по умолчанию равно нулю, что означает, что элементы изначально не претендуют на дополнительное пространство. Если задать `flex-grow` значение больше нуля, флекс-элемент начинает захватывать оставшееся свободное пространство во флекс-контейнере.

![flex grow](/images/flex_grow.png)

Посмотрите на картинку. Внутри флекс-контейнера находятся два флекс-элемента, и осталось свободное пространство. Мы задаём одному из элементов `flex-grow: 1`, и он занимает это свободное пространство. Если же мы зададим обоим элементам `flex-grow: 1`, то они разделят свободное пространство поровну.

![flex grow](/images/flex_grow1.1.png)

Если флекс-элементам задать одинаковые значения `flex-grow`, они поделят свободное пространство поровну. При разных значениях пространство распределяется пропорционально.

Вернёмся к примеру с флекс-контейнером шириной 500px и флекс-элементами с исходным базовым размером 100px. Если задать этим элементам `flex-grow: 1`, они поделят 200px свободного пространства поровну, то есть каждому достанется по 66.6px. В результате базовый размер каждого элемента станет 166.6px. Обратите внимание, что это уже не исходный, а итоговый базовый размер (который в дальнейшем может быть изменён).

![](/images/base_weight_flexbox1.2.png)

`flex-grow` применяется для создания «резиновых» интерфейсов, когда не требуется точное соблюдение пропорций колонок. Если нужно точно контролировать ширину, например, чтобы каждая колонка занимала ровно 30% родителя, используют `width: 30%` или `flex-basis: 30%`, но не `flex-grow`.

Свойство `flex-shrink` отвечает за гибкость на сжатие. Оно может принимать числовые значения и по умолчанию равно единице, что означает, что все флекс-элементы изначально могут сжиматься, если после определения исходных базовых размеров выяснится, что места во флекс-контейнере недостаточно. При этом сжимается только область содержимого, а отступы, паддинги и границы остаются неизменными.

Свойство `flex-shrink` используется редко, так как его применение обычно не требуется. Если в микросетке предполагается большое количество элементов, лучше включить многострочный флекс-контейнер, что сделает `flex-shrink` неактуальным (за исключением редких случаев). При создании сеток рекомендуется отключить возможность сжатия у элементов-колонок.