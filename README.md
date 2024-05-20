# OTUS_SA_Basic :sunglasses:
## :bowtie: Регистрация клиента и автомобиля, осмотр, составление плана ремонта формирование заказ наряда, приемка авто :bowtie:
- [Бизнес требования](#busines)
- [Определение предметной области](#predmet)
- [Определение требований](#treb)
- [Пользовательские истории](#us)
- [Информационная модель приложения](#imodel)
- [Проектирование структуры приложения](#proekt)
- [Примеры прототипов интерфейсов](#prototype)
- [Взаимодействие со сторонними API](#api)
- [Acceptance Criteria для MVP](#ac)
- [Тест кейсы для задач MVP](#testc)
- [Задачи для разработки](#dev)

<a name="busines"><h2>Бизнес требования к приложению</h2></a>
### Бизнес требования:
1) **Эффективность работы:**
- Уменьшение времени, затрачиваемого на выполнение заказов.
- Повышение производительности персонала и оборудования.
- Сокращение времени ожидания клиентов и сроков выполнения заказов.
2) **Качество обслуживания:**
- Сокращение числа ошибок и брака в процессе ремонта.
- Обеспечение точности диагностики и ремонта автомобилей.
- Улучшение уровня обслуживания клиентов и удовлетворенности их потребностей.
3) **Экономическая эффективность:**
- Снижение издержек на складирование запасных частей и материалов.
- Оптимизация использования ресурсов и сокращение излишних затрат.
- Увеличение доходов за счет увеличения объема обслуживаемых заказов.
4) **Прозрачность и контроль:**
- Обеспечение возможности отслеживания статуса заказов и работы сотрудников.
- Возможность мониторинга запасов и расходов материалов.
- Предоставление администрации автомастерской подробной отчетности и аналитики о работе предприятия.
5) **Адаптивность и масштабируемость:**
- Гибкость системы для внесения изменений в процессы работы и требований клиентов.
- Возможность масштабирования системы при расширении бизнеса или увеличении объема заказов.
- Совместимость системы с другими программными и аппаратными средствами для интеграции существующих технологий и развития новых.
6) **Безопасность и конфиденциальность:**
- Обеспечение защиты конфиденциальных данных клиентов и информации о заказах.
- Предотвращение несанкционированного доступа к системе и возможных угроз безопасности данных.
- **Удобство использования:**
- Простота в освоении и использовании системы для сотрудников мастерской.
- Предоставление интуитивно понятного интерфейса для управления заказами, расписанием и другими функциями.
7) **Устойчивость и надежность:**
- Обеспечение стабильной работы системы без сбоев и простоев.
- Гарантирование сохранности данных и возможность быстрого восстановления после сбоев или аварийных ситуаций.
### Критерии успеха
-
-
-
-
### Процессы которые требуют автоматизации:
1) **Регистрация клиента и автомобиля:**
- Система должна позволять регистрировать новых клиентов и их автомобили.
- Должна быть возможность ввода основной информации о клиенте (ФИО, контактная информация) и автомобиле (марка, модель, год выпуска, VIN-номер).
- Предусмотреть функционал для обновления информации о клиентах и их автомобилях.
2) **Осмотр автомобиля:**
- Система должна поддерживать функционал осмотра автомобиля специалистом (мастером) для определения неисправностей и составления плана ремонта.
- Должна быть возможность ввода результатов осмотра (виды неисправностей, их описание, предварительная оценка стоимости ремонта).
3) **Составление плана ремонта:**
- Система должна автоматически генерировать план ремонта на основе результатов осмотра автомобиля.
- В плане ремонта должны быть указаны виды работ, запчасти и материалы, необходимые для исправления выявленных неисправностей.
- Предусмотреть возможность редактирования плана ремонта для учета дополнительных требований клиента или изменений в ходе ремонта.
4) **Формирование заказ-наряда:**
- Система должна позволять формировать заказ-наряд на основе утвержденного плана ремонта.
- В заказ-наряде должны быть указаны все необходимые работы, запчасти и материалы, а также предварительная оценка стоимости и сроки выполнения ремонта.
5) **Приемка автомобиля:**
- Система должна предоставлять возможность проведения приемки автомобиля после выполнения ремонта.
- Должна быть возможность внесения результатов приемки (подтверждение выполнения работ, оценка качества ремонта).
- Предусмотреть функционал для подписания заказ-наряда клиентом и закрытия заказа после приемки.
- **Эти требования должны обеспечить эффективный и прозрачный процесс обслуживания автомобилей и удовлетворить потребности как клиентов, так и работников автосервиса. В целом, автоматизация данных процессов не только повышает эффективность и качество обслуживания клиентов, но и оптимизирует внутренние операции автосервиса, делая его более конкурентоспособным на рынке.**




