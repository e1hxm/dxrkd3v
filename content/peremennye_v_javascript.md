+++
date = '2024-10-29T18:53:24+03:00'
title = 'Переменные в JavaScript'
categories = [ "javascript" ]
+++

<p>Лекция с Udemy про переменые в JavaScript</p>
            <p>
              Переменные в JavaScript - это хранилище информации. Визуально их можно представить как
              коробки, которые что то содержат внутри себя.
            </p>
            <p>Чтобы объявить переменную существует сразу 3 способа.</p>
            <p>Две ключевые фразы let и const относятся к современной версии JavaScript.</p>
            <p>
              Так же есть ключевое слово var с помощью которого можно объявить переменную, но он
              относится к устаревшей версии и использовать var не рекомендуется.
            </p>
            <h3>let</h3>
            <p>Первый способ - через ключевое слово let</p>
            <p>
              Для того чтобы объявить переменную, прописываем ключевое слово let, после этого пишем
              имя переменной, дальше ставим знак присваивания "=", и пишем значение этой самой
              переменной.
            </p>
            <p>
              В программировании знак равенства "=" называется знаком присваивания. Нужно помнить об
              этом.
            </p>
            <pre><code>let name = "Dxrkd3v"; 
let    // Ключевое слово, для объявления переменной   
name      // имя переменной
=      // знак присваивания
Dxrkd3v      // значение переменной
;      // завершение блока кода</code></pre>
            <h3>const</h3>
            <p>Второй способ - через ключевое слово const</p>
            <p>
              const - переводится как "константа" и переменная созданная с помощью const не может
              быть перезаписана.
            </p>
            <pre>
<code>const dateOfBirth = 29.06.1999;</code></pre>
            <p>
              Имя переменной может сосотоять из букв, цифр, симфола доллара "$" и нижнего
              подчеркивая. И первый символ имени переменной не может быть цифрой
            </p>
            <p>
              Еще имена переменных не должны повторять зарезервированные слова в самом языке
              JavaScript такие как error, alert, prompt и так далее
            </p>
            <p>
              const используется в таких переменных, значения которых в дальнейшем не меняются.
              Например для хранения имен, даты рождений и так далее.
            </p>
            <p>
              У ключевого слова const есть одна особенность, его значение можно перезаписать если
              создать объект через const
            </p>
            <pre><code>const object {
    age: 25;    
}
object.age = 35;   // перепишем значение age
console.log(object.age);  // ответ получим 35     </code></pre>
            <h3>var</h3>
            <p>
              var - это устаревший формат записи переменных. Переменные записанные через var
              встречаются в старых скриптах.
            </p>
            <p>Переменные записанные через var можно перезаписать как и через let</p>
            <p>
              Проблема var в том что, переменная записанная через var существует еще до того как она
              была объявлена в коде и поэтому она видна везде
            </p>
            <p>
              При обращеннии к переменной которая записана через var еще до того как до нее дойдет
              поток консоль выдаст undefined. Например:
            </p>
            <pre><code>console.log(name);  // выдаст undefined    
var name = "Dxrkd3v"; </code></pre>
            <p>Такое поведение называется "hoisting" или всплытие переменных.</p>
            <p>
              Еще одна особеность let и const в том что они видны в блоке кода ограниченного
              фигурными скобками
            </p>
            <pre><code>{ 
  let result = 29;    
}
console.log(result);   // вернет result is not defined   </code></pre>
            <p>Если записать через var то доступ к переменной "result" будет открыт.</p>
            <p>
              Если нужно узнать какие конструкции можно использовать в разных браузерах нужно
              использовать сервис <a href="https://caniuse.com/">Can I Use</a>
            </p>
            <h3>"use strict"</h3>
            <p>
              Дериктива указывается в начале скрипта и указывает браузеру, что дальнейший код
              работает в "современном" режиме".
            </p>
            <pre><code>"use strict";
// этот код работает в современном режиме   
    ...</code></pre>
            <p>
              Без использования "use strict" можно обращаться к переменным которые были объявлены
              без ключевых слов и получать из них информацию. С "use strict" получаем is not
              defined.
            </p>