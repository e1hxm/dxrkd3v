+++
date = '2024-11-21T18:53:24+03:00'
title = 'Свойство justify-content'
categories = [ "css", "flexbox" ]
+++

<p>
                            Лекция от HTMLAcademy про justify-content
                        </p>
                        <p>
                            В Flexbox есть свойства justify-content,
                            которые позволяют равномерно
                            распределять элементы вдоль главной оси:
                        </p>
                        <ul>
                            <li>
                                'space-between' — это значение,
                                при котором расстояния между
                                соседними элементами равны,
                                а отступы между элементами и
                                краями контейнера отсутствуют.
                            </li>
                            <li>
                                'space-around' — это значение,
                                при котором расстояния между
                                соседними элементами равны,
                                а отступы между элементами и
                                краями контейнера составляют половину
                                расстояния между соседними элементами.
                            </li>
                            <li>
                                'space-evenly' — это значение,
                                при котором расстояния
                                между всеми элементами,
                                включая края контейнера, равны.
                            </li>
                        </ul>
                        <p>
                            Свойство 'justify-content' контролирует
                            распределение элементов вдоль главной оси и
                            принимает пять различных значений:
                        </p>
                        <ul>
                            <li>
                                Значение по умолчанию "flex-start"
                                Располгает элементы в начале оси.
                            </li>
                        </ul>
                            <pre><code>justify-content: flex-start;  </code></pre>
                            <ul>
                                <li>
                                    <p>
                                        "flex-end" распологает
                                        элементы в конце главной оси.
                                    </p>
                                    <p>
                                        Нужно обратить внимание, что
                                        "justify-content: flex-end" не изменяет
                                        порядок элементов,
                                        в отличие от "flex-direction: row-reverse".
                                    </p>
                                </li>
                            </ul>
                            <pre><code>justify-content: flex-end;  </code></pre>
                        </ul>
                        <ul>
                            <li>
                                <p>
                                    "space-between" расстояния между
                                    соседними элементами равны, отступы от
                                    краёв контейнера отсутствуют.
                                </p>
                            </li>
                        </ul>
                        <pre><code>justify-content: space-between;  </code></pre>
                        <ul>
                            <li>
                                <p>
                                    "space-around" расстояния между соседними
                                    элементами равны, отступы от краёв
                                    контейнера равны половине
                                    расстояния между элементами.
                                </p>
                            </li>
                        </ul>
                        <pre><code>justify-content: space-around;  </code></pre>
                        <ul>
                            <li>
                                <p>
                                    "space-evenly" Расстояния между соседними
                                    элементами и краями контейнера равны.
                                </p>
                            </li>
                        </ul>
                        <pre><code>justify-content: space-evenly;  </code></pre>