<a name="predmet"><h2>Определение предметной области</h2></a>

### Предметная область для автомастерской включает в себя широкий спектр услуг, связанных с обслуживанием и ремонтом автомобилей. В эту область входят следующие основные элементы:
1) **Обслуживание и ремонт автомобилей:**
- Диагностика неисправностей и техническое обслуживание автомобилей.
- Плановые и внеплановые ремонтные работы, включая замену запчастей и компонентов.
- Регулировка и обслуживание различных систем автомобиля, таких как двигатель, трансмиссия, подвеска, тормозная система и электроника.
2) **Запасные части и материалы:**
- Приобретение, хранение и управление запасными частями и материалами для ремонта автомобилей.
- Отслеживание инвентаря, учет расходных материалов и поддержание оптимального уровня запасов.
- Управление заказами и клиентским сервисом:
- Принятие заказов на обслуживание и ремонт автомобилей от клиентов.
- Планирование и распределение рабочих мест для выполнения заказов с учетом срочности и приоритетности.
- Взаимодействие с клиентами, предоставление информации о статусе заказов, консультации по необходимым ремонтным работам и ценам.
3) **Финансовое управление:**
- Учет финансовых операций, включая выставление счетов, оплату услуг и закупку материалов.
- Анализ прибыльности и затрат на ремонтные работы, управление бюджетом и финансовым планированием.
4) **Технологические инструменты и оборудование:**
- Использование специализированных технических инструментов и оборудования для диагностики и ремонта автомобилей.
- Обеспечение обновления и поддержки технологического оборудования для эффективного выполнения работ.
5) **Законодательные требования и стандарты:**
- Соблюдение правовых норм, стандартов безопасности и требований по охране окружающей среды в процессе обслуживания и ремонта автомобилей.
- Лицензирование и сертификация персонала и предприятия в соответствии с законодательством.
6) **Управление персоналом:**
- Найм, обучение и мотивация персонала, включая механиков, автомехаников и административный персонал.
- Распределение обязанностей, планирование графиков работы и контроль производительности сотрудников.



