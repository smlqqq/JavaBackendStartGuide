# Руководство по вкатыванию в backend-разработку на Java для почти начинающих и сочувствующих.

Дисклеймер:

- *В руководстве рассматривается развитие Java backend-разработчика.*

- *Руководство написано исходя из того, что читатель не полный новичок в CS и у него есть базовые знания*.

- *Руководство намеренно написано в неформальном стиле, в формате монолога. Все предлагаемые изменения должны соответствовать данному стилю.*

- *Целью руководства не является составление полного списка всех возможных курсов, книг или обучающих материалов. Состав должен представлять собой краткий, но не кратчайший список из максимально полезных обучающих материалов, советов и рекомендаций*.

- *Использование изображений в руководстве разрешено только в крайних случаях. Оставьте картинки профильным статьям.*

  

  ## Оглавление:
  - [Руководство по вкатыванию в backend-разработку на Java для почти начинающих и сочувствующих.](#руководство-по-вкатыванию-в-backend-разработку-на-java-для-почти-начинающих-и-сочувствующих)
  - [Почему Java?](#почему-java)
  - [Обучение](#обучение)
    - [Подготовка к подготовке](#подготовка-к-подготовке)
    - [Java Core Base](#java-core-base)
      - [Курсы](#курсы)
        - [Туториалы от Oracle](#туториалы-от-oracle)
        - [JavaRush](#javarush)
        - [Stepik](#stepik)
        - [HyperSkill (JetBrains Academy)](#hyperskill-jetbrains-academy)
        - [YouTube](#youtube)
        - [Udemy](#udemy)
      - [Книги](#книги)
        - [Герберт Шилдт, Java. Полное руководство и Java. Руководство для начинающих](#герберт-шилдт-java-полное-руководство-и-java-руководство-для-начинающих)
        - [(Опционально) Кей Хорстманн, Java. Библиотека профессионала, Том 1. Основы](#опционально-кей-хорстманн-java-библиотека-профессионала-том-1-основы)
        - [(Опционально) Кэти Сьерра и Берт Бейтс, Изучаем Java (Head First Java)](#опционально-кэти-сьерра-и-берт-бейтс-изучаем-java-head-first-java)
        - [Джошуа Блох, Java. Эффективное программирование](#джошуа-блох-java-эффективное-программирование)
      - [Упражнения](#упражнения)
      - [Что делать если возникли вопросы?](#что-делать-если-возникли-вопросы)
      - [Подведение итогов Core](#подведение-итогов-core)
    - [Java Core Advanced](#java-core-advanced)
      - [Книги](#книги-1)
        - [Рауль Урма, Марио Фуско, Алан Майкрофт. Современный язык Java](#рауль-урма-марио-фуско-алан-майкрофт-современный-язык-java)
        - [Брайан Гетц. Java Concurrency на практике](#брайан-гетц-java-concurrency-на-практике)
        - [Адитья Бхаргава. Грокаем алогритмы](#адитья-бхаргава-грокаем-алогритмы)
        - [(Опционально) Роберт Лафоре. Структуры данных и алгоритмы Java](#опционально-роберт-лафоре-структуры-данных-и-алгоритмы-java)
        - [(Опционально) Николай Палрог. Система модулей Java](#опционально-николай-палрог-система-модулей-java)
        - [(Опционально) Кен Коузен. Современный Java. Рецепты программирования](#опционально-кен-коузен-современный-java-рецепты-программирования)
      - [Паттерны](#паттерны)
      - [Упражнения](#упражнения-1)
      - [Подведение итогов Advanced Core](#подведение-итогов-advanced-core)
    - [Вступаем во взрослый мир](#вступаем-во-взрослый-мир)
      - [Системы сборки](#системы-сборки)
      - [Тестирование](#тестирование)
      - [Логирование](#логирование)
      - [SQL](#sql)
      - [Базы данных](#базы-данных)
        - [JDBC](#jdbc)
      - [ORM](#orm)
        - [Hibernate](#hibernate)
    - [Spring](#spring)
      - [Spring Core](#spring-core)
        - [Книги](#книги-2)
          - [Craig Walls. Spring in Action 4](#craig-walls-spring-in-action-4)
        - [Курсы](#курсы-1)
        - [Официальная документация](#официальная-документация)
      - [Spring Boot](#spring-boot)
        - [Курсы](#курсы-2)
      - [Spring Data](#spring-data)
      - [Spring MVC](#spring-mvc)
      - [Spring Security](#spring-security)
      - [Упражнения](#упражнения-2)
    - [Контейнеры](#контейнеры)
      - [Docker](#docker)
      - [Kubernetes](#kubernetes)
    - [Основы CI/CD](#основы-cicd)
      - [Jenkins](#jenkins)
    - [Реактивное программирование](#реактивное-программирование)
    - [Эпилог](#эпилог)

## Почему Java?

Первый вопрос который сразу приходит в голову, когда выбираешь язык. На это есть целый ряд причин:

1. **Огромная база кода.** Если ты хочешь что-то сделать, с большой вероятностью для этого уже есть библиотека;
2. **Отличная документация.** Подробнейшее описание API языка (Javadoc), дотошно описанная спецификация самого языка (JLS) и спецификация модели памяти (JMM) добавляют уверенности, что если у тебя появился вопрос: «Как это работает?» или «Почему это работает именно так?» — на него получится найти ответ;
3. **Гибкость.** Java это не только язык, но и JVM платформа. С использованием этой платформы написаны, например, Kotlin (привет, Android), Scala (привет, ФинТех) и Clojure (привет, эээ, страдание?). Всё это позволяет нам, оседлав Java и потратив некоторое время, дрейфовать в сторону той предметной области, которая наиболее интересна;
4. **Сообщество.** Если у вас появился вопрос, на него, скорее всего, ответили ещё в 2010. Если у тебя появилась гениальная идея проекта, на гитхабе, вероятно, уже есть десяток различных реализаций. Новичкам всегда радостно помогут советами прочитать, наконец, Javadoc;
5. **Карьерные возможности.** Java повсюду: backend, mobile, desktop (нет, он не умер). Без работы точно не останешься.

Есть и ворох недостатков:

1. **Многословность**. Java многословна. То, что сейчас в пайтоне занимает одну строку, в Java займёт 10. Не такой большой минус в современном мире, где есть Intellij и автодополнение, плюс в язык добавляются модные фичи вроде `var` . К тому же в языках вроде Kotlin или Scala можно писать достаточно компактный код;
2. **Обилие устаревшего кода.** Java появилась в 1995 году, и с тех пор было написано много кода. Чертовски много. Всё это нужно поддерживать, развивать и лелеять, так как бизнес очень не любит тратить деньги. Например Java 8 вышла в 2014 году, а согласно [опросу](https://www.jetbrains.com/ru-ru/lp/devecosystem-2020/java/) JetBrains в 2020 году, её доля составляет 75%! Так что, залетев на работу, с высокой долей вероятности ты будешь писать на старой версии, в которой нет современного сахара, увы;
3. **Ограниченная сфера применения.** В современном мире Java по настоящему блистает в качестве backend-языка. Да, ты можешь писать mobile, но там развивается Kotlin. Да, ты можешь писать desktop, но люди выбирают Electron. Локомотив хайпа находится в вебе, поэтому мы садимся именно в него.

## Обучение

Если хорошенько поискать, можно найти десятки статей о том, какие книги лучше читать и какие курсы лучше проходить. Заботливые люди рисуют дорожные карты и, казалось бы, просто бери и следуй гайдам. Но проблема в том, что их слишком много! Современный мир backend-разработки требует от тебя разбираться в куче вещей, и простой человек Василий, попробовав во всём этом разобраться, очень скоро почувствует беспомощность, грусть и отчаяние. 

Однако, всё не так страшно. Учиться придется действительно очень много, однако мы отобрали только самые лучшие ~~зёрна~~ материалы.

### Подготовка к подготовке

Перед обучением тебе понадобится:

- **Установка Java**. Бери всегда самую свежую версию. Даже если на работе будешь писать на восьмерке, всегда стоит держать руку на пульсе и быть в курсе всех современных Java фишек. 

- **Среда разработки.** Используй intellij IDEA Community, скажешь спасибо потом. Из альтернатив есть: 
  - Eclipse. Старый, неудобный, но ещё относительно популярный в некоторых местах;
  - VS Code. Это не IDE, но хороший редактор кода, который обвешивают кучей плагинов;
  - NetBeans. Когда-то очень давно была популярна, сейчас используется только теми, кто случайно скачал инсталлятор.
- **Знакомство с Git**. Гит — система контроля версий. Если ты когда-нибудь слышал слова "коммиты", "ветки" и "PR" — это оно. Для начала хватит простого [гайда](https://rogerdudler.github.io/git-guide/index.ru.html), чтобы понимать базовые термины. Потом стоит почитать документацию к своей IDE. IDEA, например, поддерживает работу с гит из коробки.
- **Профиль на GitHub**. Гитхаб — это такая социальная сеть для разработчиков. Ставь лайки библиотекам, которые используешь, и изучай тренды. Не стесняйся выкладывать туда все свои мелкие проекты, только не забывай про Readme. Потом будешь рад, когда будешь искать проект, в котором ты делал работающие аспекты или работу с авторизацией.
- **Ведение заметок.** Очень важный пункт. Тебе предстоит поглощать огромное количество информации, большую часть которой ты забудешь уже на следующий день. Чтобы помочь своему мозгу, начни вести заметки по методике ZettelKasten, например, в notion.io https://habr.com/ru/post/509756/.
- **Будь в курсе**. Java активно развивается. Чтобы не остаться в стороне от важных новостей, ты должен читать эти новости. Начни с подписки на ежемесячную подборку [Java Annotated](https://blog.jetbrains.com/idea/tag/java-annotated/) и не стесняйся подписываться на интересных авторов.

### Java Core Base

Java Core — это основа понимания языка и представление о его возможностях, работающих «из коробки». Так как это фундамент, подойти к его формированию стоит очень ответственно, чтобы не страдать позже и не пытаться изобрести велосипед. Не стоит пытаться сэкономить время, хитрить или пропускать «неинтересные» куски. Поверь, уверенная база тебе воздастся в будущем, ибо на собеседованиях гоняют в основном по Core.

#### Курсы

**Помни, что ни один из курсов не дает полную базу. Используй их как дополнение к книгам.**

##### Туториалы от Oracle

Oracle является разработчиком языка и предоставляет собственные обучающие [материалы](https://docs.oracle.com/javase/tutorial/), довольно неплохого качества. Ещё и бесплатно. Из минусов: рассматривается java 8, и некоторые темы рассмотрены очень сжато. Но всё равно обязательно загляни, там много интересного.

##### JavaRush

В странах СНГ и Украине весьма популярен великий и ужасный JavaRush. Интернет пестрит историями успеха, как простой слесарь Григорий стал успешным и теперь зарабатывает 300кк/наносек. Тысячи практических задач! Сотни тысяч пользователей! За какие-то смешные деньги ты сможешь полностью изменить свою жизнь!

Так вот, ни в коем случае на это не ведись. JavaRush очень сильно страдает отрывочной подачей теории, из-за чего люди застревают даже на простых задачках. Задумайся, при написании технической книги она проходит множество стадий вычитки и рецензирования. На JavaRush таким, понятное дело, никто не занимается. Не трать зря время, деньги и нервы, и представь, что такого сайта просто не существует. Даже если ты знаешь человека, который знает человека, который сказал, что там всё круто.

##### Stepik

Агрегатор курсов от различных авторов, разной степени качества. Из того, что смотрел сам, могу посоветовать [Java. Базовый курс](https://stepik.org/course/187/promo).

##### HyperSkill (JetBrains Academy)

Совместный проект Stepik и JetBrains. Содержит треки (курсы) по разным языкам: Python, Java, Kotlin, JS. 

Обучение ведется в разрезе мини-проектов: выбираете проект определенной сложности (от консольных крестиков-ноликов до интеграций со Spotify и веб-приложений), который разбивается на несколько стадий. По каждой стадии дается набор теории, по теории проходятся мелкие задачки. Кто-то скажет, что весьма смахивает на JavaRush, но отличие в качестве материала. Часть берется со Stepik, часть создают сами с модерированием и предварительной бетой.

Тем у них ОЧЕНЬ много, от Java Core до математики и алгоритмов. Core описан очень хорошо, остальные похрамывают. 

Материал полностью на «русском английском», так что читать его несложно, но иногда не понятно, что пытался сказать автор. Платный, можно получить три месяца бесплатного триала, потом по $249 в год.

Из минусов, очень задумчивый интерфейс, некоторые проекты крайне скудны на описание некоторые тесты приходится «хакать» из-за непонятной логики проверки. В остальном, идеальный вариант для механического прорешивания простых задачек.

##### YouTube

Тысячи индусов и сочувствующих готовы прийти на помощь. Заманивают бесплатностью и объемом материалов, но помни про устаревание и что за адекватность материала отвечает только сам автор. Из курсов на русском многие советуют Алишева, не смотрел не могу оценить. Зато абсолютно точно могу рекомендовать бесплатный курс Тагира Валеева, весна 2020. [Туть](https://www.youtube.com/playlist?list=PLlb7e2G7aSpRZSRZxANkvpYC82BXUzCTY)

Тагир широко известный во всем мире джавист, работает в JetBrains, является Java чемпионом (да, это реальное звание). В курсе очень хорошо проходит по кишочкам языка, может тяжеловато заходить, поэтому параллельно шлифуй другими материалами. Но курс постарайся прослушать полностью, оно того стоит.

##### Udemy

Обрати внимание на курс от Tim Buchalka, вот [здесь](https://www.udemy.com/course/java-the-complete-java-developer-course/). Он очень хорошо и подробно разжевывает Java в серии небольших видео, общей длительностью около 80 часов. Даже упражнения после тем есть. Говорит с австралийским акцентом, но есть английские субтитры, так что рекомендую. Эдакий видео Шилдт по подробности материала. На цены в 10к+ рублей не смотри, на Udemy постоянно идут распродажи со скидками в 80-90%. Так что если видишь полный прайс, просто добавь вишлист и подожди пару недель. Скинут до 1.5к рублей, всегда скидывают.

#### Книги

Лучше всего читать на английском, но можно и переводы. Помни, что переводы зачастую являются устаревшими и ВНЕЗАПНО труднее читаются, из-за того, что одни и те же термины в разных книгах могут переводить по разному.

##### Герберт Шилдт, Java. Полное руководство и Java. Руководство для начинающих

«Полное руководство» это увесистый том на 1.5к страниц, который с трудом помещается в руках. Бери его если у есть безответная любовь к справочникам или если вы любишь максмально дотошное описание API языка. Если нет, бери «Руководство для начинающих», которое в два раза короче и наслаждайся подробным описанием языка без километровых описаний API. Имей в виду, что в руководстве для начинающих не освещены «продвинутые» темы, так что сверься с содержанием.

##### (Опционально) Кей Хорстманн, Java. Библиотека профессионала, Том 1. Основы

Хорстманн пишет более сухо и сжато чем Шилдт, некоторые моменты описаны более на «низком» уровне (объяснения как оно устроено внутри). Пестрит вставками сравнениями с С++. Ваш выбор если уже есть/был опыт других языков и нет потребности в разжевывании материала.

##### (Опционально) Кэти Сьерра и Берт Бейтс, Изучаем Java (Head First Java)

Если ты начал читать Шилдта и всё равно чувствуешь, что ничего не понимаешь, попробуй эту книгу. Написано максимально простым языком, много картинок. После её прочтения в голове должна сложиться простая мозаика, что позволит вернуться к более «взрослым» книгам.

##### Джошуа Блох, Java. Эффективное программирование

Книга которую обязательно стоит прочитать после Хорстманна и Шилдта, и регулярно перечитывать. Блох один из создателей языка, и в своей книге описал best practice: правильное написание equals и hashCode, как правильно готовить generics, почему лямбды это хорошо и много другое. Написано доступно, читается легко.

#### Упражнения

Теория это замечательно, но нужно постоянно писать код. Лучшие места для этого:

1. Задачки и проекты HyperSkill. Много хороших и разных, но платно;
2. [CodeWars](https://www.codewars.com/). Ориентируйся на уровень сложности 8-7kyu, можно 6kyu но может оказаться сложно;
3. [CodingBat](https://codingbat.com/). Элементарные задачки на уровне первого курса университета;
4. [HackerRank](https://www.hackerrank.com/). Выбираешь Java, выбираешь Easy, прорешиваешь.

#### Что делать если возникли вопросы?

Не знаешь как разбить строку на символы? Не помнишь как прочитать текст из файла? Забыл как быстро можно отсортировать массив? Со всем этим помогут следующие ресурсы:

1. [Javadoc](https://docs.oracle.com/en/java/javase/16/docs/api/index.html). Подробное описание API языка. Хочешь сделать что-то со строкой? Загляни в Javadoc класса String. Хочешь сделать что-то с массивом? Загляни в javadoc класса Arrays. Javadoc это первое место куда ты должен идти при любом вопросе. Не знаешь с какого класса начать поиск? Просто вбей в поиск что-то вроде `Java String split javadoc` и с высокой долей вероятности первые строчки будут вести на нужный класс;
2. [StackOverflow](https://stackoverflow.com/). Самый популярный ресурс для копипаста кода и ответов на твои вопросы. Являются ли строки в Java иммутабельными? Что такое знак джокера? Что такое PECS? На всё это ты сможешь найти ответ вбив в поиск `Java pecs stackoverflow`
3. [Baeldung](https://www.baeldung.com/). Сборник статей и рецептов на все случаи жизни. Что нового в Java 16? Какими способами можно сортировать List? Чем отличается ArrayList от LinkedList. Скорее всего про это уже есть статьи на baeldung.
4. [Telegram](https://t.me/javastart). Если твой поиск не увенчался успехом, и ты готов опустить руки, приходи к живым, русскоговорящим людям и попроси помощи. Тут не решат за тебя твои задачи, но помогут с направлением копания.

#### Подведение итогов Core

Итак, ты прошел/посмотрел курсы, прочитал базовые книги и даже прорешал кучу упражнений. Чувствуешь себя уверенно и даже расправил плечи? Самое время поиграть в карточки. Есть отличный гитхаб [репозиторий](https://github.com/enhorse/java-interview) в котором есть куча популярных вопросов на собеседованиях. Сейчас тебе стоит обратить внимание на:

1. [ООП](https://github.com/enhorse/java-interview#ООП)
2. [Java Core](https://github.com/enhorse/java-interview#java-core)
3. [Java Collections Framework](https://github.com/enhorse/java-interview#java-collections)
4. [Java 8](https://github.com/enhorse/java-interview#java-8) 

Не ленись занести вопросы в карточки [Anki](https://apps.ankiweb.net/) или распечатать в бумажном виде. Повторяй на регулярной основе, но помни, что твоя задача не заучить их механически, но научиться приходить к ответам логическим путем. Когда придешь на собеседование и будешь трястись от нервов и пить воду шумными глотками, все твои зубрежки вылетят из головы, но понимание материала никуда не денется.

### Java Core Advanced

Итак, ты уже уверенно владеешь базовыми средствами языка. Без проблем решаешь базовые задачи, знаешь состав CollectionsFramework, понимаешь отличие HashMap от TreeMap и даже знаешь что есть стримы и ещё другие стримы. Самое время нырнуть в Core ещё глубже.

#### Книги

##### Рауль Урма, Марио Фуско, Алан Майкрофт. Современный язык Java

Выход Java 8 изменил экосистему Java навсегда. Stream API, default методы, лямбды, без этих вещей невозможно представить современную Java разработку. В этой книге подробно описаны все киллер фичи Java 8. Некоторые моменты, вроде конкурентности могут быть непонятными, но обязательно вернись к ним позже.

*Обрати внимание, в русском переводе есть проблема с перепутанными примерами кода в первых главах.*

##### Брайан Гетц. Java Concurrency на практике

Современный web это высокие нагрузки, тысячи клиентов, и терабайты данных. Чтобы твоё приложение могло утилизировать ресурсы сервера по максимуму, ты должен сдать джедаем конкурентного/параллельного программирования. Эта книга must read абсолютно для всех разработчиков. Несмотря на то, что она написана для Java 5, все её советы актуальны и по сей день. Может читаться тяжело, но прочитать ты её обязан.

##### Адитья Бхаргава. Грокаем алогритмы

По поводу того когда лучше знакомиться с алгоритмами ведутся бесконечные диспуты. Наше мнение — каждый решает сам для себя. Но конкретно эту книгу лучше прочитать пораньше. Она в интересной форме расскажет про базовые термины вроде сложности алгоритмов, познакомит тебя с некоторыми видами сортировок и прочими интересными штуками. Звучит сложно, но поверь, это именно та книга, который может вызвать у тебя любовь к алгоритмам.

##### (Опционально) Роберт Лафоре. Структуры данных и алгоритмы Java

Многие критикуют данную книгу из-за странного стиля кода и занудной подачи материала, но если вдруг тебе захотелось копнуть алгоритмы чуть поглубже, можешь попробовать.

##### (Опционально) Николай Палрог. Система модулей Java

Одной из ключевых фишек Java 9, стала новая система модулей, которая позволяет получить абстракцию над привычными пакетами и получить более сильную инкапсуляцию классов. Её весьма неохотно используют (в основном из-за лени и легаси), но уметь готовить модули будет приятным бонусом к твоим навыкам.

##### (Опционально) Кен Коузен. Современный Java. Рецепты программирования

Практически всё тоже, что в книге Урмы, только как сборник кратких рецептов: как использовать коллекторы, компараторы и потоки. Всё это с небольшими понятными примерами. Книга весьма хороша как краткая выжимка-handbook.

#### Паттерны

Многие проблемы, которые возникают при разработке приложений появляются из-за ошибок допущенных при проектировании. Умные люди выявили повторяющиеся из проекта в проект решения и закономерности (паттерны) и сделали их классификацию. Почему важно их знать? Паттерны описывают типичные способы решения часто встречающихся проблем при проектировании программ, что позволяет тебе не изобретать велосипед, а твоим коллегам гораздо быстрее понимать, что происходит в коде. Из ресурсов по паттернам можно выделить:

1. [Refactoring guru](https://refactoring.guru/ru/design-patterns). Модно, молодежно, доступный язык.
2. **Design Patterns: Elements of Reusable Object-Oriented Software (GoF)** — сухой академический оригинал, сможешь осилить — хорошо, не сможешь — используй другие источники.

#### Упражнения

Подойдут всё те же сайты которые были на прошлом этапе, но уже с более высокой сложностью. Старайся решать задачи с использованием «современных» функциональных фишек Java: Stream API и лямбды.

#### Подведение итогов Advanced Core

Помнишь те карточки которые ты поленился сделать на прошлом этапе? Самое время добавить новые:

1. [Потоки ввода-вывода в Java](https://github.com/enhorse/java-interview#Потоки-вводавывода-в-java)
2. [Сериализация](https://github.com/enhorse/java-interview#Сериализация)
3. [Многопоточность](https://github.com/enhorse/java-interview#Многопоточность) 
4. [Шаблоны проектирования](https://github.com/enhorse/java-interview#Шаблоны-проектирования)

### Вступаем во взрослый мир

Если ты добрался до этого пункта, мы мысленно пожимаем тебе руку. Осилить такое количество материала и не сдаться, достойно уважения. Но наше путешествие продолжается. Имей в виду, что если Core ты должен знать назубок, то знание всего ниже перечисленного может варьироваться от базового до нормального. Полностью прокачаться можно, увы, только на реальной работе. 

#### Системы сборки

Современные приложения редко состоят из парочки классов которые запускаются из среды разработки. Работа с зависимостями твоего проекта, его сборка/упаковка, всё это ответственность систем сборки. Они берут на себя нудную и иногда тяжелую работу, чтобы твой проект на развалился под грузом [JAR hell](https://dzone.com/articles/what-is-jar-hell). На момент 2021 года, в Java есть две наиболее популярных системы сборки:

1. [Gradle](https://gradle.org/). Модно, молодежно, инкрементальная компиляция, описание билд файла на Groovy или Kotlin DSL. Быстрый старт [здесь](https://docs.gradle.org/current/samples/sample_building_java_applications.html).
2. [Maven](https://maven.apache.org/). Почти нестареющая классика. Описание билда файла на XML, есть множество плагинов на любой вкус, расширяющие стандартную функциональность. Быстрый старт [здесь](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html).

Попробуй оба варианта, останься на том который тебе больше нравится. С этого момента **все** твои проекты должны собираться только с использованием выбранной тобой системой сборки. Они используются в любом реальном проекте, и ты должен уметь такие проекты открывать, дорабатывать и собирать.

#### Тестирование

Ты можешь быть уверенным в качестве своего кода, но ещё больше уверенности тебе даст покрытие своего кода тестами. Тестирование это отдельная крупная тема для разговора. Наиболее популярным фреймворком для тестирования является JUnit. Начать своё погружение в увлекательный мир тестирования ты можешь

- Со сборника статей Baeldung [здесь](https://www.baeldung.com/junit)
- С официальных [гайдов](https://junit.org/junit5/docs/current/user-guide/) JUnit

#### Логирование

Чем крупнее твоё приложение, тем больше возникает необходимость понимать, что за процессы в нем происходят. Отладка возникающих ошибок, сбор статистики и многое другое практически невозможно без наличия логов. С системами логирования в Java всё очень плохо. Их много, у них разный подход к конфигурации, а ещё они могут связываться друг с другом в забавных франкенштейнов. Из наиболее популярного, обрати внимание на:

- SLF4J + Logback
- Log4j2
- JBoss logging

Проще всего будет настроить SLF4J Simple по этому [мануалу](http://www.slf4j.org/manual.html). И помни, с этого момента в твоём коде не должно быть ни одного ```System.out.println``` только взрослое логирование.

#### SQL

Современный web мир невозможен без данных, а где данные, там и базы данных. Тебе нужно понимать синтаксис SQL и уметь писать на нем запросы. В этом тебе поможет:

1. [Туториал](https://www.w3schools.com/sql/) от W3Schools
2. Книга Алана Бьюли «Изучаем SQL»
3. Прорешивание задачек на [SQL-EX](https://www.sql-ex.ru/learn_exercises.php)
4. Если у тебя есть доступ к HyperSkill, пройди раздел «Databases and SQL» вот [тут](https://hyperskill.org/knowledge-map/520).

Становится джедаем запросов не надо, но у тебя должно сложиться понимание как ты можешь вертеть данные на своей будущей БД.

#### Базы данных

После того как ты овладел SQL, самое время подключить к своему приложению настоящую базу данных. Систем управления базой данных великое множество, на начальном этапе обрати внимание на:

1. PostgreSQL/MySQL — классические реляционные СУБД;
2. H2 — наиболее популярная in memory СУБД, хорошо подойдет для твоих небольших проектов;
3. MongoDB — популярная NoSQL СУБД

##### JDBC

#### ORM

##### Hibernate

### Spring

Спринг — это самая популярная веб-экосистема в Java. Состоит из целого набора различных фреймворков, разного назначения: работа с БД, облаками, безопасностью, и многое другое. Да, у него есть менее популярные альтернативы, но с высокой долей вероятности, на работе ты столкнешься именно с ним. Так что добро пожаловать в весну.

#### Spring Core

Как у Java есть свой базовый Core, так есть он и у Spring. Стоит хорошенько разбираться в его составе, чтобы когда ты поднимешься на абстракцию выше, в Spring Boot, он не показался тебе загадочной магией.

##### Книги

###### Craig Walls. Spring in Action 4

Обрати внимание, **именно 4-е издание**. Да, мы в курсе, что есть пятое. Да, мы в курсе, что перевод на русский есть только на третье издание. Но в пятом нет подробного описания подкапотных кишочков, и выкинута настройка с помощью XML. Ты можешь подумать, что «Какой XML, аннотации везде?», но твой будущий работодатель запиливший систему в мохнатых годах может не разделять твоё прогрссивное мнение. Так что читай 4-е издание и наслаждайся. Книга стоит того.

##### Курсы

На Udemy есть хороший инструктор, John Tompson, который шпарит курсы по Spring как автомат. Не стоит обходить его вниманием и загляни [сюда](https://www.udemy.com/course/spring-core/). Рассматривается более старая версия Spring (4), но за 6 часов даётся вполне неплохая база по Spring и затрагивается работа со Spring MVC.

##### Официальная документация

Казалось бы, зачем мы явно включили официальную документацию, если мы с самого начала запомнили, что всегда стоит начинать поиск с неё? Однако, со Spring ситуация несколько иная. Его документация ВОСХИТИТЕЛЬНА. Серьезно, эта документация одна из весомых причин, почему Spring так быстро завоевал популярность. Подробнейшие описания его концептов, сопровождаемые примерами кода, описание концептов, и многое, многое другое. Начни своё путешествие [отсюда](https://docs.spring.io/spring-framework/docs/current/reference/html/index.html) и поверь, очень многие вопросы у тебя не появятся, если ты внимательно ознакомишься с этими материалами.

#### Spring Boot

Spring Boot это абстракция над абстракциями. Разработчики взяли обычный Spring, полезные библиотеки и упаковали всё это в фреймворк более высокого (по абстракции) уровня. Меньше бойлерплейта и головной боли, больше магии и головной боли.

##### Курсы

Помнишь John Tompson? Даже если нет, самое время навернуть его 60 часовой [курс](https://www.udemy.com/course/spring-framework-5-beginner-to-guru/) по Spring Boot. В нем также затрагивается работа со Spring MVC, Spring Data и немножко Hibernate. Объясняет доступно, много примеров, простой английский язык. Полностью стоит своих 1.5к рублей.

#### Spring Data

#### Spring MVC

#### Spring Security

#### Упражнения

### Контейнеры

#### Docker

#### Kubernetes

### Основы CI/CD

#### Jenkins

### Реактивное программирование

### Эпилог

