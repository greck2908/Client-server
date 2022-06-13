# Client-server

Client_Server

1) Прочиать про клиент-серверную архитектуру
	
	Вычислительная или сетевая архитектура, в которой задания или сетевая нагрузка распределены между поставщиками услуг, называемымисерверами, и заказчиками услуг, называемыми клиентами. Фактически это программное обеспечение.
	
2) Что ткое HTTP и HTTPS
	
	HTTP -протокол передачи данных между браузером и сервером, HTTPS - это тот же HTTP, но с добавленными методами шифрованияданных и проверки безопасности.
	
3) HTTP методы
	
	GET - запрашивает представление ресурса, можно только извлекать данные
	HEAD - запрашивает ресурс так же, как и метод GET, но без тела ответа
	POST - используется для отправки сущностей к определенному ресурсу
	PUT - заменяет все текущие представления ресурса данными запроса
	DELETE - удаляет указанный ресурс
	CONNECT - устанавливает "туннель" к серверу, определенному по ресурсу
	OPTIONS - используется для описания параметров соединения с ресурсом
	TRACE - выполняет вызов возвращаемого тестового сообщения ресурса
	PATCH - используется для частичного изменения ресурса
	
4) HTTP статус коды сервера
	
	1хх - информационные
	2хх - успешные
	3хх - перенаправление
	4хх - ошибка клиента
	5хх - ошибка сервера
	
5) Что такое ядро браузера 
	
	Ядро браузера можно разделить на две части: движок рендеринга (инженер макета или движок рендеринга) и движок JS. Он отвечает за получение содержимого веб-страницы (HTML, XML, изображения и т. Д.), Организацию информации (например, добавление CSS и т. Д.) И расчет режима отображения веб-страницы, а затем вывод ее на монитор или принтер. Разница в ядре браузера будет по-разному интерпретировать синтаксис веб-страницы, поэтому эффект рендеринга будет другим. Все веб-браузеры, почтовые клиенты и другие приложения, которым необходимо редактировать и отображать сетевой контент, требуют ядра. (См. Википедия). Движок JS анализирует язык Javascript и выполняет язык Javascript для достижения динамических эффектов веб-страницы. Сначала не было четкого различия между движком рендеринга и движком JS, а позже движок JS становился все более независимым, и ядро ​​имело тенденцию ссылаться только на движок рендеринга. Механизм рендеринга определяет, как браузер отображает содержимое веб-страницы и информацию о формате страницы. Разные ядра браузеров по-разному интерпретируют синтаксис записи веб-страниц, поэтому эффект рендеринга (отображения) одной и той же веб-страницы в браузерах разных ядер также может быть различным. Именно поэтому авторам веб-страниц необходимо тестировать веб-страницы в браузерах разных ядер. Покажите причину эффекта. Движок JS отвечает за интерпретацию, компиляцию и выполнение JavaScript, чтобы заставить веб-страницу достигать некоторых динамических эффектов. Но обычные ядра браузера можно разделить на эти пять типов: Trident, Gecko, Presto, Webkit, Blink.
	
6) Какие браузеры какиие ядра используют
	
	Trident (ядро IE)
	Gecko (ядро Firefox)
	Presto (pre-Opera kernel) (устарело)
	Webkit (ядро Safari, прототип ядра Chrome, открытый исходный код)
	Blink - это механизм верстки браузера, разработанный Google и Opera Software. Google планирует использовать этот механизм рендеринга в рамках проекта Chromium, и анонсировал эту новость в апреле 2013 года. , Этот движок рендеринга является ветвью компонента WebCore движка с открытым исходным кодом WebKit и используется в браузерах Chrome (28 и более поздние версии), Opera (15 и более поздние версии) и Яндекса.
		
7) Что такое API
	
	API (Application Programming Interface или интерфейс программирования приложений) — это совокупность инструментов и функций в виде интерфейса для создания новых приложений, благодаря которому одна программа будет взаимодействовать с другой.
	
8. Что такое ендпоинты
	
	Эндпоинт (Endpoint - конечная точка) — это само обращение к маршруту отдельным HTTP методом. Эндпоинт выполняют конкретную задачу, принимают параметры и возвращают данные Клиенту.
	