<a name="treb"><h2>Определение требований к системе</h2></a>
#### Нефункциональные требования:
<table><tr><th valign="top"><i>№</i></th><th valign="top"><i>Тема</i></th><th valign="top"><i>Требование</i></th><th valign="top"><i>Тип</i></th><th valign="top"><i>Комментарий</i></th></tr>
<tr><td rowspan="3" valign="top"></td><td rowspan="3" valign="top"><i>Технологический стек</i></td><td valign="top"><i>Разработка backend на Python,</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"><i>Разработка front-end NODE, NEXT/React</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"><i>Связь между клиентом и сервером WireGuard</i> </td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td rowspan="4" valign="top"></td><td rowspan="4" valign="top"><i>Безопасность</i></td><td valign="top"><i>Клиент должен взаимодействовать с сервером посредством протокола SSL</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"><i>Требуется двухфакторная аутентификация</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"><i>Отслеживание активности пользователя, при бездействии закрывать сессию с сохранением данных.</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"><i>Требуется шифровать межсервисный трафик</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"></td><td rowspan="2" valign="top"><i>Совместимость</i></td><td valign="top"><p><i>Веб  приложение должно поддерживать как мобильную версию для смартфонов, так и версию браузеров на ПК (Safari, Google Chrome, Яндекс Браузер, Mozila Firefox, Microsoft Edge, IE 11)</i></p><p></p></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"></td><td valign="top"><p><i>Приложение должно обеспечивать передачу данных с использованием шифрования</i></p><p></p></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"></td><td rowspan="2" valign="top"><i>Масштабируемость</i></td><td valign="top"><i>Решение должно поддерживать ежегодный рост на 30% новых терминалов</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"></td><td valign="top"><p><i>Решение должно поддерживать ежегодный рост на 25% от предыдущего количества транзакций.</i></p><p></p></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"></td><td valign="top"><i>Поддерживаемость:</i></td><td valign="top"><i>Обязательное логирование поведения приложения, авторизация пользователей, контроль учётных записей.</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"></td><td valign="top"><i>Требования к модульности приложения:</i></td><td valign="top"><i>Инфраструктура поддерживающая сервис должна состоять из следующих модулей: БД, сервер приложений, клиентский веб интерфейс.</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td rowspan="5" valign="top"></td><td rowspan="5" valign="top"><i>Производительность:</i></td><td valign="top"><i>Резервное копирование базы (инкрементное) каждые 5 минут без потери производительности базы</i></td><td rowspan="5" valign="top"><i>Нефункциональное</i></td><td rowspan="5" valign="top"></td></tr>
<tr><td valign="top"><i>Среднее время загрузки главной страницы сайта не должно превышать 3 секунды при использовании стандартного интернет-соединения.</i></td></tr>
<tr><td valign="top"><i>Сайт должен обеспечивать достаточную пропускную способность для поддержания стабильной работы при одновременном обслуживании 30 пользователей</i></td></tr>
<tr><td valign="top"><i>Время отклика интерфейса должно быть менее 0.5 секунды для основных действий пользователя, таких как переход по ссылкам или отправка форм.</i></td></tr>
<tr><td valign="top"><i>Пиковое значение 200 активных пользователей одновременно</i></td></tr>
<tr><td valign="top"></td><td rowspan="2" valign="top"><i>Доступность:</i></td><td valign="top"><p><i>Сервис должен быть доступен 95% времени с территории РФ.</i></p><p></p></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
<tr><td valign="top"></td><td valign="top"><i>Режим работы 24/7</i></td><td valign="top"><i>Нефункциональное</i></td><td valign="top"></td></tr>
</table>


