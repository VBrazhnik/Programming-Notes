# Соглашения об именовании

Одной из важнейших характеристик исходного кода является его «читаемость» — насколько просто будет разобраться в написанном стороннему программисту.

Чтобы упростить процесс чтения кода, улучшить его «читаемость», применяются соглашения об именовании, форматировании и прочих аспектах кодирования.

Часто в языке программирования существует общепризнанный или официально рекомендованный стандарт.

Также команды могут создавать свои стандарты и соглашения исходя из нужд проекта или личных предпочтений.

Каждый стандарт имеет свои преимущества и недостатки. Но самым важным в контексте «читаемости» является наличие стандарта как такового, а также его последовательное применение в исходном коде.

Одним из важнейших соглашений является соглашение об именовании, которое определяет как будут именоваться сущности: переменные, константы, функции, классы и модули.

Существует несколько популярных нотаций именования:

* Camel case \(camelCase\)
* Pascal case \(PascalCase\)
* Snake case \(snake\_case\)
* Uppercase snake case \(UPPERCASE\_SNAKE\_CASE\)
* Kebab case \(kebab-case\)

В реальности их гораздо больше, хотя многие уже вышли из обихода и не употребляются, либо употребляются крайне редко. Например, Cobol case \(COBOL-CASE\).

Каждая из перечисленных выше нотаций являет собою подход к записи нескольких слов без использования пробелов между ними. Это обусловлено тем, что в языках программирования нет возможности использовать пробелы в именах сущностей.

Поэтому эти нотации также называют стилями написания составных слов.

Также существует особая нотация — Венгерская \(Hungarian notation\). Ее стоит отделять от уже упомянутых, поскольку основным ее назначением является не задание стиля записи, а добавление метаданных в названия сущностей.

## Camel case

**Русскоязычное название:** «Верблюжий регистр», «Горбатый регистр».

**Стилизованное название:** camelCase.

**Описание:** Имя записанное в Camel case являет собою несколько слов, записанных слитно без пробелов. Первое слово начинается со строчной буквы, все последующие — с прописной.

**Примеры:** `user`, `isConnected`, `symbolsCount`, `unsubscribeTitle`, `campaignId`.

**Применение:** Во многих языках данная нотация используется в качестве соглашения об именовании переменных.

## Pascal case

**Русскоязычное название:** «Нотация Паскаля».

**Стилизованное название:** PascalCase.

**Описание:** В Pascal case слова пишутся слитно. Каждое из них начинается с заглавной буквы. В отличие от Camel case, где первое слово начинается со строчной.

**Примеры:** `User`, `IsConnected`, `SymbolsCount`, `UnsubscribeTitle`, `CampaignId`.

**Применение:** Данная нотация широко используется при именовании классов во многих языках программирования.

{% hint style="info" %}
Существует альтернативное мнение, касательно стилей называемых Camel case и Pascal case.

Согласно этому мнению есть два подвида нотации Camel case: lower \(lowerCamelCase\) и upper \(UpperCamelCase\).

И Pascal case является лишь альтернативным названием для подвида upper, а не отдельным стилем.
{% endhint %}

## Snake case

**Русскоязычное название:** «Змеиный регистр».

**Стилизованное название:** snake\_case.

**Описание:** В Snake case все слова пишутся строчными буквами. А вместо пробела используется символ нижнего подчеркивания — `_`.

**Примеры:** `user`, `is_connected`, `symbols_count`, `unsubscribe_title`, `campaign_id`.

**Применение:** Snake case используется при именовании полей в базах данных.

## Uppercase snake case

**Русскоязычное название:** «Змеиный регистр в верхнем регистре».

**Стилизованное название:** UPPERCASE\_SNAKE\_CASE.

**Описание:** Uppercase snake case, как и Snake case, использует символ нижнего подчеркивания в качестве замены пробелу. Только в отличие от Snake case все слова записываются прописными буквами.

