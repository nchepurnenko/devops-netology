**Задача 1**  

* Электронные чеки в json виде - NOSQL документо-ориентированная БД
* Склады и автомобильные дороги для логистической компании - возможно графовая БД? Но я о них ничего не понял =) Реляционная в любом случае подойдет 
* Генеалогические деревья - сетевая БД, т.к. родителей обычно больше одного
* Кэш идентификаторов клиентов с ограниченным временем жизни для движка аутенфикации - key-value БД
* Отношения клиент-покупка для интернет-магазина - в самом простом случае подойдет key-value БД, но если нужны хранить данные о клиентах и товарах, то лучше использовать реляционную БД  

**Задача 2**  

Описание | CAP | PACELC
---------|-----|-------
Данные записываются на все узлы с задержкой до часа (асинхронная запись) | AP | PA/EL
При сетевых сбоях, система может разделиться на 2 раздельных кластера | AP | PA/EL
Система может не прислать корректный ответ или сбросить соединение | CP | PC/EC

**Задача 3**  

Мне кажется это взаимоисключающие принципы и совместить их в одной системе не получится. ACID больше сконцентрирован на консистентности данных, а BASE на доступности.

**Задача 4**  

Это система "Издатель-подписчик", в которой одни сервисы выступают как "издатели", т.е. создают и публикуют сообщения в системе, а другие как "подписчики" - получают и обрабатывают эти сообщения. Отличительной особенностью является то, что "издатели" и "подписчики" не знают друг о друге, а связаны только через эту систему.
Минусов что-то я не придумал.