#### Формализация бизнес требований:
![image1](https://github.com/AlexSterlev/OTUS_SA_Basic/blob/main/needs.png)

<a name="us"><h2>Пользовательские истории</h2></a>

|US001|Я как менеджер хочу видеть список свободных мастеров для их назначения на работы|must|Менеджер|mvp|На сайте сервиса отображается список свободных мастеров|
| :- | :- | :- | :- | :- | :- |
|US002|Я как менеджер хочу иметь доступ к заказ-наряду что бы согласовать список з\ч|must|Менеджер|mvp|После входа в систему менеджер должен видеть список запчастей, включенных в заказ-наряд, вместе с их описанием и количеством.|
|US003|Я как мастер-диагност хочу получить машину для выполнения диагностики|must|Мастер|mvp|Мастер-диагност должен иметь возможность получить доступ к машине, которую необходимо диагностировать.|
|US004|Я как менеджер хочу передать ТС мастеру для проведения диагностики|must|Менеджер|mvp|<p>Менеджер может выбрать техническое средство (ТС) для передачи, указать мастера, которому будет передано ТС.</p><p>Система должна уведомить мастера о передаче ТС для проведения диагностики.</p>|
|US005|Я как мастер-диагност хочу провести диагностику для дальнейшего согласования с клиентом|should|Мастер||В системе присутствует форма, результаты диагностик которая заполняется мастером|
|US006|Я как мастер-дианост хочу видеть предварительное описание проблемы со слов заказчика.|must|Мастер|mvp|При приёмке мастером машины на диагностику в системе есть графа. Описание проблемы. Её заполняет менеджер при приёме ТС.|
|US007|Я как мастер хочу иметь доступ к диагностической карте ТС что бы знать историю ремонта|must|Менеджер|mvp|После входа в систему  мастер-диагност видит информацию о машине, включая ее марку, модель, год выпуска и предыдущие работы, если таковые имели место.|
|US008|Я как менеджер хочу проверить наличие запчастей для согласования сроков выполнения заказ-наряда|must|Менеджер|mvp|<p>Менеджер может увидеть в системе список запчастей, необходимых для выполнения заказ-наряда.</p><p></p><p></p>|
|US009|Я как менеджер хочу иметь доступ к заказ-наряду для предварительного подсчёта стоимости ремонта|must|Менеджер|mvp|Менеджер может получить доступ к заказ-наряду для предварительного ознакомления с работами, которые требуется выполнить.|
|US010|Я как мастер хочу видеть какие ТС назначены мне для проведения работ для эффективно планирования рабочего времени|must|Мастер|mvp|Мастер может видеть список технических средств (ТС), которые назначены ему для проведения работ (тип работ, сроки выполнения и дополнительные требования).|
|US011|Я как мастер хочу иметь доступ к заказ-наряду что бы планировать перечень работ|must|Мастер|mvp|Мастер имеет доступ к заказ-наряду, содержащему перечень работ, которые требуется выполнить.|
|US012|Я как менеджер хочу прикрепить диагностический лист к заказ-наряду для контроля выполняемых работ|should|Менеджер||При формировании заказ-наряда есть кнопка прикрепить диагностический лист|
|US013|Я как менеджер хочу иметь доступ к каталогу запчастей для корректного составления заказ-наряда|must|Менеджер|mvp|Менеджер может получить доступ к каталогу запчастей, содержащему полный список доступных запчастей.|
|US014|Я как мастер хочу иметь возможность вносить изменения в заказ наряд в случае отсутствия необходимых запчастей|must|Менеджер|mvp|При внесении изменений в заказ-наряд мастер может корректировать стоимость работ и сроки выполнения.|
|US015|Я как менеджер хочу иметь форму заказа запчастей для составления заявки на склад|should|Менеджер||<p>Менеджер имеет доступ к форме заказа запчастей через соответствующий интерфейс</p><p></p><p></p>|
|US016|Я как менеджер хочу иметь возможность отслеживать статус заявки на склад для более эффективного планирования работ|should|Менеджер||Менеджер имеет доступ к информации о текущем статусе заявки на складе через соответствующий интерфейс|
|US017|Я как менеджер хочу иметь возможность автоматизированного заказ на наиболее популярные виды расходников что бы не тратить время на создание заявки|should|Менеджер||Менеджер имеет возможность использовать функцию автоматического заполнения заявки, которая автоматически добавляет наиболее популярные виды расходников в заказ без необходимости ручного ввода.|
|US018|Я как менеджер хочу иметь возможность объединять мелкие заказы в один крупный, что бы экономить время на приёмке |should|Менеджер||Менеджер может выбирать заказы из списка доступных заказов и добавлять их к объединяемому заказу.|
|US019|Я как мастер хочу иметь возможность сформировать заказ на запчасти для выполнения работ|must|Мастер|mvp|В форме заказа мастер может выбирать необходимые запчасти из каталога или предложенного списка.|
|US020|Я как мастер хочу иметь возможность отмечать выполненные работы для обновления информации по ремонту ТС|must|Мастер|mvp|Мастер имеет доступ к списку работ через соответствующий интерфейс, отмечает выполненные работы в списке, указав статус "Выполнено" или подобное обозначение.|
|US021|Я как менеджер хочу видеть каждый этап ремонта ТС для контроля работ|should|Менеджер||Менеджер имеет доступ к информации о текущем этапе ремонта каждого ТС через соответствующий интерфейс. Для каждого ТС предоставляется подробное описание текущего этапа ремонта, включая название этапа, описание и предполагаемые сроки завершения.|
|US022|Я как менеджер хочу что бы мастер вносил все изменения в заказ-наряд для более точного расчёта стоимости|should|Менеджер||Интерфейс предоставляет возможность вносить изменения в различные аспекты заказа-наряда, такие как количество материалов, часы работы и т.д.|


<a name="imodel"><h2>Информационная модель приложения</h2></a>
#### Проектирование диаграммы классов
![image2](https://github.com/AlexSterlev/OTUS_SA_Basic/blob/main/ClassDiag.jpg)
#### Основные сущности в системе управления проигрыванием видеоконтента включают:

#### На основе этих сущностей, мы можем спроектировать следующую диаграмму классов:

#### Алгоритм приёмки ТС в ремонт:
![image4](https://github.com/AlexSterlev/OTUS_SA_Basic/blob/main/BPMN.jpg)

#### Алгоритм технического обслуживания ТС:
![image3](https://github.com/AlexSterlev/OTUS_SA_Basic/blob/main/Activity.png)

<a name="ac"><h2>Acceptance Criteria для MVP</h2></a>

<details>
	<summary><h4>US001 Я как менеджер хочу видеть список свободных мастеров для их назначения на работы</h4></summary>
 
* Пользователь (менеджер) должен иметь возможность войти в систему с использованием своих учетных данных.
* После входа в систему, менеджер должен иметь доступ к разделу "Список свободных мастеров" или аналогичному разделу, где перечислены все мастера, доступные для назначения на работы.
* Для каждого мастера в списке должны быть указаны следующие данные: ФИО, специализация, текущая загрузка работы (например, количество назначенных работ за определенный период времени).
* Список мастеров должен быть актуальным и обновляться в реальном времени, отражая текущую доступность каждого мастера.
* Менеджер должен иметь возможность фильтровать список мастеров по различным критериям, таким как специализация, доступность на конкретные даты и т. д.
* После выбора мастера, менеджер должен иметь возможность назначить его на конкретную работу или задание.
* После назначения мастера на работу, его статус должен измениться на "занят" или аналогичный, чтобы избежать дублирования назначений.
* Система должна сохранять и отображать историю назначений для каждого мастера, чтобы можно было отследить его загрузку и производительность.

</details>

<details>

<summary><h4>US002 Я как менеджер хочу видеть список свободных мастеров для их назначения на работы.</h4></summary>
	
- Пользователь (менеджер) должен иметь возможность войти в систему с использованием учетных данных.
- После входа в систему, менеджер должен видеть список доступных заказ-нарядов.
- При выборе конкретного заказ-наряда, менеджер должен видеть список запчастей, включенных в данный заказ-наряд.
- Для каждой запчасти должны быть указаны следующие данные: наименование, количество, статус согласования (согласовано/не согласовано).
- Менеджер должен иметь возможность просмотреть подробную информацию о каждой запчасти.
- Менеджер должен иметь возможность выразить согласие или несогласие с каждой запчастью.
- После выражения согласия или несогласия, статус согласования запчасти должен обновиться.
- Система должна сохранять и отображать историю согласований для каждого заказ-наряда.
- В случае изменений в заказ-наряде или списках запчастей, менеджер должен видеть соответствующие уведомления или обновленную информацию.

</details>

<details>

<summary><h4>US003 Я как мастер-диагност хочу получить машину для выполнения диагностики.</h4></summary>
	
- Пользователь (мастер-диагност) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, мастер-диагност должен видеть список доступных автомобилей для диагностики.
- Для каждого автомобиля в списке должны быть указаны следующие данные: марка, модель, год выпуска, номер автомобиля (при наличии), статус (например, "ожидает диагностики").
- Список доступных автомобилей должен быть актуальным и обновляться в реальном времени, отражая текущую доступность для диагностики.
- Мастер-диагност должен иметь возможность выбрать конкретный автомобиль из списка для дальнейшей работы.
- После выбора автомобиля, его статус должен измениться на "в процессе диагностики" или аналогичный, чтобы избежать дублирования работ.
- После завершения диагностики, мастер-диагност должен иметь возможность указать результаты диагностики в системе.
- Система должна сохранять и отображать историю диагностики для каждого автомобиля, включая результаты и действия мастера-диагноста.
</details>

<details>

<summary><h4>US004 Я как менеджер хочу передать ТС мастеру для проведения диагностики.</h4></summary>
	
- Пользователь (менеджер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, менеджер должен иметь возможность просмотреть список доступных транспортных средств, подлежащих диагностике.
- Для каждого транспортного средства в списке должны быть указаны следующие данные: марка, модель, год выпуска, номер автомобиля (при наличии), статус (например, "ожидает диагностики").
- Список транспортных средств должен быть актуальным и обновляться в реальном времени, отражая текущую доступность для диагностики.
- Менеджер должен иметь возможность выбрать конкретное транспортное средство из списка для передачи мастеру для диагностики.
- После выбора транспортного средства, его статус должен измениться на "в процессе диагностики" или аналогичный, чтобы избежать дублирования работ.
- Система должна сохранять и отображать историю передачи транспортных средств для диагностики, включая информацию о том, когда, кому и какое транспортное средство было передано.
- В случае необходимости, система должна предоставить возможность добавления дополнительной информации о транспортном средстве, такой как замечания или особые инструкции для мастера.

</details>

<details>

<summary><h4>US006 Я как мастер-диагност хочу видеть предварительное описание проблемы со слов заказчика.</h4></summary>
	
- Пользователь (мастер-диагност) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, мастер-диагност должен видеть список автомобилей, для которых предоставлено предварительное описание проблемы.
- Для каждого автомобиля в списке должны быть указаны следующие данные: марка, модель, год выпуска, номер автомобиля (при наличии), предварительное описание проблемы, статус (например, "ожидает диагностики").
- Предварительное описание проблемы должно быть доступно для просмотра мастеру-диагносту в четко сформулированном и понятном виде.
- Список автомобилей с предварительным описанием проблемы должен быть актуальным и обновляться в реальном времени.
- Мастер-диагност должен иметь возможность выбрать конкретное транспортное средство из списка для дальнейшей диагностики на основе предварительного описания проблемы.
- После выбора автомобиля, мастер-диагност должен иметь доступ к предварительному описанию проблемы в процессе работы с транспортным средством.
- В случае необходимости уточнения или дополнения информации о проблеме, мастер-диагност должен иметь возможность связаться с заказчиком или другими соответствующими лицами для получения дополнительных данных.

</details>

<details>

<summary><h4>US007 Я как мастер хочу иметь доступ к диагностической карте ТС что бы знать историю ремонта.</h4></summary>
	
- Пользователь (мастер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, мастер должен иметь возможность искать диагностическую карту транспортного средства (ТС) по его уникальному идентификатору (например, по номеру автомобиля или VIN-коду).
- Для каждой диагностической карты ТС должна быть доступна история ремонта, включая предыдущие диагностики, ремонты, замены деталей и другие обслуживающие работы.
- История ремонта должна содержать следующие данные: дата обслуживания, описание выполненных работ, замененные детали, результаты диагностики, замечания и комментарии мастера или заказчика.
- Мастер должен иметь возможность просматривать историю ремонта транспортного средства в удобном и понятном формате, предпочтительно через веб-интерфейс или мобильное приложение.
- Информация в диагностической карте ТС должна быть актуальной и обновляться в реальном времени, отражая последние изменения и проведенное обслуживание.
- Мастер должен иметь возможность добавлять комментарии или обновлять информацию в диагностической карте ТС после проведения диагностики или ремонта.
- Система должна сохранять историю изменений в диагностической карте ТС, чтобы можно было отследить все проведенные работы и обновления информации.

</details>

<details>

<summary><h4>US008 Я как менеджер хочу проверить наличие запчастей для согласования сроков выполнения заказ-наряда.</h4></summary>
	
- Пользователь (менеджер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, менеджер должен иметь возможность просмотреть список запчастей, необходимых для выполнения заказ-наряда.
- Для каждой запчасти в списке должны быть указаны следующие данные: наименование, количество, доступность (в наличии/нет в наличии).
- Список запчастей должен быть актуальным и обновляться в реальном времени, отражая текущее наличие запчастей на складе или их доступность у поставщиков.
- Менеджер должен иметь возможность отфильтровать список запчастей по различным критериям, таким как наименование, производитель, наличие и т. д.
- После проверки наличия запчастей, менеджер должен иметь возможность согласовать сроки выполнения заказ-наряда в зависимости от доступности необходимых запчастей.
- В случае, если какие-либо запчасти отсутствуют, система должна предоставить возможность запросить их закупку у поставщиков или предложить альтернативные решения.
- Система должна сохранять историю проверки наличия запчастей и согласования сроков выполнения заказ-наряда для дальнейшего отслеживания и анализа.

</details>

<details>

<summary><h4>US009 Я как менеджер хочу иметь доступ к заказ-наряду для предварительного подсчёта стоимости ремонта.</h4></summary>
	
- Пользователь (менеджер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, менеджер должен иметь возможность найти и просмотреть нужный заказ-наряд в системе.
- Для каждого заказ-наряда должны быть доступны следующие данные: информация о клиенте, описание работ, список запчастей и их стоимость, предыдущие работы (если таковые имеются).
- Система должна автоматически предоставлять возможность предварительного подсчета стоимости ремонта на основе списка запчастей и предыдущих работ, если они есть.
- Менеджер должен иметь возможность редактировать список запчастей и их стоимость, если это необходимо для более точного подсчета стоимости ремонта.
- После внесения всех необходимых изменений, менеджер должен иметь возможность просмотреть окончательную стоимость ремонта заказ-наряда.
- Система должна автоматически сохранять предварительный и окончательный расчет стоимости ремонта для каждого заказ-наряда.
- Менеджер должен иметь возможность сгенерировать отчет о стоимости ремонта для клиента или для внутреннего использования.
</details>

<details>

<summary><h4>US010 Я как мастер хочу видеть какие ТС назначены мне для проведения работ для эффективно планирования рабочего времени</h4></summary>
	
- Пользователь (мастер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, мастер должен иметь возможность просмотреть список транспортных средств (ТС), которые назначены ему для проведения работ.
- Для каждого назначенного ТС должны быть доступны следующие данные: марка, модель, год выпуска, номер автомобиля (при наличии), статус работ (например, "в процессе", "ожидает диагностики" и т.д.).
- Список назначенных ТС должен быть актуальным и обновляться в реальном времени, отражая текущую загрузку мастера и его рабочее расписание.
- Мастер должен иметь возможность фильтровать список назначенных ТС по различным критериям, таким как статус работ или дата назначения.
- При наличии изменений в назначении ТС (например, добавление нового ТС или изменение статуса работ), система должна предоставлять уведомления мастеру для оперативного реагирования.
- Мастер должен иметь возможность просматривать подробную информацию о каждом назначенном ТС, включая предварительное описание проблемы (если оно предоставлено) и историю обслуживания.
- Система должна сохранять и отображать историю назначений ТС для каждого мастера, чтобы можно было отслеживать его загрузку и производительность.

</details>

<details>

<summary><h4>US011 Я как мастер хочу иметь доступ к заказ-наряду что бы планировать перечень работ.</h4></summary>
	
- Пользователь (мастер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, мастер должен иметь возможность найти и просмотреть нужный заказ-наряд в системе.
- Для каждого заказ-наряда должны быть доступны следующие данные: информация о клиенте, описание работ, предыдущие работы (если таковые имеются), список запчастей и их статус, предварительная стоимость ремонта.
- Система должна автоматически предоставлять возможность мастеру добавлять работы в список работ заказ-наряда на основе предоставленного описания работ и результатов диагностики.
- Мастер должен иметь возможность редактировать список работ заказ-наряда, добавляя, удаляя или изменяя описание работ, их приоритетность и оценочное время выполнения.
- После внесения всех необходимых изменений, мастер должен иметь возможность просмотреть обновленный список работ и убедиться, что он соответствует требованиям клиента и заявленным проблемам с транспортным средством.
- Система должна автоматически сохранять и отображать историю изменений в заказ-наряде, включая добавление, изменение и удаление работ, а также изменение статусов работ и запчастей.
- Мастер должен иметь возможность сгенерировать отчет о планируемых работах для внутреннего использования или для предоставления клиенту при необходимости.
</details>

<details>

<summary><h4>US013 Я как менеджер хочу иметь доступ к каталогу запчастей для корректного составления заказ-наряда.</h4></summary>
	
- Пользователь (менеджер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, менеджер должен иметь возможность найти и открыть каталог запчастей в системе.
- В каталоге запчастей должны быть доступны следующие данные для каждой запчасти: наименование, описание, производитель, номер запчасти (если применимо), цена, наличие на складе.
- Система должна предоставлять возможность менеджеру использовать фильтры и поиск для быстрого нахождения нужных запчастей по различным критериям, таким как наименование, производитель или номер запчасти.
- Менеджер должен иметь возможность добавлять выбранные запчасти в заказ-наряд с указанием нужного количества.
- После добавления запчастей в заказ-наряд, система должна автоматически обновлять информацию о наличии на складе и предоставлять уведомления, если какие-то запчасти отсутствуют или заканчиваются.
- Система должна сохранять и отображать историю добавления запчастей в заказ-наряд для каждого менеджера, чтобы можно было отследить, когда и какие запчасти были заказаны.
- Менеджер должен иметь возможность сгенерировать отчет о составленном заказ-наряде для внутреннего использования или для передачи в отдел закупок.


<details>

<summary><h4>US014 Я как мастер хочу иметь возможность вносить изменения в заказ наряд в случае отсутствия необходимых запчастей.</h4></summary>
	
- Пользователь (мастер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, мастер должен иметь возможность найти и открыть нужный заказ-наряд, который требует изменений из-за отсутствия необходимых запчастей.
- Для каждой запчасти, которая отсутствует на складе, система должна предоставлять возможность мастеру выбрать альтернативные запчасти или запланировать их заказ у поставщика.
- Мастер должен иметь возможность добавить новые или измененные запчасти в список работ заказ-наряда с указанием их описания, количества и приоритета.
- После внесения изменений в заказ-наряд, система должна автоматически обновить информацию о заказе и уведомить о них соответствующих заинтересованных сторон, таких как менеджер или клиент.
- Система должна сохранять и отображать историю изменений в заказ-наряде, чтобы можно было отследить, когда и какие изменения были внесены, а также кто их внес.
- Мастер должен иметь возможность связаться с менеджером или отделом закупок через систему, если требуется дополнительное согласование или уточнение по поводу изменений в заказе.
- После успешного внесения изменений, мастер должен иметь возможность сгенерировать обновленный отчет о заказ-наряде для внутреннего использования или для предоставления клиенту.

</details>


<details>

<summary><h4>US019 Я как мастер хочу иметь возможность сформировать заказ на запчасти для выполнения работ.</h4></summary>
	
- Пользователь (мастер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, мастер должен иметь возможность найти и открыть нужный заказ-наряд, для которого требуется заказать запчасти.
- Система должна предоставлять мастеру доступ к каталогу запчастей, где он может найти необходимые компоненты для выполнения работ.
- Для каждой запчасти, мастер должен иметь возможность выбрать количество и указать примечания или дополнительные требования.
- После выбора необходимых запчастей и указания всех деталей заказа, мастер должен иметь возможность отправить заказ на запчасти в отдел закупок или к поставщику через систему.
- Система должна подтвердить получение заказа и предоставить мастеру уведомление о статусе заказа (например, "в обработке", "отправлен поставщику" и т. д.).
- Мастер должен иметь возможность отслеживать статус своих заказов на запчасти через систему и получать уведомления об изменениях в статусе.
- В случае необходимости, мастер должен иметь возможность отредактировать или отменить заказ до момента его обработки отделом закупок или отправки поставщику.
</details>


<details>

<summary><h4>US020 Я как мастер хочу иметь возможность отмечать выполненные работы для обновления информации по ремонту ТС.</h4></summary>
	
- Пользователь (мастер) должен иметь доступ к системе с использованием своих учетных данных.
- После входа в систему, мастер должен иметь возможность найти и открыть нужный заказ-наряд или диагностическую карту транспортного средства, для которого выполнены работы.
- Для каждой работы или задачи в списке выполненных работ, мастер должен иметь возможность отметить их выполнение с указанием даты выполнения и комментарием (при необходимости).
- Система должна автоматически обновлять информацию о статусе работ в заказе-наряде или диагностической карте, отмечая выполненные работы как завершенные.
- После отметки выполнения работ, система должна предоставлять возможность мастеру просмотреть обновленный список выполненных работ для проверки и подтверждения.
- Мастер должен иметь возможность добавить комментарии или замечания к выполненным работам, если это необходимо для дальнейшего отслеживания и анализа.
- В случае необходимости, мастер должен иметь возможность отменить отметку выполнения работы и вернуть ее в статус "выполняется" для дальнейших изменений или доработок.
- Система должна сохранять и отображать историю изменений статуса работ для каждого заказа-наряда или диагностической карты, чтобы можно было отследить все проведенные работы и их статусы.
</details>

<a name="dev"><h2>Задание на разработку</h2></a>
- 1111
- 2222
- 3333
- 
