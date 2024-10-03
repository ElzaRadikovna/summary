# План автоматизации тестирования

1. **Перечень автоматизируемых сценариев.**

**Навигация**

|**1**|<p>1. Открыть  [Веб-сайт Нетологии](https://netology.ru/)</p><p>2. Найти сверху вкладку “Каталог курсов” ,кликнуть по ней</p><p>3. Выбрать “Программирование”, перейти по ссылке</p><p>4. Из предложенного списка курсов найти “Инженер по тестированию”, кликнуть</p><p>5. Кликнуть кнопку “Записаться”</p>|
| :- | :- |
|**2**|<p>1. Открыть  [Веб-сайт Нетологии](https://netology.ru/)</p><p>2. Пролистать страницу до “Направления обучения”</p><p>3. Кликнуть на “Программирование”</p><p>4. Из предложенного списка курсов найти “Инженер по тестированию”, кликнуть</p><p>5. Кликнуть кнопку “Записаться”</p>|
|**3**|<p>1. Открыть  [Веб-сайт Нетологии](https://netology.ru/)</p><p>2. Найти сверху вкладку “Каталог курсов” ,кликнуть по ней</p><p>3. Выбрать “Программирование”, перейти по ссылке</p><p>4. В строке поиска написать “Инженер по тестированию”, кликнуть </p><p>5. Кликнуть кнопку “Записаться” </p>|
|**4**|<p>1. Открыть  [Веб-сайт Нетологии](https://netology.ru/)</p><p>2. Найти сверху вкладку “Каталог курсов” ,кликнуть по ней</p><p>3. В строке поиска написать “Инженер по тестированию”</p><p>4. В всплывающем окне кликнуть на “Инженер по тестированию”</p><p>5. Кликнуть кнопку “Записаться” </p>|



### Заполнение формы

**Валидные значения:**

*Поле **“Имя”** -*  русскими буквами,допускается двойное имя через дефис/пробел, например “*Дарья”, “Анна-Мария”, “Ева Оливия”*

*Поле **“Телефон”** -*  начинается с +7, общее количество цифр -11, например “+79002223311”



||**Название**|**Шаги реализации**|**Ожидаемый результат**|
| :- | :- | :- | :- |
|**1**|**Успешная отправка формы**|<p>1. Заполнить поля “Имя” и “Телефон” валидными данными</p><p>2. Кликнуть кнопку “Записаться”</p>|Форма успешно отправлена|
||**Отправка формы с невалидными данными в поле “Имя”**|||
|**2**|**Отправка пустого поля**|<p>1. Оставить поле “Имя” пустым</p><p>2. Заполнить поле “Телефон” валидными данными</p><p>3. Кликнуть кнопку “Записаться”</p>|Поле “Имя” подсвечивается красным, выходит сообщение о необходимости заполнить все поля|
|**3**|**Ввод данных на латинице**|<p>1. Заполнить поле “Имя” на латинице, например “Arina”</p><p>2. Заполнить поле “Телефон” валидными данными</p><p>3. Кликнуть кнопку “Записаться”</p>|Поле “Имя” подсвечивается красным, выходит сообщение “Поле “Имя” должно быть заполнено русскими буквами”|
|**4**|**Ввод недопустимых символов**|<p>1. Заполнить поле “Имя” с символами, например “\*Анна?%;”</p><p>2. Заполнить поле “Телефон” валидными данными</p><p>3. Кликнуть кнопку “Записаться”</p>|Поле “Имя” подсвечивается красным, выходит сообщение “Поле “Имя” должно быть заполнено без символов”|
|**5**|**Ввод цифр в поле “Имя”**|<p>1. Заполнить поле “Имя” цифрами, например “10234”</p><p>2. Заполнить поле “Телефон” валидными данными</p><p>3. Кликнуть кнопку “Записаться”</p>|Поле “Имя” подсвечивается красным, выходит сообщение “Поле “Имя” не должно содержать цифры”|
||**Отправка формы с невалидными данными в поле “Телефон”**|||
|**6**|**Отправка пустого поля**|<p>1. Заполнить поле “Имя” валидными данными</p><p>2. Оставить поле “Телефон” пустым</p><p>3. Кликнуть кнопку “Записаться”</p>|Поле “Телефон” подсвечивается красным, выходит сообщение о необходимости заполнить все поля|
|**7**|**Ввод букв в поле “Телефон”**|<p>1. Заполнить поле “Имя” валидными данными</p><p>2. Ввести в поле “Телефон” буквы, например “привет”</p><p>3. Кликнуть кнопку “Записаться”</p>|Поле “Телефон” подсвечивается красным, выходит сообщение “Поле “Телефон” должно содержать только цифры”|
|**8**|**Ввод недостаточного количества цифр**|<p>1. Заполнить поле “Имя” валидными данными</p><p>2. Ввести в поле “Телефон” 8 цифр, например “+7905625”</p><p>3. Кликнуть кнопку “Записаться”</p>|Поле “Телефон” подсвечивается красным, выходит сообщение “Поле “Телефон” должно содержать 11 цифр”|
|**9**|**Ввод цифр, превышающие количество допустимого**|<p>1. Заполнить поле “Имя” валидными данными</p><p>2. Ввести в поле “Телефон” 12 цифр, например “+790562565651”</p><p>3. Кликнуть кнопку “Записаться”</p>|Поле “Телефон” подсвечивается красным, выходит сообщение “Поле “Телефон” должно содержать 11 цифр”|

**2. Перечень используемых инструментов с обоснованием выбора.**

|**Gradle**|Он считается более гибким, так как не использует xml, поэтому многие конструкции в нем выглядят короче, еще и имеют сокращения. Gradle сам следит за тем, чтобы запускать нужные задачи в нужном порядке, плюс запускать только те задачи для которых что-то изменилось. Если не менялись исходные коды проекта, только автотесты, то не нужно перекомпилировать весь проект.|
| :- | :- |
|**Selenide**|Сам скачивает драйвер, использует SelenideElement, включает матчеры для проверок.|
|**Faker**|Для генерации данных при отправке формы|
|**Allure**|Создание визуально наглядной картины выполнения тестов|

**3. Перечень необходимых разрешений, данных и доступов.**

- Доступ к данным и тестам
- К тестовому сервису
- Учетные записи
- Доступ к базе данных, API
- Разрешение на автотестирование

**4.Перечень и описание возможных рисков при автоматизации.**

- Изменения в структуре сайта
- Трудности при поиске элементов
- Сбой в системе

**5.Перечень необходимых специалистов для автоматизации.**

Инженер по автоматизированному тестированию

**6.Интервальная оценка с учётом рисков в часах.**

70 часов


  

  

    