**Примеры:** `USER`, `IS_CONNECTED`, `SYMBOLS_COUNT`, `UNSUBSCRIBE_TITLE`, `CAMPAIGN_ID`.

**Применение:** Данная нотация часто используется в качестве соглашения об именовании констант.

## Kebab case

**Русскоязычное название:** «Шашлычная нотация».

**Стилизованное название:** kebab-case.

**Описание:** Kebab case похож на Snake case, только в нем пробелы заменяются на дефисы — `-`. Слова также пишутся строчными буквами.

**Примеры:** `user`, `is-connected`, `symbols-count`, `unsubscribe-title`, `campaign-id`.

**Применение:** Данный стиль часто используется в ссылках. Например, _http://example.com/article-about-cases/_.

## Венгерская нотация

Венгерская нотация \(Hungarian notation, HN\) — соглашение об именовании переменных, констант и прочих идентификаторов, созданное венгерским программистом Чарльзом Симони во время работы в Microsoft.

Именно происхождение автора дало имя данной нотации.

Согласно Венгерской нотации идентификатор должно иметь префикс, который бы указывал, что находится в переменной, константе или поле — содержал метаданные о них.

Существует множество различных метаданных, которые можно добавить к именам идентификаторов. Среди них есть следующие виды:

* Данные о типе
* Данные о видимости
* Данные о назначении

### Данные о типе

Это наиболее распространенное использование метаданных: именование сущности таким образом, чтобы ее тип можно было узнать по имени.

**Примеры**

| Идентификатор | Префикс | Значение |
| :--- | :--- | :--- |
| `sUnsubscribeTitle` | `s` | string |
| `bIsEmpty` | `b` | boolean |
| `iSize` | `i` | integer |

### Данные о видимости

В ином случае используемые метаданные могут указывать с каким видом переменной программист имеет дело: приватным полем, локальным параметром, глобальной переменной или параметром функции.

**Примеры**

В JavaScript префикс состоящий из нижнего подчеркивания — `_` используется, чтобы пометить поле или метод как приватные.

Также во многих языках программирования широко используется префикс `g_` для обозначения глобальных переменных.

### Данные о назначении

Также метаданные могут отражать назначение сущности.

**Примеры**

| Идентификатор | Префикс | Значение |
| :--- | :--- | :--- |
| `aDimensions` | `a` | array |
| `iCat` | `i` | index |
| `сSymbols` | `c` | counter |

Венгерская нотация имеет неоднозначную репутацию. Многие программисты заявляют, что являются противниками данного подхода к именованию.

В книге Мартина Роберта «Чистый код: создание, анализ и рефакторинг» есть следующие строки о схемах кодирования имен:

> У нас и так хватает хлопот с кодированием, чтобы искать новые сложности. Кодирование информации о типе или области видимости в именах только создает новые хлопоты по расшифровке. Вряд ли разумно заставлять каждого нового работника изучать очередной «язык» кодирования — в дополнение к изучению \(обычно немалого\) объема кода, с которым он будет работать.

А также о Венгерской нотации в частности:

> Таким образом, в наши дни венгерская запись и другие формы кодирования типов в именах превратились в обычные пережитки прошлого. Они усложняют изменение имени или типа переменных, функций и классов. Они затрудняют чтение кода. Наконец, они повышают риск того, что система кодирования собьет с толку читателя кода.

**Источники информации:**

* [«Именование в программировании»](https://ru.hexlet.io/blog/posts/naming-in-programming)
* [«Case Styles: Camel, Pascal, Snake, and Kebab Case»](https://medium.com/better-programming/string-case-styles-camel-pascal-snake-and-kebab-case-981407998841)
* [«Я являюсь причиной появления венгерской нотации в Android»](https://habr.com/en/post/333596/)
* [«Making Wrong Code Look Wrong»](https://www.joelonsoftware.com/2005/05/11/making-wrong-code-look-wrong/)