9) URL (URI, URL, URN)
	
	URL — Унифицированный указатель ресурса — система унифицированных адресов электронных ресурсов, или единообразный определитель местонахождения ресурса (файла).
	URI — символьная строка, позволяющая идентифицировать какой-либо ресурс
	URN — это постоянная последовательность символов, идентифицирующая абстрактный или физический ресурс
	
10) Идемпотентные HTTP методы
	
	Метод HTTP является идемпотентным, если повторный идентичный запрос, сделанный один или несколько раз подряд, имеет один и тот же эффект, не изменяющий состояние сервера. Другими словами, идемпотентный метод не должен иметь никаких побочных эффектов (side-effects), кроме сбора статистики или подобных операций.
	При использование таких методов побочные эффекты одинаковы как в случае однократного запроса, так и в случае многократного повторения одного и того же запроса, т.е. нагрузка одинакова, но HTTP ответ от сервера может поступать каждый раз разный. К идемпотентным методам относятся следующие HTTP методы: GET, HEAD, PUT и DELETE. Так же эффектом идемпотентности обладают HTTP методы OPTIONS и TRACE.
	
11) Безопасные HTTP методы
	
	На данный момент принято соглашение о том, что HTTP методы GET и HEAD никогда не должны иметь иного значения, кроме загрузки, поэтому данные HTTP методы нужно рассматривать, как безопасные, это требование HTTP. Поэтому ваш браузер, когда используются методы POST, PUT или DELETE предупреждает вас о том, что может произойти потенциально опасное действие и спрашивает: нужно ли его выполнить.
	
12) Иденфикация, Аутентификация, Авторизация
	
	Идентификация - это установление тождественности чего-либо неизвестного известному, на основании совпадения признаков или иных методов. 
	Аутентификация – это процесс обмена учетными данными для идентификации пользователя.
	Авторизация — предоставление определённому лицу или группе лиц прав на выполнение определённых действий; а также процесс проверки (подтверждения) данных прав при попытке выполнения этих действий.
	
13) Что такое IP
	
	IP-адрес – это уникальный адрес, идентифицирующий устройство в интернете или локальной сети.
	
14) Что такое октаты в DNS
	
	В компьютерных и сетевых технологиях октет представляет собой 8-битное количество. Математическое значение октетов колеблется от 0 до 255.
	Все современные компьютерные системы реализуют байт как восьмибитную величину. Октеты и байты одинаковы с этой точки зрения. По этой причине оба термина используются взаимозаменяемо. 
	Термин строка октетов относится к набору любого количества связанных октетов. Строки октетов обычно встречаются при адресации по интернет-протоколу (IP), в которой четыре байта адреса IPv4 состоят из четырех октетов. В десятичном формате с точками IP-адрес отображается как [октет]. [Октет]. [Октет]. [Октет] , как в 192.168.0.1 . 
	
15) Что такое порт, сколько портов у Linux сервера
	
	Порт — целое неотрицательное число, записываемое в заголовках протоколов транспортного уровня сетевой модели OSI (TCP, UDP, SCTP, DCCP).
	Количество портов ограничено с учётом 16-битной адресации (216=65536, начало — «0»). Все порты разделены на три диапазона — общеизвестные (или системные, 0—1023), зарегистрированные (или пользовательские, 1024—49151) и динамические (или частные, 49152—65535).
	
16) Уровни OSI
	
	7. Прикладной уровень (application layer)
	6. Уровень представления (presentation layer)
	5. Сеансовый уровень (session layer)
	4. Транспортный уровень (transport layer)
	3. Сетевой уровень (network layer)
	2. Канальный уровень (data link layer)
	1. Физический уровень (physical layer)
	
17) Хедеры http запросов
	
	Заголовки HTTP позволяют клиенту и серверу отправлять дополнительную информацию с HTTP запросом или ответом. 
	Заголовки могут быть сгруппированы по следующим контекстам:

    Основные заголовки - применяется как к запросам, так и к ответам, но не имеет отношения к данным, передаваемым в теле.
    Заголовки запроса - содержит больше информации о ресурсе, который нужно получить, или о клиенте, запрашивающем ресурс.
    Заголовки ответа - содержат дополнительную информацию об ответе, например его местонахождение, или о сервере, предоставившем его.
    Заголовки сущности - содержат информацию о теле ресурса, например его длину содержимого или тип MIME.

	
