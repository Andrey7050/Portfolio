<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Открытие-файлов-с-данными-и-объединения-их-в-один-датафрейм" data-toc-modified-id="Открытие-файлов-с-данными-и-объединения-их-в-один-датафрейм-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Открытие файлов с данными и объединения их в один датафрейм</a></span><ul class="toc-item"><li><span><a href="#Изучим-общую-информацию-о-данных-таблицы-mkrf_shows.csv" data-toc-modified-id="Изучим-общую-информацию-о-данных-таблицы-mkrf_shows.csv-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Изучим общую информацию о данных таблицы mkrf_shows.csv</a></span></li><li><span><a href="#Изучим-общую-информацию-о-данных-таблицы-mkrf_shows.csv" data-toc-modified-id="Изучим-общую-информацию-о-данных-таблицы-mkrf_shows.csv-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Изучим общую информацию о данных таблицы mkrf_shows.csv</a></span></li><li><span><a href="#Объединим-таблицы-mkrf_movies-и-mkrf_shows-в-одну-методом-merge(),-по-колонке-puNumber" data-toc-modified-id="Объединим-таблицы-mkrf_movies-и-mkrf_shows-в-одну-методом-merge(),-по-колонке-puNumber-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Объединим таблицы mkrf_movies и mkrf_shows в одну методом merge(), по колонке puNumber</a></span></li></ul></li><li><span><a href="#Предобработка-данных" data-toc-modified-id="Предобработка-данных-2"><span class="toc-item-num">2&nbsp;&nbsp;</span>Предобработка данных</a></span><ul class="toc-item"><li><span><a href="#Проверьте-типы-данных" data-toc-modified-id="Проверьте-типы-данных-2.1"><span class="toc-item-num">2.1&nbsp;&nbsp;</span>Проверьте типы данных</a></span><ul class="toc-item"><li><span><a href="#Столбец-show_start_date" data-toc-modified-id="Столбец-show_start_date-2.1.1"><span class="toc-item-num">2.1.1&nbsp;&nbsp;</span>Столбец show_start_date</a></span></li><li><span><a href="#Столбец-puNumber" data-toc-modified-id="Столбец-puNumber-2.1.2"><span class="toc-item-num">2.1.2&nbsp;&nbsp;</span>Столбец puNumber</a></span></li></ul></li><li><span><a href="#Изучим-пропуски-в-датафрейме" data-toc-modified-id="Изучим-пропуски-в-датафрейме-2.2"><span class="toc-item-num">2.2&nbsp;&nbsp;</span>Изучим пропуски в датафрейме</a></span><ul class="toc-item"><li><span><a href="#Найдем-и-изучим-пропущенные-значения-в-столбцах,-отсортировав-значения-по-убыванию,-и-визуализируем-долю-пропусков-по-столбцам-нашего-датасета" data-toc-modified-id="Найдем-и-изучим-пропущенные-значения-в-столбцах,-отсортировав-значения-по-убыванию,-и-визуализируем-долю-пропусков-по-столбцам-нашего-датасета-2.2.1"><span class="toc-item-num">2.2.1&nbsp;&nbsp;</span>Найдем и изучим пропущенные значения в столбцах, отсортировав значения по убыванию, и визуализируем долю пропусков по столбцам нашего датасета</a></span></li><li><span><a href="#Столбцы-refundable_support,-nonrefundable_support,-budget,-financing_source" data-toc-modified-id="Столбцы-refundable_support,-nonrefundable_support,-budget,-financing_source-2.2.2"><span class="toc-item-num">2.2.2&nbsp;&nbsp;</span>Столбцы refundable_support, nonrefundable_support, budget, financing_source</a></span></li><li><span><a href="#Столбец-box_office" data-toc-modified-id="Столбец-box_office-2.2.3"><span class="toc-item-num">2.2.3&nbsp;&nbsp;</span>Столбец box_office</a></span></li><li><span><a href="#Столбец-ratings" data-toc-modified-id="Столбец-ratings-2.2.4"><span class="toc-item-num">2.2.4&nbsp;&nbsp;</span>Столбец ratings</a></span></li><li><span><a href="#Столбец-genres" data-toc-modified-id="Столбец-genres-2.2.5"><span class="toc-item-num">2.2.5&nbsp;&nbsp;</span>Столбец genres</a></span></li><li><span><a href="#Столбец-producer" data-toc-modified-id="Столбец-producer-2.2.6"><span class="toc-item-num">2.2.6&nbsp;&nbsp;</span>Столбец producer</a></span></li><li><span><a href="#Столбец-director" data-toc-modified-id="Столбец-director-2.2.7"><span class="toc-item-num">2.2.7&nbsp;&nbsp;</span>Столбец director</a></span></li><li><span><a href="#Столбец-film_studio" data-toc-modified-id="Столбец-film_studio-2.2.8"><span class="toc-item-num">2.2.8&nbsp;&nbsp;</span>Столбец film_studio</a></span></li><li><span><a href="#Столбец-production_country" data-toc-modified-id="Столбец-production_country-2.2.9"><span class="toc-item-num">2.2.9&nbsp;&nbsp;</span>Столбец production_country</a></span></li></ul></li><li><span><a href="#Изучим-дубликаты-в-датафрейме" data-toc-modified-id="Изучим-дубликаты-в-датафрейме-2.3"><span class="toc-item-num">2.3&nbsp;&nbsp;</span>Изучим дубликаты в датафрейме</a></span><ul class="toc-item"><li><span><a href="#Проверим-датафрейм-на-наличие-явных-дубликатов-методом-duplicated()" data-toc-modified-id="Проверим-датафрейм-на-наличие-явных-дубликатов-методом-duplicated()-2.3.1"><span class="toc-item-num">2.3.1&nbsp;&nbsp;</span>Проверим датафрейм на наличие явных дубликатов методом duplicated()</a></span></li><li><span><a href="#Посмотрим-на-наличие-дубликатов-в-столбце-title" data-toc-modified-id="Посмотрим-на-наличие-дубликатов-в-столбце-title-2.3.2"><span class="toc-item-num">2.3.2&nbsp;&nbsp;</span>Посмотрим на наличие дубликатов в столбце title</a></span></li><li><span><a href="#Посмотрим-на-наличие-дубликатов-в-столбце-punumber" data-toc-modified-id="Посмотрим-на-наличие-дубликатов-в-столбце-punumber-2.3.3"><span class="toc-item-num">2.3.3&nbsp;&nbsp;</span>Посмотрим на наличие дубликатов в столбце punumber</a></span></li><li><span><a href="#Посмотрим-на-наличие-неявных-дубликатов-в-столбце-production_country" data-toc-modified-id="Посмотрим-на-наличие-неявных-дубликатов-в-столбце-production_country-2.3.4"><span class="toc-item-num">2.3.4&nbsp;&nbsp;</span>Посмотрим на наличие неявных дубликатов в столбце production_country</a></span></li></ul></li><li><span><a href="#Категориальные-значения" data-toc-modified-id="Категориальные-значения-2.4"><span class="toc-item-num">2.4&nbsp;&nbsp;</span>Категориальные значения</a></span></li><li><span><a href="#Проверим-количественные-значения" data-toc-modified-id="Проверим-количественные-значения-2.5"><span class="toc-item-num">2.5&nbsp;&nbsp;</span>Проверим количественные значения</a></span><ul class="toc-item"><li><span><a href="#Подсчет-средней-доли-господдержки-в-общем-бюджете-фильмов" data-toc-modified-id="Подсчет-средней-доли-господдержки-в-общем-бюджете-фильмов-2.5.1"><span class="toc-item-num">2.5.1&nbsp;&nbsp;</span>Подсчет средней доли господдержки в общем бюджете фильмов</a></span></li></ul></li><li><span><a href="#Добавление-новых-столбцов" data-toc-modified-id="Добавление-новых-столбцов-2.6"><span class="toc-item-num">2.6&nbsp;&nbsp;</span>Добавление новых столбцов</a></span><ul class="toc-item"><li><span><a href="#Посчитаем,-какую-долю-от-общего-бюджета-фильма-составляет-государственная-поддержка" data-toc-modified-id="Посчитаем,-какую-долю-от-общего-бюджета-фильма-составляет-государственная-поддержка-2.6.1"><span class="toc-item-num">2.6.1&nbsp;&nbsp;</span>Посчитаем, какую долю от общего бюджета фильма составляет государственная поддержка</a></span></li></ul></li></ul></li><li><span><a href="#Исследовательский-анализ-данных" data-toc-modified-id="Исследовательский-анализ-данных-3"><span class="toc-item-num">3&nbsp;&nbsp;</span>Исследовательский анализ данных</a></span></li><li><span><a href="#Исследование-фильмов,-получившие-государственную-поддержку" data-toc-modified-id="Исследование-фильмов,-получившие-государственную-поддержку-4"><span class="toc-item-num">4&nbsp;&nbsp;</span>Исследование фильмов, получившие государственную поддержку</a></span><ul class="toc-item"><li><span><a href="#Поищем-интересные-закономерности-в-данных.-Посмотрим,-сколько-выделяют-средств-на-поддержку-кино.-Проверим,-хорошо-ли-окупаются-такие-фильмы,-какой-у-них-рейтинг" data-toc-modified-id="Поищем-интересные-закономерности-в-данных.-Посмотрим,-сколько-выделяют-средств-на-поддержку-кино.-Проверим,-хорошо-ли-окупаются-такие-фильмы,-какой-у-них-рейтинг-4.1"><span class="toc-item-num">4.1&nbsp;&nbsp;</span>Поищем интересные закономерности в данных. Посмотрим, сколько выделяют средств на поддержку кино. Проверим, хорошо ли окупаются такие фильмы, какой у них рейтинг</a></span></li><li><span><a href="#Исследуем-поведение-окупаемости-фильмов-с-государственной-поддержкой" data-toc-modified-id="Исследуем-поведение-окупаемости-фильмов-с-государственной-поддержкой-4.2"><span class="toc-item-num">4.2&nbsp;&nbsp;</span>Исследуем поведение окупаемости фильмов с государственной поддержкой</a></span><ul class="toc-item"><li><span><a href="#Построим-график-показывающий-количество-фильмов-получивших-государственную-поддержку-по-годам" data-toc-modified-id="Построим-график-показывающий-количество-фильмов-получивших-государственную-поддержку-по-годам-4.2.1"><span class="toc-item-num">4.2.1&nbsp;&nbsp;</span>Построим график показывающий количество фильмов получивших государственную поддержку по годам</a></span></li><li><span><a href="#Какие-жанры-фильмов-оказались-наиболее-популярными-при-получении-государственной-поддержки?" data-toc-modified-id="Какие-жанры-фильмов-оказались-наиболее-популярными-при-получении-государственной-поддержки?-4.2.2"><span class="toc-item-num">4.2.2&nbsp;&nbsp;</span>Какие жанры фильмов оказались наиболее популярными при получении государственной поддержки?</a></span></li></ul></li><li><span><a href="#Посмотрим-окупаемость-фильмов-в-зависимости-от-жанров" data-toc-modified-id="Посмотрим-окупаемость-фильмов-в-зависимости-от-жанров-4.3"><span class="toc-item-num">4.3&nbsp;&nbsp;</span>Посмотрим окупаемость фильмов в зависимости от жанров</a></span></li><li><span><a href="#Рейтинг-фильмов-и-поиск-зависимостей" data-toc-modified-id="Рейтинг-фильмов-и-поиск-зависимостей-4.4"><span class="toc-item-num">4.4&nbsp;&nbsp;</span>Рейтинг фильмов и поиск зависимостей</a></span></li><li><span><a href="#Зависимость-рейтинга-от-суммы-государственной-поддержки" data-toc-modified-id="Зависимость-рейтинга-от-суммы-государственной-поддержки-4.5"><span class="toc-item-num">4.5&nbsp;&nbsp;</span>Зависимость рейтинга от суммы государственной поддержки</a></span></li></ul></li><li><span><a href="#Общий-вывод" data-toc-modified-id="Общий-вывод-5"><span class="toc-item-num">5&nbsp;&nbsp;</span>Общий вывод</a></span></li></ul></div>

# Исследование  российского кинопроката

**Описание проекта**

Заказчик исследования — Министерство культуры Российской Федерации. Мне необходимо изучить рынок российского кинопроката и выявить текущие тренды. Уделить внимание фильмам, которые получили государственную поддержку. Попробую ответить на вопрос, насколько такие фильмы интересны зрителю. Моя задача — выполнить предобработку данных и изучить их, чтобы найти интересные особенности и зависимости, которые существуют на рынке российского кинопроката. Я буду работать с данными, опубликованными на портале открытых данных Министерства культуры РФ. Набор данных содержит информацию о прокатных удостоверениях, сборах и государственной поддержке фильмов, а также информацию с сайта КиноПоиск.

**Описание данных:**

Таблица **mkrf_movies** содержит информацию из реестра прокатных удостоверений. У одного фильма может быть несколько прокатных удостоверений. Cтолбец **budget** уже включает в себя полный объём государственной поддержки. Данные в этом столбце указаны только для тех фильмов, которые получили государственную поддержку.

- **title** — название фильма;
- **puNumber** — номер прокатного удостоверения;
- **show_start_date** — дата премьеры фильма;
- **type** — тип фильма;
- **film_studio** — студия-производитель;
- **production_country** — страна-производитель;
- **director** — режиссёр;
- **producer** — продюсер;
- **age_restriction** — возрастная категория;
- **refundable_support** — объём возвратных средств государственной поддержки;
- **nonrefundable_support** — объём невозвратных средств государственной поддержки;
- **financing_source** — источник государственного финансирования;
- **budget** — общий бюджет фильма;
- **ratings** — рейтинг фильма на КиноПоиске;
- **genres** — жанр фильма.

**Таблица mkrf_shows содержит следующие сведения о показах фильмов в российских кинотеатрах:**

- **puNumber** — номер прокатного удостоверения;
- **box_office** — сборы в рублях.

**Для оптимизации рабоы по проекту составим краткий план исселования:**
1. Исследуем поступившие в наше распоряжение данные и выполним обьединение данных для удобства работы и полноты исседования данных
2. Для выявления и  устранения ошибок в данных выполним предобработку поступивших данных, следующими способами:
- проверим тип данных и приведем к единому значению;
- проверим и устраненим пропуски данных;
- изучим дубликаты данных;
- изучим категориальные данных;
- изучим количественные значений;
- добавление новых столбцов(при необходимости);
3. Проведем исседовательский анализ данных.
4. Исседование фильмов получаемых государственную поддержку.
5. В заключении опишем порядок процесса исседования и подведем красткие итоги.

## Открытие файлов с данными и объединения их в один датафрейм 



```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import sys as sy
from datetime import datetime, timedelta

pd.options.display.float_format = '{:.2f}'.format
```

### Изучим общую информацию о данных таблицы mkrf_shows.csv


```python
# загрузим данные в датасете

pd.options.display.max_columns = None

try:
    mkrf_movies = pd.read_csv('/datasets/mkrf_movies.csv')
except:
    mkrf_movies = pd.read_csv('https://code.s3.yandex.net/datasets/mkrf_movies.csv')

mkrf_movies.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>puNumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Открытый простор</td>
      <td>221048915</td>
      <td>2015-11-27T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Тачстоун Пикчерз, Кобальт Пикчерз, Бикон Пикче...</td>
      <td>США</td>
      <td>Кевин Костнер</td>
      <td>Дэвид Валдес, Кевин Костнер, Джейк Эбертс</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.2</td>
      <td>боевик,драма,мелодрама</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Особо важное задание</td>
      <td>111013716</td>
      <td>2016-09-13T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Киностудия "Мосфильм"</td>
      <td>СССР</td>
      <td>Е.Матвеев</td>
      <td>NaN</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.6</td>
      <td>драма,военный</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Особо опасен</td>
      <td>221038416</td>
      <td>2016-10-10T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Юниверсал Пикчерз, Кикстарт Продакшнз, Марк Пл...</td>
      <td>США</td>
      <td>Тимур Бекмамбетов</td>
      <td>Джим Лемли, Джейсон Нетер, Марк Е.Платт, Яйн Смит</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.8</td>
      <td>фантастика,боевик,триллер</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Особо опасен</td>
      <td>221026916</td>
      <td>2016-06-10T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Юниверсал Пикчерз, Кикстарт Продакшнз, Марк Пл...</td>
      <td>США</td>
      <td>Тимур Бекмамбетов</td>
      <td>Джим Лемли, Джейсон Нетер, Марк Е.Платт, Яйн Смит</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.8</td>
      <td>фантастика,боевик,триллер</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Особо опасен</td>
      <td>221030815</td>
      <td>2015-07-29T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Юниверсал Пикчерз, Кикстарт Продакшнз, Марк Пл...</td>
      <td>США</td>
      <td>Тимур Бекмамбетов</td>
      <td>Джим Лемли, Джейсон Нетер, Марк Е.Платт, Яйн Смит</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.8</td>
      <td>фантастика,боевик,триллер</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Остановился поезд</td>
      <td>111013816</td>
      <td>2016-09-13T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Киностудия "Мосфильм"</td>
      <td>СССР</td>
      <td>В.Абдрашитов</td>
      <td>NaN</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.7</td>
      <td>драма</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Любовь и голуби</td>
      <td>111007013</td>
      <td>2013-10-18T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Киностудия "Мосфильм"</td>
      <td>СССР</td>
      <td>В.Меньшов</td>
      <td>NaN</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>8.3</td>
      <td>мелодрама,комедия</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Любовь и сигареты</td>
      <td>221074614</td>
      <td>2014-12-29T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Юнайтед Артистс, Грин Стрит Филмз, Айкон Интер...</td>
      <td>США</td>
      <td>Джон Туртурро</td>
      <td>Джон Пенотти, Джон Туртурро</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.6</td>
      <td>мюзикл,мелодрама,комедия</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Отпетые мошенники.</td>
      <td>121011416</td>
      <td>2016-05-05T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Пульсар Продюксьон, ТФ1 Фильм</td>
      <td>Франция</td>
      <td>Эрик Беснард</td>
      <td>Патрис Леду</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>8.0</td>
      <td>комедия,криминал</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Отпуск за свой счет</td>
      <td>111019114</td>
      <td>2014-12-01T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>Киностудия "Мосфильм", Телевидение ВНР</td>
      <td>СССР, Венгрия</td>
      <td>В.Титов</td>
      <td>NaN</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.8</td>
      <td>мелодрама,комедия</td>
    </tr>
  </tbody>
</table>
</div>




```python
# получим общую информацию о данных исходной таблицы mkrf_movies, применив к ней метод info():

mkrf_movies.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 7486 entries, 0 to 7485
    Data columns (total 15 columns):
     #   Column                 Non-Null Count  Dtype  
    ---  ------                 --------------  -----  
     0   title                  7486 non-null   object 
     1   puNumber               7486 non-null   object 
     2   show_start_date        7486 non-null   object 
     3   type                   7486 non-null   object 
     4   film_studio            7468 non-null   object 
     5   production_country     7484 non-null   object 
     6   director               7477 non-null   object 
     7   producer               6918 non-null   object 
     8   age_restriction        7486 non-null   object 
     9   refundable_support     332 non-null    float64
     10  nonrefundable_support  332 non-null    float64
     11  budget                 332 non-null    float64
     12  financing_source       332 non-null    object 
     13  ratings                6519 non-null   object 
     14  genres                 6510 non-null   object 
    dtypes: float64(3), object(12)
    memory usage: 877.4+ KB
    

### Изучим общую информацию о данных таблицы mkrf_shows.csv


```python
# выведем 10 первых строк таблицы mkrf_movies

try:
    mkrf_shows = pd.read_csv('/datasets/mkrf_shows.csv')
except:
    mkrf_shows = pd.read_csv('https://code.s3.yandex.net/datasets/mkrf_shows.csv')

mkrf_shows.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>puNumber</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>111000113</td>
      <td>2450.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>111000115</td>
      <td>61040.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>111000116</td>
      <td>153030013.40</td>
    </tr>
    <tr>
      <th>3</th>
      <td>111000117</td>
      <td>12260956.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>111000118</td>
      <td>163684057.79</td>
    </tr>
    <tr>
      <th>5</th>
      <td>111000119</td>
      <td>4293649.51</td>
    </tr>
    <tr>
      <th>6</th>
      <td>111000212</td>
      <td>200.00</td>
    </tr>
    <tr>
      <th>7</th>
      <td>111000216</td>
      <td>355567.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>111000313</td>
      <td>710.00</td>
    </tr>
    <tr>
      <th>9</th>
      <td>111000314</td>
      <td>1607970.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
# получим общую информацию о данных исходной таблицы mkrf_movies, применив к ней метод info():

mkrf_shows.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 3158 entries, 0 to 3157
    Data columns (total 2 columns):
     #   Column      Non-Null Count  Dtype  
    ---  ------      --------------  -----  
     0   puNumber    3158 non-null   int64  
     1   box_office  3158 non-null   float64
    dtypes: float64(1), int64(1)
    memory usage: 49.5 KB
    

### Объединим таблицы mkrf_movies и mkrf_shows в одну методом merge(), по колонке puNumber

Объединим данные таким образом, чтобы все объекты из датасета **mkrf_movies** обязательно вошли в получившийся датафрейм. Обратим внимание, что тип данных в столбце puNumber различается у исходных датафреймов. В таблице таблицы **mkrf_movies** - это тип данных object, когда в **mkrf_shows** - это int64. Найдем строки **mkrf_movies** в которых присутствуют нецифровые символы применив логическую фильтрацию.


```python
mkrf_movies[~mkrf_movies['puNumber'].str.isdigit()]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>puNumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>804</th>
      <td>Паранормальный Якутск</td>
      <td>111004112</td>
      <td>2012-08-24T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>ИП Тимофеев К.П.</td>
      <td>Россия</td>
      <td>К.Тимофеев</td>
      <td>NaN</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1797</th>
      <td>Курбан-роман. (История с жертвой)</td>
      <td>нет</td>
      <td>2014-05-15T12:00:00.000Z</td>
      <td>Художественный</td>
      <td>ФОНД "ИННОВАЦИЯ"</td>
      <td>Россия</td>
      <td>С.Юзеев</td>
      <td>М.Галицкая</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



Можно предположить, что в строке 804 присутствуют пробелы. Для их удаления используем метод strip(). В строке 1787 значение "нет" заменим нулевым значением. Приведем эти строки к целым числам функцией to_numeric(). После замены проверим ещё раз тип данных столбца puNumber методом dtype.


```python
# заменим значение "Нет" столбца puNumber и переведём его в int64

mkrf_movies['puNumber'] = pd.to_numeric(mkrf_movies['puNumber'], errors= 'coerce')
mkrf_movies['puNumber'] = pd.to_numeric(mkrf_movies['puNumber'])
mkrf_movies.dtypes
```




    title                     object
    puNumber                 float64
    show_start_date           object
    type                      object
    film_studio               object
    production_country        object
    director                  object
    producer                  object
    age_restriction           object
    refundable_support       float64
    nonrefundable_support    float64
    budget                   float64
    financing_source          object
    ratings                   object
    genres                    object
    dtype: object



Убедившись что тип данных в обоих датафреймах совпадает, добавим в датафрейм с фильмами сведения о показах.


```python
# слияние таблиц по 'puNumber', 'puNumber' таблицы mkrf_movies включены в итоговую таблицу df
df = mkrf_movies.merge(mkrf_shows, on='puNumber', how='left')

# создадим резервную копию
df_raw = df.copy()

df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 7486 entries, 0 to 7485
    Data columns (total 16 columns):
     #   Column                 Non-Null Count  Dtype  
    ---  ------                 --------------  -----  
     0   title                  7486 non-null   object 
     1   puNumber               7485 non-null   float64
     2   show_start_date        7486 non-null   object 
     3   type                   7486 non-null   object 
     4   film_studio            7468 non-null   object 
     5   production_country     7484 non-null   object 
     6   director               7477 non-null   object 
     7   producer               6918 non-null   object 
     8   age_restriction        7486 non-null   object 
     9   refundable_support     332 non-null    float64
     10  nonrefundable_support  332 non-null    float64
     11  budget                 332 non-null    float64
     12  financing_source       332 non-null    object 
     13  ratings                6519 non-null   object 
     14  genres                 6510 non-null   object 
     15  box_office             3158 non-null   float64
    dtypes: float64(5), object(11)
    memory usage: 935.9+ KB
    

**Вывод:** 

Мы видим что все 3158 значений **box_office** были присоединены без потерь. Продолжим работу с данными.

## Предобработка данных

### Проверьте типы данных

- Проверьте типы данных в датафрейме и преобразуйте их там, где это необходимо.


```python
# выведем информацию о таблице

df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 7486 entries, 0 to 7485
    Data columns (total 16 columns):
     #   Column                 Non-Null Count  Dtype  
    ---  ------                 --------------  -----  
     0   title                  7486 non-null   object 
     1   puNumber               7485 non-null   float64
     2   show_start_date        7486 non-null   object 
     3   type                   7486 non-null   object 
     4   film_studio            7468 non-null   object 
     5   production_country     7484 non-null   object 
     6   director               7477 non-null   object 
     7   producer               6918 non-null   object 
     8   age_restriction        7486 non-null   object 
     9   refundable_support     332 non-null    float64
     10  nonrefundable_support  332 non-null    float64
     11  budget                 332 non-null    float64
     12  financing_source       332 non-null    object 
     13  ratings                6519 non-null   object 
     14  genres                 6510 non-null   object 
     15  box_office             3158 non-null   float64
    dtypes: float64(5), object(11)
    memory usage: 935.9+ KB
    

**Проверка типов данных в датасете df и последующая замена**

Проверим типы данных в датафрейме и преобразуем их там, где это необходимо. Мы видим что столбец **show_start_date** имеет тип объекта, и не является нужным нам типом даты datetime для последующего извлечения дня и месяца. Значения столбца **ratings** не являются целочисленными значениями. 

Преобразуем тип данных в выбранных столбцах следующим образом:

- **show_start_date** - тип данных object заменим на datetime. Для работы со временем необходимо привести данные в формат  
  datetime, это позволит нам получать интересующие нас параметры в будущем.
- **ratings - object заменим на float64** - так как рейтинг на Кинопоиске проходит по 10-балльной шкале, где 1 — это ужас, а 10 — шедевр. Также посмотрим уникальные значения рейтинга для проверки если есть значения включающие в себя не только цифры иточку.
- **puNumber** - приведем название данного столбца к нижнему регистру.

#### Столбец show_start_date


```python
# тип данных столбца 'show_start_date'

df['show_start_date'] = pd.to_datetime(df['show_start_date'],format='%Y-%m-%dT%H:%M:%S.%fZ', utc=True)
(df['show_start_date'].head(5))
```




    0   2015-11-27 12:00:00+00:00
    1   2016-09-13 12:00:00+00:00
    2   2016-10-10 12:00:00+00:00
    3   2016-06-10 12:00:00+00:00
    4   2015-07-29 12:00:00+00:00
    Name: show_start_date, dtype: datetime64[ns, UTC]




```python
# выведем уникальные значения столбца 'ratings'

df['ratings'].unique()
```




    array(['7.2', '6.6', '6.8', '7.7', '8.3', '8.0', '7.8', '8.1', '7.1',
           '6.0', '7.4', '5.8', '8.7', '6.3', '6.9', '5.0', '4.3', '7.3',
           '7.0', '6.4', nan, '8.2', '7.5', '6.7', '7.9', '5.9', '6.2', '5.6',
           '6.5', '2.4', '7.6', '6.1', '8.6', '8.5', '8.8', '5.5', '5.1',
           '5.7', '5.4', '99%', '4.4', '4.5', '5.3', '4.1', '8.4', '2.6',
           '3.8', '4.6', '4.8', '4.0', '3.0', '1.6', '4.2', '5.2', '4.7',
           '4.9', '3.9', '2.7', '3.3', '2.9', '28%', '3.7', '1.4', '3.1',
           '97%', '3.5', '3.2', '2.8', '1.5', '2.1', '2.5', '9.2', '3.4',
           '1.1', '3.6', '83%', '64%', '91%', '94%', '62%', '79%', '90%',
           '19%', '88%', '1.0', '89%', '1.3', '1.9', '1.8', '1.2', '1.7',
           '9.0', '98%', '8.9', '9.1'], dtype=object)



Часть данных представлена в формате процентов, но для рейтингов Кинопоиска официально используют десятибальную систему. Выведем фильмы с рейтингом представленных в процентах.


```python
# создадим список где значения рейтинга представлена в процентах

unk_ratings = ['99%', '28%', '97%','83%', '64%',
                  '91%', '94%', '62%', '79%', '90%',
                  '19%', '88%', '89%', '98%']
```


```python
# используем фильтрацию при помощи метода query и сортируем по возрастанию рейтинга

df.query('ratings in @unk_ratings').sort_values(by='ratings')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>puNumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3431</th>
      <td>Наурыз</td>
      <td>131000217.00</td>
      <td>2017-03-09 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Эс Джи</td>
      <td>Республика Казахстан</td>
      <td>Аскар Бисембин</td>
      <td>Олег Головашкин, Алмас Султангазин</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>19%</td>
      <td>комедия</td>
      <td>37960.00</td>
    </tr>
    <tr>
      <th>811</th>
      <td>От винта!</td>
      <td>114000212.00</td>
      <td>2012-08-06 12:00:00+00:00</td>
      <td>Анимационный</td>
      <td>ЗАО "Продюсерский центр "Парадиз"</td>
      <td>Россия</td>
      <td>О.Лопато</td>
      <td>Г.Нерсисян, А.Манасарян, А.Нерсесян</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>28%</td>
      <td>детский,приключения,комедия</td>
      <td>1740.00</td>
    </tr>
    <tr>
      <th>2438</th>
      <td>Самый рыжий Лис</td>
      <td>111012715.00</td>
      <td>2015-07-30 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Продюсерский центр "Ленфильм"</td>
      <td>Россия</td>
      <td>А.Стреляная</td>
      <td>А.Котелевский, Э.Пичугин</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>62%</td>
      <td>фэнтези,семейный</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1899</th>
      <td>Золушка /По сказке Шарля Перро/. Холодное торж...</td>
      <td>121003615.00</td>
      <td>2015-02-27 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Женр Филмз, Уолт Дисней Пикчерз</td>
      <td>США</td>
      <td>Кеннет Брана</td>
      <td>Дэвид Бэррон, Саймон Кинберг, Эллисон Ширмур</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>64%</td>
      <td>мюзикл,фэнтези,мелодрама</td>
      <td>528732557.70</td>
    </tr>
    <tr>
      <th>7159</th>
      <td>Анна Каренина. Интимный дневник</td>
      <td>111013919.00</td>
      <td>2019-10-23 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "РТВ"</td>
      <td>Россия</td>
      <td>Ю.Грымов</td>
      <td>Ю.Грымов</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>79%</td>
      <td>драма</td>
      <td>182882.50</td>
    </tr>
    <tr>
      <th>2680</th>
      <td>Год Белого Слона</td>
      <td>111003915.00</td>
      <td>2015-04-08 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Творческое объединение ЮГ"</td>
      <td>Россия</td>
      <td>Ю.Грымов</td>
      <td>П.Поляков</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>79%</td>
      <td>семейный</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3446</th>
      <td>Короткие истории о любви - 4</td>
      <td>126006316.00</td>
      <td>2016-12-30 12:00:00+00:00</td>
      <td>Прочие</td>
      <td>Нетворг Айлэнд Телевижн, Магнетфильм, Шорткатс...</td>
      <td>Великобритания - Аргентина - США - Франция - Р...</td>
      <td>Д.Адар, П.Антохин, М.Биасин, А.Бурунова, К.Кол...</td>
      <td>Д.Адар, Д.Амсон, П.Антохин, А.Армстронг, С.Бил...</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>83%</td>
      <td>NaN</td>
      <td>2266408.00</td>
    </tr>
    <tr>
      <th>5455</th>
      <td>Вечный холод</td>
      <td>111006417.00</td>
      <td>2017-08-28 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ЗАО "Производственный комплекс "ГЛАВКИНО", ООО...</td>
      <td>Россия</td>
      <td>А.Мигачев</td>
      <td>И.Бачурин</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>83%</td>
      <td>фэнтези,боевик,триллер</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1874</th>
      <td>Короткие истории о любви 2</td>
      <td>121002615.00</td>
      <td>2015-02-13 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Кавиар, Курт 13, СтритЛайт Филмз, Нэйер Дойче ...</td>
      <td>Нидерланды - США - Германия - Канада - Франция...</td>
      <td>Мэтью Аувро, Лео Брайдл, Бен Бренд, Ден Кларк,...</td>
      <td>Мэри Пэт Бентел, Бен Бренд, Сиара Гиллан, Джор...</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>83%</td>
      <td>NaN</td>
      <td>1429859.00</td>
    </tr>
    <tr>
      <th>5332</th>
      <td>Добыча.</td>
      <td>121009411.00</td>
      <td>2011-06-15 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Афтер Дарк Филмз</td>
      <td>США</td>
      <td>Патрик Сиверсен</td>
      <td>Закари Ти Брайан, Кристофер</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>88%</td>
      <td>фантастика,боевик,триллер</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3439</th>
      <td>Семь диких историй</td>
      <td>126005916.00</td>
      <td>2016-11-28 12:00:00+00:00</td>
      <td>Прочие</td>
      <td>Макс Бэйкер, Джон Е.Брайан, Пьер-Луи Гарнон,  ...</td>
      <td>США - Пуэрто-Рико - Франция</td>
      <td>М.Бэйкер, Д.Е.Брайант, Д.Рондот, Я.Серсар, Д.С...</td>
      <td>М.Бэйкер, Д.Е.Брайан, П.-Л.Гарнон, М.Х.Дельгад...</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>88%</td>
      <td>NaN</td>
      <td>1025937.00</td>
    </tr>
    <tr>
      <th>7277</th>
      <td>Добыча</td>
      <td>121028319.00</td>
      <td>2019-10-03 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Блумхаус Продакшнз, Хайд Парк Интертейнмент, Т...</td>
      <td>США</td>
      <td>Франк Халфун</td>
      <td>Ашок Амритрадж, Джейсон Блум, Трэвис Клафф</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>88%</td>
      <td>фантастика,боевик,триллер</td>
      <td>4416590.45</td>
    </tr>
    <tr>
      <th>3786</th>
      <td>Охотники</td>
      <td>111017816.00</td>
      <td>2016-02-06 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Селиверстов Александр Александрович</td>
      <td>Россия</td>
      <td>А.Селиверстов</td>
      <td>Е.Тарковская, Т.Лагода, Д.Степанян</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>89%</td>
      <td>фантастика,комедия,боевик</td>
      <td>82840.00</td>
    </tr>
    <tr>
      <th>3139</th>
      <td>Я умею вязать</td>
      <td>111019615.00</td>
      <td>2015-11-27 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Белое Зеркало"</td>
      <td>Россия</td>
      <td>Н.Степанова при участии С.Иванова</td>
      <td>С.Кикнавелидзе, Д.Улюкаев</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>4700000.00</td>
      <td>14462464.00</td>
      <td>Министерство культуры</td>
      <td>90%</td>
      <td>драма</td>
      <td>801370.00</td>
    </tr>
    <tr>
      <th>2126</th>
      <td>Поездка к матери</td>
      <td>111002015.00</td>
      <td>2015-03-02 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ЗАО "Киностудия "М"-Фильм"</td>
      <td>Россия</td>
      <td>М.Косырев-Нестеров</td>
      <td>М.Косырев-Нестеров</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>91%</td>
      <td>драма,семейный</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>6426</th>
      <td>Памятные даты России. Партизаны и подпольщики</td>
      <td>112013018.00</td>
      <td>2018-11-28 12:00:00+00:00</td>
      <td>Документальный</td>
      <td>ООО Кинокомпания "Вектор"</td>
      <td>Россия</td>
      <td>Н.Иванова, А.Кузнецова</td>
      <td>В.Коханович</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>91%</td>
      <td>драма,биография</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3514</th>
      <td>Чужой дом</td>
      <td>111015516.00</td>
      <td>2016-09-14 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Лига Продакшн"</td>
      <td>Россия, Грузия, Хорватия, Испания</td>
      <td>Р.Глурджидзе</td>
      <td>З.Магалашвили, К.Гечмен-Вальдек, Н.Горшкова</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>91%</td>
      <td>драма</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2146</th>
      <td>Главный</td>
      <td>111003415.00</td>
      <td>2015-03-27 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Киностудия "МАСТЕР"</td>
      <td>Россия</td>
      <td>Ю.Кара</td>
      <td>Ю.Кара</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>0.00</td>
      <td>10000000.00</td>
      <td>40000000.00</td>
      <td>Министерство культуры</td>
      <td>94%</td>
      <td>фантастика,боевик,комедия</td>
      <td>334750.00</td>
    </tr>
    <tr>
      <th>5910</th>
      <td>Мира</td>
      <td>112000118.00</td>
      <td>2018-06-04 12:00:00+00:00</td>
      <td>Документальный</td>
      <td>ООО "Компания "Новые люди"</td>
      <td>Россия</td>
      <td>Д.Шабаев</td>
      <td>Н.Мокрицкая</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>94%</td>
      <td>драма</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5821</th>
      <td>Свинья</td>
      <td>121007018.00</td>
      <td>2018-04-11 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Дарк Прекёрсор Продакшен, Филмиран, Хедейт Филм</td>
      <td>Иран</td>
      <td>Мани Хагиги</td>
      <td>Мани Хагиги</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>94%</td>
      <td>триллер,драма</td>
      <td>1587221.51</td>
    </tr>
    <tr>
      <th>1053</th>
      <td>Песочный человек</td>
      <td>121029212.00</td>
      <td>2012-11-29 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Спотлайт Медиа Продакшн</td>
      <td>Швейцария</td>
      <td>Питер Луизи</td>
      <td>Дэвид Луизи, Питер Луизи</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>97%</td>
      <td>ужасы,фантастика,фэнтези</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3948</th>
      <td>Круиз.</td>
      <td>211038210.00</td>
      <td>2010-09-03 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "ЮНАЙТЕД МУЛЬТИМЕДИА ПРОДЖЕКТС"</td>
      <td>Россия</td>
      <td>И.Ромащенко</td>
      <td>Р.Атамалибеков</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>97%</td>
      <td>приключения,комедия,фэнтези</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3585</th>
      <td>Машины Страшилки. Серия "Жутчайшая повесть о п...</td>
      <td>114003916.00</td>
      <td>2016-12-09 12:00:00+00:00</td>
      <td>Анимационный</td>
      <td>ООО Студия "АНИМАККОРД", АНИМАККОРД ЛТД.</td>
      <td>Россия, Республика Кипр</td>
      <td>Д.Червяцов</td>
      <td>Д.Ловейко, О.Кузовков</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>97%</td>
      <td>мультфильм,ужасы,фэнтези</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6616</th>
      <td>ОТ ВОЙНЫ ДО НАШИХ ДНЕЙ</td>
      <td>111026518.00</td>
      <td>2019-01-21 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ИП Вайсман Анатолий Александрович</td>
      <td>Россия</td>
      <td>А.Сазонов, Е.Климович, А.Коломеец, С.Черникова...</td>
      <td>Д.Руюежин, Л.Пятницкая, Д.Колеров, Э.Ким, А.Хомич</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>98%</td>
      <td>фантастика,боевик</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6737</th>
      <td>Колесо времени</td>
      <td>111003219.00</td>
      <td>2019-03-01 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "БестМедиа"</td>
      <td>Россия</td>
      <td>Б.Куломзин</td>
      <td>Б.Куломзин</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>98%</td>
      <td>фэнтези,приключения</td>
      <td>34992.00</td>
    </tr>
    <tr>
      <th>1805</th>
      <td>Спираль.</td>
      <td>111001014.00</td>
      <td>2014-01-30 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Компания Питон"</td>
      <td>Россия</td>
      <td>А.Волгин</td>
      <td>Е.Ковалева</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>99%</td>
      <td>аниме,мультфильм,ужасы</td>
      <td>4295.00</td>
    </tr>
    <tr>
      <th>6882</th>
      <td>Животные рядом со Святыми</td>
      <td>112003719.00</td>
      <td>2019-05-03 12:00:00+00:00</td>
      <td>Документальный</td>
      <td>ООО "Кинопрограмма "XXI век"</td>
      <td>Россия</td>
      <td>Т.Мирошник</td>
      <td>В.Есинов, Е.Калинина</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>99%</td>
      <td>криминал,драма</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1341</th>
      <td>Сказка о добре и Вре</td>
      <td>111008913.00</td>
      <td>2013-11-15 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>НП "Студия игрового кино "Лик"</td>
      <td>Россия</td>
      <td>Е.Шиляева</td>
      <td>К.Терещенко</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>99%</td>
      <td>триллер,драма,детектив</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>259</th>
      <td>Прошлое</td>
      <td>221030715.00</td>
      <td>2015-07-29 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>20 Сенчюри Фокс де Архентина, Чемо, ЭйчБи Филм...</td>
      <td>Аргентина - Бразилия</td>
      <td>Эктор Бабенко</td>
      <td>Эктор Бабенко, Оскар Крамер, Хуго Сидмэн</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>99%</td>
      <td>ужасы,триллер,драма</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



После ручного поиска данных фильмов на сайте Кинопоиска (https://www.kinopoisk.ru/) можно заметить, что на момент формирования данных для них было недостаточно оценок, рейтинг формируется. Заменим значения рейтингов данных картин на NaN и преобразуем значения в тип данных с плавающей точкой методом to_numeric.


```python
# находим строки где значения рейтингов представлены в процентах

df.loc[df['ratings'].isin(unk_ratings), 'ratings'] = np.nan
df['ratings'] = pd.to_numeric(df['ratings'])

# проверим замененные значения

df['ratings'].unique()
```




    array([7.2, 6.6, 6.8, 7.7, 8.3, 8. , 7.8, 8.1, 7.1, 6. , 7.4, 5.8, 8.7,
           6.3, 6.9, 5. , 4.3, 7.3, 7. , 6.4, nan, 8.2, 7.5, 6.7, 7.9, 5.9,
           6.2, 5.6, 6.5, 2.4, 7.6, 6.1, 8.6, 8.5, 8.8, 5.5, 5.1, 5.7, 5.4,
           4.4, 4.5, 5.3, 4.1, 8.4, 2.6, 3.8, 4.6, 4.8, 4. , 3. , 1.6, 4.2,
           5.2, 4.7, 4.9, 3.9, 2.7, 3.3, 2.9, 3.7, 1.4, 3.1, 3.5, 3.2, 2.8,
           1.5, 2.1, 2.5, 9.2, 3.4, 1.1, 3.6, 1. , 1.3, 1.9, 1.8, 1.2, 1.7,
           9. , 8.9, 9.1])



#### Столбец puNumber


```python
# приведем данный столбец к нижнему регистру.

df.columns = df.columns.str.lower()
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 7486 entries, 0 to 7485
    Data columns (total 16 columns):
     #   Column                 Non-Null Count  Dtype              
    ---  ------                 --------------  -----              
     0   title                  7486 non-null   object             
     1   punumber               7485 non-null   float64            
     2   show_start_date        7486 non-null   datetime64[ns, UTC]
     3   type                   7486 non-null   object             
     4   film_studio            7468 non-null   object             
     5   production_country     7484 non-null   object             
     6   director               7477 non-null   object             
     7   producer               6918 non-null   object             
     8   age_restriction        7486 non-null   object             
     9   refundable_support     332 non-null    float64            
     10  nonrefundable_support  332 non-null    float64            
     11  budget                 332 non-null    float64            
     12  financing_source       332 non-null    object             
     13  ratings                6490 non-null   float64            
     14  genres                 6510 non-null   object             
     15  box_office             3158 non-null   float64            
    dtypes: datetime64[ns, UTC](1), float64(6), object(9)
    memory usage: 935.9+ KB
    

**Вывод:** 

Изначально некоторые типы данных в столбцах не соответствовали правильным типам. Мы привели данные к нужным нам для дальнейшей работы типам данных, используя несколько классических инструментов для предобработки. Также исправили стиль столбца puNumber с помощью применения нижнего регистра.

### Изучим пропуски в датафрейме

#### Найдем и изучим пропущенные значения в столбцах, отсортировав значения по убыванию, и визуализируем долю пропусков по столбцам нашего датасета


```python
# выведем количество пропусков в датасете

df.isna().sum().sort_values(ascending=False)
```




    refundable_support       7154
    nonrefundable_support    7154
    budget                   7154
    financing_source         7154
    box_office               4328
    ratings                   996
    genres                    976
    producer                  568
    film_studio                18
    director                    9
    production_country          2
    punumber                    1
    title                       0
    show_start_date             0
    type                        0
    age_restriction             0
    dtype: int64




```python
# используем удобный для визуалиции стиль и настроим параметры сетки, цвета и размера шрифта

plt.style.use('ggplot')

# среднее пропущенных значений с сортировкой по убыванию

df.isna().mean().sort_values(ascending=False).plot(
    kind='bar', figsize=(14,4), 
    grid=True, color='midnightblue', 
    edgecolor='black', linewidth=1,
)
plt.title('Визуализация пропусков по столбцам датасета',fontsize=14, fontweight="bold")
plt.xlabel('Название столбца',fontweight="bold")
plt.ylabel('Доля пропусков', fontweight="bold")
plt.show()
```


    
![png](output_41_0.png)
    


#### Столбцы refundable_support, nonrefundable_support, budget, financing_source


```python
print('Доля пропусков по столбцу "budget": {:.2%}'.format(df['budget'].isna().mean()))
```

    Доля пропусков по столбцу "budget": 95.57%
    

**Вывод**

Пропущена значительная часть данных в столбцах **refundable_support**, **nonrefundable_support**, **budget**, **financing_source**. В описании данных указано, что столбец **budget** уже включает в себя полный объём государственной поддержки. Данные в этом столбце указаны только для тех фильмов, которые получили государственную поддержку. Замену пропусков или их удаление производить не будем, т. к. доля пропусков по этим столбцам велика и приведет к искажению при анализе данных. Можем предположить, что пропуски в данных вызваны тем, что большинство фильмов нашего датасета не получило государственной поддержки. Это могли быть как картины производства России так и зарубежных стран.

#### Столбец box_office

Данные значений **box_office** были получены из другой таблицы, которая содержала сведения о показах лишь определенных фильмов в российских кинотеатрах и имела количество 3158 значений. Соответственно, не все фильмы нашего датасета будут иметь сведения о сборах. Оставим пропущенные значения без каких-либо изменений.

#### Столбец ratings


```python
print('Доля пропусков по столбцу "ratings": {:.2%}'.format(df['ratings'].isna().mean()))
```

    Доля пропусков по столбцу "ratings": 13.30%
    


```python
df.loc[df['ratings'].isna() == True].sample(8)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3140</th>
      <td>Маша и Медведь. Серия "В гостях у сказки"</td>
      <td>124004415.00</td>
      <td>2015-12-17 12:00:00+00:00</td>
      <td>Анимационный</td>
      <td>Анимаккорд Лтд</td>
      <td>Республика Кипр</td>
      <td>Андрей Беляев</td>
      <td>Олег Кузовков, Дмитрий Ловейко, Марина Ратина</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6000.00</td>
    </tr>
    <tr>
      <th>2549</th>
      <td>"Бежин луг" Сергея Эйзенштейна</td>
      <td>112000115.00</td>
      <td>2015-04-23 12:00:00+00:00</td>
      <td>Документальный</td>
      <td>Киностудия "Мосфильм"</td>
      <td>СССР</td>
      <td>С.Эйзенштейна</td>
      <td>NaN</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5275</th>
      <td>Шарль Гуно. Ромео и Джульетта /По одноименной ...</td>
      <td>126000711.00</td>
      <td>2011-03-25 12:00:00+00:00</td>
      <td>Прочие</td>
      <td>Р А И Синема</td>
      <td>Италия</td>
      <td>Бартлетт Шер</td>
      <td>Зальцбургский фестиваль</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6343</th>
      <td>Остров информатики</td>
      <td>112010918.00</td>
      <td>2018-10-01 12:00:00+00:00</td>
      <td>Документальный</td>
      <td>Наумов Виктор Борисович</td>
      <td>Россия</td>
      <td>М.Якубсон</td>
      <td>И.Викторова</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3331</th>
      <td>Одарённая</td>
      <td>121007717.00</td>
      <td>2017-04-27 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ХХ век Фокс, Фокс Сёрчлайт Пикчерз</td>
      <td>США</td>
      <td>Марк Уэбб</td>
      <td>Энди Коэн, Карен Ландер</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>19174428.00</td>
    </tr>
    <tr>
      <th>3478</th>
      <td>Мастерская</td>
      <td>111003417.00</td>
      <td>2017-05-17 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ОЧУ ДПО "Академия кинематографического и театр...</td>
      <td>Россия</td>
      <td>В.Алеников</td>
      <td>ОЧУ ДПО "Академия кинематографического и театр...</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4860</th>
      <td>4.3.2.1.</td>
      <td>121000911.00</td>
      <td>2011-01-28 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Анстопэбл Интертейнмент, Ретро-джус Продакшнз,...</td>
      <td>Великобритания</td>
      <td>Марк Дэвис, Ноэль Кларк</td>
      <td>Дэймон Брайан, Йоко Лайтл, Джастин Лэнчбери, С...</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1902</th>
      <td>Правд. Цель 102</td>
      <td>111001915.00</td>
      <td>2015-03-02 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Соколов Николай Никонорович</td>
      <td>Россия</td>
      <td>О.Джураев</td>
      <td>Н.Соколов</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



После ручного поиска фильмов с пропущенными значениями в рейтингах на сайте Кинопоиска (https://www.kinopoisk.ru/) можно предположить, что на момент формирования наших исходных данных для фильмов было недостаточное количество оценок, и тем самым рейтинг находился в процессе формирования. Исходя из информации Кинопоиск начинает проставлять рейтинг фильмам, которые набрали более 100 оценок. Мы не можем каким-либо образом заменить пропущенные значения рейтингов, и удалять их не будем, так как доля пропусков существенна и может исказить наш анализ.

#### Столбец genres


```python
print('Доля пропусков по столбцу "genres": {:.2%}'.format(df['genres'].isna().mean()))
```

    Доля пропусков по столбцу "genres": 13.04%
    

Данные категориальные значения будут использоваться нами для создания нового столбца, поэтому для удобства заменим пропуски в данных столбца genre на значения "unknown" методом fillna. При необходимости восстановить пропущенные значения можно было бы воспользовавшись ручным поиском по каждому фильму.


```python
df['genres'] = df['genres'].fillna(value='unknown')
```

#### Столбец producer


```python
print('Доля пропусков по столбцу "producer": {:.2%}'.format(df['producer'].isna().mean()))
```

    Доля пропусков по столбцу "producer": 7.59%
    

Данные из указанного столбца не используются в нашем анализе. Нам нет необходимости определять взаимосвязь между продюсером картины и каких-либо других характеристик, поэтому необходимости заменять пропущенные значения нет. При необходимости восстановить пропущенные значения можно было бы воспользовавшись ручным поиском по каждому фильму.

#### Столбец director


```python
print('Доля пропусков по столбцу "director": {:.2%}'.format(df['director'].isna().mean()))
```

    Доля пропусков по столбцу "director": 0.12%
    

Доля пропусков минимальна. Нам предстоит последующая работа со значениями из данного столбца. Для удобства можем произвести замену пропущенных категориальных значений на "unknown" методом fillna. При необходимости восстановить пропущенные значения можно было бы воспользовавшись ручным поиском по каждому фильму.


```python
df['director'] = df['director'].fillna(value='unknown')
```

#### Столбец film_studio


```python
print('Доля пропусков по столбцу "film_studio": {:.2%}'.format(df['film_studio'].isna().mean()))
```

    Доля пропусков по столбцу "film_studio": 0.24%
    


Доля пропусков минимальна. Данные из указанного столбца не используются в нашем анализе. Оставим пропуски без изменений

#### Столбец production_country


```python
df.loc[df['production_country'].isna() == True]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3186</th>
      <td>Детский юмористический киножурнал "Ералаш. Ну ...</td>
      <td>111001216.00</td>
      <td>2016-02-09 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Продюсерский центр ЕРАЛАШ"</td>
      <td>NaN</td>
      <td>Р.Светлов, И.Магитон, А.Арутюнян, Л.Мирский, А...</td>
      <td>ООО "Продюсерский центр ЕРАЛАШ"</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.20</td>
      <td>детский,комедия</td>
      <td>194527.00</td>
    </tr>
    <tr>
      <th>4441</th>
      <td>Мульт личности. Выпуск 5</td>
      <td>214000410.00</td>
      <td>2010-01-25 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>unknown</td>
      <td>NaN</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.00</td>
      <td>мультфильм,комедия</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



В данном столбце всего 2 пропуска. После ручного поиска картины на сайте Кинопоиск, выясняем, что обе картины производства России. Сделаем необходимую замену.


```python
df.loc[df['production_country'].isna() == True, 'production_country'] = 'Россия'
df.loc[[4441, 3186]]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4441</th>
      <td>Мульт личности. Выпуск 5</td>
      <td>214000410.00</td>
      <td>2010-01-25 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>NaN</td>
      <td>Россия</td>
      <td>unknown</td>
      <td>NaN</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.00</td>
      <td>мультфильм,комедия</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3186</th>
      <td>Детский юмористический киножурнал "Ералаш. Ну ...</td>
      <td>111001216.00</td>
      <td>2016-02-09 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Продюсерский центр ЕРАЛАШ"</td>
      <td>Россия</td>
      <td>Р.Светлов, И.Магитон, А.Арутюнян, Л.Мирский, А...</td>
      <td>ООО "Продюсерский центр ЕРАЛАШ"</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.20</td>
      <td>детский,комедия</td>
      <td>194527.00</td>
    </tr>
  </tbody>
</table>
</div>



### Изучим дубликаты в датафрейме
- Проверьте, есть ли в данных дубликаты. Опишите причины, которые могли повлиять на появление дублей.

#### Проверим датафрейм на наличие явных дубликатов методом duplicated()


```python
print('Количество явных дубликатов:', df.duplicated().sum())
```

    Количество явных дубликатов: 0
    

#### Посмотрим на наличие дубликатов в столбце title


```python
# выведем первые 10 значений отсортировав по названию фильма

df[df['title'].duplicated(keep=False)].sort_values(by='title').head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>455</th>
      <td>100 миллионов евро</td>
      <td>121013712.00</td>
      <td>2012-06-06 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Патэ, Эсквуд, Серенити Фильм, ТФ1 Фильм Продюк...</td>
      <td>Франция</td>
      <td>Оливер Барру</td>
      <td>Ричард Грандпьерр</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.10</td>
      <td>комедия</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>454</th>
      <td>100 миллионов евро</td>
      <td>221024616.00</td>
      <td>2016-05-25 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Патэ, Эсквуд, Серенити Фильм, ТФ1 Фильм Продюк...</td>
      <td>Франция</td>
      <td>Оливер Барру</td>
      <td>Ричард Грандпьерр</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.10</td>
      <td>комедия</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4852</th>
      <td>127 часов</td>
      <td>121000811.00</td>
      <td>2011-01-27 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Фокс Серчлайт Пикчерз, Клод Эйт Филмз, Филм Фо...</td>
      <td>США - Великобритания</td>
      <td>Дэнни Бойл</td>
      <td>Бернард Беллью, Тесса Росс, Гаррет Смит</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.70</td>
      <td>триллер,биография,драма</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5058</th>
      <td>127 часов</td>
      <td>221069011.00</td>
      <td>2011-05-18 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Фокс Серчлайт Пикчерз, Клод Эйт Филмз, Филм Фо...</td>
      <td>США - Великобритания</td>
      <td>Дэнни Бойл</td>
      <td>Бернард Беллью, Тесса Росс, Гаррет Смит</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.70</td>
      <td>триллер,биография,драма</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3129</th>
      <td>13 часов: Тайные солдаты Бенгази</td>
      <td>221019616.00</td>
      <td>2016-04-19 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Парамаунт, Дан Филмз, Латина Пикчарз,3 Арт Инт...</td>
      <td>США</td>
      <td>Майкл Бэй</td>
      <td>Майкл Бэй, Эрвин Стофф</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.70</td>
      <td>боевик,триллер,драма</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3130</th>
      <td>13 часов: Тайные солдаты Бенгази</td>
      <td>121001016.00</td>
      <td>2016-01-15 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Парамаунт, Дан Филмз, Латина Пикчарз,3 Арт Инт...</td>
      <td>США</td>
      <td>Майкл Бэй</td>
      <td>Майкл Бэй, Эрвин Стофф</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.70</td>
      <td>боевик,триллер,драма</td>
      <td>18439240.55</td>
    </tr>
    <tr>
      <th>1494</th>
      <td>13-й район: Кирпичные особняки</td>
      <td>121008314.00</td>
      <td>2014-04-25 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Брик Мэншэнс Продакшнз,Синэ+ Канал+, Д8, Европ...</td>
      <td>Франция-Канада</td>
      <td>Камиль Деламарр</td>
      <td>Люк Бессон, Клод Леже, Джонатан Вэнджер</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5.50</td>
      <td>боевик,криминал</td>
      <td>750.00</td>
    </tr>
    <tr>
      <th>1493</th>
      <td>13-й район: Кирпичные особняки</td>
      <td>221033314.00</td>
      <td>2014-08-20 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Брик Мэншэнс Продакшнз,Синэ+ Канал+, Д8, Европ...</td>
      <td>Франция-Канада</td>
      <td>Камиль Деламарр</td>
      <td>Люк Бессон, Клод Леже, Джонатан Вэнджер</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5.50</td>
      <td>боевик,криминал</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4107</th>
      <td>13.</td>
      <td>221123710.00</td>
      <td>2010-10-25 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Барбариан Филмз, Магнет Медиа Групп, Морабито ...</td>
      <td>США</td>
      <td>Гела Баблуани</td>
      <td>NaN</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.80</td>
      <td>триллер,драма,криминал</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4307</th>
      <td>13.</td>
      <td>121018110.00</td>
      <td>2010-09-30 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Барбариан Филмз, Магнет Медиа Групп, Морабито ...</td>
      <td>США</td>
      <td>Гела Баблуани</td>
      <td>NaN</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.80</td>
      <td>триллер,драма,криминал</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



Наличие дубликатов в данных названий фильмов может быть обусловлено тем, что у одного фильма может быть несколько прокатных удостоверений. Данная специфика была указана изначально в описании данных. Так один и тот же фильм могут начать показывать в разное время под разной лицензией и/или разными прокатчиками. Данные дубликаты удалять не стоит.

#### Посмотрим на наличие дубликатов в столбце punumber


```python
df[df['punumber'].duplicated(keep=False)]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4638</th>
      <td>Как жениться и остаться холостым</td>
      <td>221154310.00</td>
      <td>2010-12-17 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Ше Вам, Скрипт Ассосье, Тэ Фэ 1 Фильм Продюксь...</td>
      <td>Франция</td>
      <td>Эрик Лартиго</td>
      <td>Амандин Било, Алан Шаба</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.00</td>
      <td>мелодрама,комедия</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4639</th>
      <td>Иоанна - женщина на папском престоле /По роман...</td>
      <td>221154310.00</td>
      <td>2010-12-17 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Константин Фильм, А Эр Ди Дегето Фильм, Дюне ...</td>
      <td>Германия - Великобритания - Италия - Испания</td>
      <td>Зенке Вортманн</td>
      <td>Оливер Бербен, Дорис Д.Хайнце, Фарук Элтан</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.60</td>
      <td>драма,мелодрама,история</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5067</th>
      <td>Анализируй это!</td>
      <td>221054410.00</td>
      <td>2010-05-25 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Уорнер Бразерс, Вилладж Роудшоу Филмз ЛТД</td>
      <td>США-Австралия</td>
      <td>ХЭрольд Рэмис</td>
      <td>Джейн Розенталь, Пола Уейнстейн</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.40</td>
      <td>комедия,криминал</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5068</th>
      <td>Анализируй то!</td>
      <td>221054410.00</td>
      <td>2010-05-25 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Уорнер Бразерс, Виллидж Роадшоу Пикчерз, Эн-Пи...</td>
      <td>США</td>
      <td>Гарольд Реймис</td>
      <td>Джейн Розенталь, Паул Уэйнстейн</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.80</td>
      <td>комедия,криминал</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



Под одним номером прокатного удостоверения числятся два разных фильма с идентичной датой премьеры. Возможно сыграл человеческий фактор при заполнении данных. Номер прокатного удостоверения не имеет принципиального значения для нашего анализа, поэтому принимаем решение оставить эти дубликаты как есть.

#### Посмотрим на наличие неявных дубликатов в столбце production_country


```python
# для удобства визуализации выведем результат уникальных значений столбца списком

sorted(df['production_country'].unique().tolist())
```




    [' СССР',
     ' СССР ',
     ' СССР   ',
     '2019',
     'CША',
     'Австралия',
     'Австралия - Великобритания - Бельгия - Индия',
     'Австралия - Германия',
     'Австралия - Ирландия',
     'Австралия - Колумбия',
     'Австралия - США',
     'Австралия, Канада',
     'Австралия, США',
     'Австралия-Великобритания',
     'Австралия-Ирландия',
     'Австралия-США',
     'Австралия-Турция-США',
     'Австрия',
     'Австрия - Германия',
     'Австрия - Германия - Франция',
     'Австрия - Люксембург',
     'Австрия, Великобритания, Германия',
     'Австрия-Германия-Франция',
     'Австрия-Франция-Германия',
     'Азербайджан-Россия',
     'Аргентина',
     'Аргентина - Бразилия',
     'Аргентина - Испания',
     'Аргентина - Испания - Уругвай',
     'Аргентина - Мексика - Бразилия - Франция - США',
     'Аргентина - Уругвай - Россия - Германия - Франция - Нидерланды',
     'Аргентина - Франция - Испания',
     'Аргентина, Испания',
     'Аргентина-Испания',
     'Армения',
     'Армения - Германия',
     'Армения - Казахстан',
     'Армения-Россия',
     'Бельгия',
     'Бельгия - Германия - Люксембург',
     'Бельгия - Германия - Люксембург - Франция',
     'Бельгия - Испания - Канада - Нидерланды',
     'Бельгия - Италия - Франция ',
     'Бельгия - Люксембург',
     'Бельгия - Люксембург - Франция - Швейцария',
     'Бельгия - Нидерланды - Франция',
     'Бельгия - США',
     'Бельгия - Франция',
     'Бельгия - Франция - Люксембург',
     'Бельгия, Великобритания, США',
     'Бельгия, Канада',
     'Бельгия-Германия-Канада-Франция-США-Великобритания',
     'Бельгия-Нидерланды',
     'Бельгия-Франция',
     'Бельгия-Франция-Италия',
     'Болгария',
     'Болгария - США',
     'Болгария - Франция - Изриль',
     'Босния и Герцеговина - Франция - Великобритания - Германия - Словения - Бельгия - Сербия',
     'Бразилия',
     'Бразилия - Германия - Порртугалия - Франция ',
     'Бразилия - Испания',
     'Бразилия - К;анада',
     'Бразилия - Канада - США',
     'Бразилия - Португалия - Франция',
     'Бразилия - США',
     'Бразилия - США - КНР ',
     'Бразилия, Уругвай, Дания, Норвегия, Чили, Швеция',
     'Великобритания',
     'Великобритания ',
     'Великобритания - Австралия - США',
     'Великобритания - Австрия - Германия',
     'Великобритания - Австрия - Франция - США',
     'Великобритания - Аргентина - США - Франция - Россия - Испания',
     'Великобритания - Германия',
     'Великобритания - Германия - Нидерланды - Дания',
     'Великобритания - Германия - США',
     'Великобритания - Германия - Франция - Кипр - США',
     'Великобритания - Гонконг - Венгрия - США - Ирландия',
     'Великобритания - Дания',
     'Великобритания - Израиль',
     'Великобритания - Израиль - Франция - Япония - США',
     'Великобритания - Ирландия',
     'Великобритания - Ирландия - США',
     'Великобритания - Ирландия - США ',
     'Великобритания - Исландия - Испания - Швейцария - США',
     'Великобритания - Испания',
     'Великобритания - Испания - Германия',
     'Великобритания - Испания - Италия - Латвия - Франция - Эстония',
     'Великобритания - Испания - Непал - Индия - Венгрия - Гонконг - Германия - Дания - Бахрейн',
     'Великобритания - Италия',
     'Великобритания - Италия - Испания',
     'Великобритания - Италия - Швейцария',
     'Великобритания - КНР',
     'Великобритания - Канада',
     'Великобритания - Канада - США',
     'Великобритания - Люксембург',
     'Великобритания - Мексика - США',
     'Великобритания - Нидерланды - Германия - Франция - Бельгия - Австрия ',
     'Великобритания - Нидерланды - Франция - США',
     'Великобритания - Нидерланды - Франция - Хорватия',
     'Великобритания - Новая Зеландия',
     'Великобритания - Норвегия - Дания - Германия',
     'Великобритания - Норвегия - Кения - Хорватия',
     'Великобритания - Польша',
     'Великобритания - Польша - КНР - Индия - Норвегия',
     'Великобритания - Пуэрто-Рико',
     'Великобритания - Россия - КНР',
     'Великобритания - Россия - Украина - США',
     'Великобритания - Румыния',
     'Великобритания - США',
     'Великобритания - США - Австралия - Ирландия - Германия - Куба - Канада',
     'Великобритания - США - Германия',
     'Великобритания - США - Германия - Бельгия',
     'Великобритания - США - Германия - Канада - Австралия',
     'Великобритания - США - Индия',
     'Великобритания - США - Канада',
     'Великобритания - США - Канада - Бельгия - Нидерланды - Австрия - Германия',
     'Великобритания - США - Канада - Нидерланды - Франция',
     'Великобритания - США - Россия',
     'Великобритания - США - Франция',
     'Великобритания - США - Швейцария',
     'Великобритания - Франция',
     'Великобритания - Франция - Австрия - Швеция',
     'Великобритания - Франция - Бельгия',
     'Великобритания - Франция - Бельгия - Италия',
     'Великобритания - Франция - Бельгия - США',
     'Великобритания - Франция - Венгрия',
     'Великобритания - Франция - Германия',
     'Великобритания - Франция - Германия - США',
     'Великобритания - Франция - Италия',
     'Великобритания - Франция - Италия - Индия - Дания - КНР - Бангладеш - Камбоджа - Гаити - Уганда',
     'Великобритания - Франция - Италия - США',
     'Великобритания - Франция - Республика Кипр - Швейцария - США - Сербия',
     'Великобритания - Франция - США',
     'Великобритания - Франция - Швеция - Бельгия',
     'Великобритания - Чехия - Франция',
     'Великобритания - Чехия - Франция - Италия',
     'Великобритания - ЮАР',
     'Великобритания - Япония - США',
     'Великобритания, Австралия',
     'Великобритания, Германия, Дания, США',
     'Великобритания, Канада',
     'Великобритания, Канада, США',
     'Великобритания, Нидерланды, Польша, Швейцария, Франция',
     'Великобритания, Новая Зеландия',
     'Великобритания, США',
     'Великобритания, США, Испания',
     'Великобритания, Франция',
     'Великобритания, Франция, Бельгия',
     'Великобритания, Швеция, США',
     'Великобритания, Южная Корея, Канада, США, Индия, Китай, Япония',
     'Великобритания, Япония, США',
     'Великобритания-Австралия - США',
     'Великобритания-Венгрия',
     'Великобритания-Германия-Канада-ЮАР',
     'Великобритания-США',
     'Великобритания-США-Германия-КНР',
     'Великобритания-США-Франция',
     'Великобритания-Франция',
     'Великобритания-Франция-Германия',
     'Великобритания-Франция-Италия',
     'Венгрия',
     'Венгрия - Германия - Швеция',
     'Венесуэла',
     'Германия',
     'Германия - Австралия',
     'Германия - Австрия',
     'Германия - Австрия - Ирландия',
     'Германия - Австрия - Франция',
     'Германия - Аргентина - Нидерланды - Чили',
     'Германия - Бельгия',
     'Германия - Бельгия - Великобритания',
     'Германия - Бельгия - Люксембург - Ирландия',
     'Германия - Бельгия - Люксембург - Норвегия',
     'Германия - Бельгия - США -Франция',
     'Германия - Великобритания',
     'Германия - Великобритания - Австрия',
     'Германия - Великобритания - Италия - Испания',
     'Германия - Великобритания - США',
     'Германия - Дания - Испания - Швеция - Канада - Эстония - Франция',
     'Германия - Дания - Норвегия',
     'Германия - Исландия',
     'Германия - Италия',
     'Германия - Италия - США',
     'Германия - Италия - Франция',
     'Германия - Канада',
     'Германия - Китай',
     'Германия - Люксембург - Бельгия',
     'Германия - Люксембург - Дания',
     'Германия - Люксембург - Франция',
     'Германия - Нидерланды - Беларусь - Россия - Латвия',
     'Германия - Нидерланды - ЮАР',
     'Германия - Россия',
     'Германия - США',
     'Германия - США - Великобритания - Израиль',
     'Германия - США - Великобритания - Ирландия',
     'Германия - США - Франция - Испания',
     'Германия - США - Швеция - Франция',
     'Германия - Финляндия - Австралия',
     'Германия - Франция',
     'Германия - Франция -  Польша - Турция - Канада - Италия - Россия ',
     'Германия - Франция - Австрия',
     'Германия - Франция - Бельгия',
     'Германия - Франция - Великобритания - Польша - США',
     'Германия - Франция - Канада',
     'Германия - Франция - Люксембург',
     'Германия - Франция - Польша',
     'Германия - Швейцария',
     'Германия - Швейцария - Франция - Южная Корея - США',
     'Германия, Австралия',
     'Германия, Бельгия',
     'Германия, Россия',
     'Германия, США',
     'Германия, Франция',
     'Германия, Франция, Великобритания',
     'Германия, Франция, США',
     'Германия-Австрия',
     'Германия-Австрия-Франция-Италия',
     'Германия-Великобритания',
     'Германия-Израиль',
     'Германия-Италия- Шри-Ланка',
     'Германия-Италия-Швейцария',
     'Германия-Канада-Великобритания-Швейцария-Франция',
     'Германия-Канада-Франция-Бельгия',
     'Германия-Кения',
     'Германия-США',
     'Германия-Украина-Нидерланды',
     'Германия-Франция-Великобритания',
     'Германия-Франция-Великобритания-США',
     'Германия-Франция-Польша',
     'Германия-Швеция',
     'Голландия',
     'Гонконг',
     'Гонконг - КНР',
     'Гонконг - Сингапур - Таиланд - Великобритания',
     'Гонконг, КНР',
     'Греция',
     'Греция - Германия - Франция',
     'Греция - Россия',
     'Грузия',
     'Грузия - Россия - Украина - Хорватия - Германия',
     'Грузия - Украина',
     'Грузия - Франция - Люксембург',
     'Грузия-Россия',
     'Грузия-Франция',
     'Дания',
     'Дания - Австрия - Ирландия - Финляндия - Норвегия - Швеция - Нидерланды',
     'Дания - Великобритания - ЮАР',
     'Дания - Германия',
     'Дания - Германия - Швеция',
     'Дания - Исландия',
     'Дания - Канада - Швеция - Франция - Германия - Великобритания - США',
     'Дания - Латвия - Россия - США',
     'Дания - Норвегия - Великобритания',
     'Дания - США',
     'Дания - Франция - Германия - Швеция',
     'Дания - Франция - Италия - Бельгия - Нидерланды',
     'Дания - Швейцария - Бельгия - Франция',
     'Дания - Швеция',
     'Дания - Швеция - Великобритания - Франция - Германия - Нидерланды - Норвегия - Финляндия',
     'Дания - Швеция - Италия - Франция - Германия',
     'Дания, Канада, Норвегия, Австралия, США',
     'Дания, Норвегия, Венгрия, Чехия',
     'Дания, Норвегия, Швеция, Исландия',
     'Дания, Швеция, Великобритания, Франция, Германия, Норвегия, Финляндия, Нидерланды, Италия',
     'Дания-Франция-Бельгия-Германия-Великобритания',
     'Дания-Швеция-Франция-Германия',
     'Израиль',
     'Израиль - Германия - Польша - Бельгия - Франция - Люксембург',
     'Израиль - Германия - Франция - Швейцария',
     'Израиль - Франция',
     'Израиль - Франция - Великобритания - Германия',
     'Израиль - Франция - Германия - Палестина - США - Австрия - Великобритания',
     'Израиль, Украина',
     'Израиль-США-Франция',
     'Индия',
     'Индия - Великобритания',
     'Индия - КНР',
     'Индия - Мексика',
     'Индия - США',
     'Индонезия',
     'Иран',
     'Иран ',
     'Иран, Франция',
     'Ирландия',
     'Ирландия - Великобритания - Канада',
     'Ирландия - Великобритания - США',
     'Ирландия - Великобритания - Франция - США',
     'Ирландия - Великобритания - Франция - США - Германия - Нидерланды',
     'Ирландия - Дания - Бельгия - Люксембург - Франция',
     'Ирландия - США',
     'Ирландия - Финляндия - Бельгия - Великобритания - США - Швейцария',
     'Ирландия, Великобритания',
     'Ирландия, Канада',
     'Ирландия-Великобритания',
     'Ирландия-Великобритания-Германия',
     'Ирландия-Нидерланды-Франция-США-Великобритания',
     'Исландия',
     'Исландия - Финляндия',
     'Исландия, Бельгия',
     'Исландия-Ирландия-Германия',
     'Испания',
     'Испания - Аргентина',
     'Испания - Аргентина - Индия - США',
     'Испания - Бельгия - Франция - Португалия - Великобритания',
     'Испания - Болгария - США',
     'Испания - Великобритания - Франция',
     'Испания - Германия - Нидерланды',
     'Испания - Италия - Франция',
     'Испания - Канада',
     'Испания - Канада - Япония',
     'Испания - Куба',
     'Испания - Мальта',
     'Испания - Мексика',
     'Испания - США',
     'Испания - США - Великобритания - Канада',
     'Испания - США - Колумбия',
     'Испания - Уругвай - Аргентина',
     'Испания - Франция',
     'Испания - Франция - Нидерланды - Германия - Бельгия - Великобритания - Канада',
     'Испания - Франция - США - Великобритания - Бельгия',
     'Испания - Швейцария - Великобритания - Германия - Новая Зеландия - Нидерланды - Канада',
     'Испания, Ирландия, Бельгия, Франция',
     'Испания, Франция, Великобритания, Дания, Бельгия, Германия',
     'Испания, Франция, Италия',
     'Испания-Аргентина',
     'Испания-Канада',
     'Испания-Колумбия',
     'Испания-Мексика',
     'Испания-Франция-Греция-Индия-США-Россия-Великобритания',
     'Италия',
     'Италия ',
     'Италия - Аргентина - Словения ',
     'Италия - Бельгия - Франция',
     'Италия - Канада',
     'Италия - Россия',
     'Италия - США',
     'Италия - Франция',
     'Италия - Франция - Германия',
     'Италия - Франция - Швейцария',
     'Италия - Франция - Швейцария - Великобритания',
     'Италия - Фрация - Бразилия - Германия',
     'Италия - Швейцария - Германия',
     'Италия, Германия',
     'Италия, Испания',
     'Италия, Франция',
     'Италия, Франция, Германия',
     'Италия-Великобритания',
     'Италия-США',
     'Италия-Франция',
     'Италия-Франция-Великобритания',
     'Италия-Швейцария',
     'Италия-Швейцария-Франция-Германия ',
     'КНР',
     'КНР - Гонконг',
     'КНР - Гонконг - США',
     'КНР - Канада - США',
     'КНР - США',
     'КНР - США ',
     'КНР - Сингапур',
     'КНР - Франция',
     'КНР, Индия, Гонконг, США',
     'КНР, США',
     'КНР-США',
     'Казахстан',
     'Канада',
     'Канада - Германия',
     'Канада - Испания',
     'Канада - Италия',
     'Канада - КНР',
     'Канада - Мексика',
     'Канада - Норвегия',
     'Канада - США',
     'Канада - США - Германия - Франция',
     'Канада - США - Нидерланды - Великобритания - Аргентина',
     'Канада - Франция',
     'Канада - Франция - Великобритания',
     'Канада - Франция - Испания',
     'Канада - Франция - США - ОАЭ - Великобритания',
     'Канада - Южная Корея',
     'Канада, Великобритания',
     'Канада, США',
     'Канада, США, Каймановы острова',
     'Канада, США, Норвегия',
     'Канада, Франция, Италия, Швейцария, США',
     'Канада- Испания',
     'Канада-Бразилия-Япония',
     'Канада-Великобритания',
     'Канада-Германия',
     'Канада-США',
     'Канада-Франция',
     'Канада-ЮАР',
     'Канада-Южная Корея-США',
     'Кения, Германия',
     'Киргизия',
     'Киргизия-Россия',
     'Китай',
     'Китай - Гонконг',
     'Китай, Канада, США',
     'Китай, США',
     'Китай-Гонконг',
     'Китай-Гонконг-США',
     'Княжество Андорра - Украина',
     'Колумбия',
     'Колумбия - США',
     'Корея',
     'Латвия - Россия',
     'Латвия - Франция',
     'Ливан-США',
     'Литва - Венгрия',
     'Литва-Россия-Украина',
     'Люксембург - Бельгия - Франция',
     'Люксембург - Нидерланды - Испания - Великобритания - США - Италия',
     'Македония - Франция - Великобритания',
     'Малайзия',
     'Малайзия - США',
     'Мексика',
     'Мексика - Аргентина - Великобритания',
     'Мексика - Испания',
     'Мексика - Испания - Дания - США',
     'Мексика - Нидерланды - Германия - Франция',
     'Мексика - США',
     'Мексика - Тайвань - США',
     'Мексика - Франция',
     'Мексика - Франция - Нидерланды - Германия',
     'Мексика - Чили',
     'Мексика - Эквадор - Канада - США - Франция - Малайзия - Италия - Аргентина - Германия - Индия  ',
     'Мексика, Франция, Германия, Дания, Швеция',
     'Мексика-Аргентина',
     'Монголия',
     'Нидерланды',
     'Нидерланды - Бельгия - Болгария',
     'Нидерланды - Бельгия - Германия - Ирландия',
     'Нидерланды - Бельгия - Люксембург',
     'Нидерланды - Великобритания - Бельгия',
     'Нидерланды - Россия',
     'Нидерланды - Россия - Германия',
     'Нидерланды - США - Германия - Канада - Франция - Ирландия - Великобритания',
     'Нидерланды - Франция - Германия - Бельгия - Швеция - Великобритания',
     'Нидерланды, Бельгия',
     'Нидерланды, Бельгия, Люксембург',
     'Нидерланды-Великобритания-Франция-Италия-Япония',
     'Новая Зеландия',
     'Новая Зеландия - КНР',
     'Новая Зеландия - США',
     'Норвегия',
     'Норвегия - Азербайджан - Россия - Колумбия - Великобритания - Венгрия - Румыния - Франция - Грузия',
     'Норвегия - Дания - Швеция',
     'Норвегия - Исландия - США - Великобритания ',
     'Норвегия - Нидерланды',
     'Норвегия - США',
     'Норвегия - Швеция',
     'Норвегия - Швеция - Дания - Германия',
     'Норвегия - Швеция - Россия',
     'Норвегия, Швеция, Дания',
     'Норвения',
     'ОАЭ - США',
     'Пакистан',
     'Парагвай',
     'Перу',
     'Польша',
     'Польша - Ирландия',
     'Польша - Италия - Россия',
     'Польша - Португалия - Франция - Великобритания',
     'Польша - Франция',
     'Польша - Франция - Великобритания',
     'Польша - Франция - Испания - Бразилия - Швеция',
     'Португалия',
     'Португалия - Франция',
     'Португалия, Франция, Польша, США',
     'Пуэрто-Рико, Великобритания, США',
     'Республика Армения',
     'Республика Беларусь',
     'Республика Беларусь, Германия, США, Россия',
     'Республика Казахстан',
     'Республика Кипр',
     'Республика Кипр - Россия',
     'Республика Кипр, Россия',
     'Республика Кипр, США, Россия',
     'Республика Кипр-Россия',
     'Республика Корея',
     'Республика Узбекистан',
     'Россия',
     'Россия - Азербайджан',
     'Россия - Болгария',
     'Россия - Германия',
     'Россия - Германия - Украина',
     'Россия - Германия - Швейцария',
     'Россия - Грузия',
     'Россия - Италия',
     'Россия - Казахстан',
     'Россия - Польша',
     'Россия - Республика Кипр',
     'Россия - США',
     'Россия - Франция - Великобритания - Латвия',
     'Россия - Эстония - Финляндия - Беларусь',
     'Россия,  Испания',
     'Россия, Австрия',
     'Россия, Армения',
     'Россия, Бельгия, Финляндия',
     'Россия, Германия',
     'Россия, Германия, Великобритания',
     'Россия, Германия, Казахстан, Польша, Китай',
     'Россия, Германия, Франция, Бельгия',
     'Россия, Грузия, Испания',
     'Россия, Грузия, Хорватия, Испания',
     'Россия, Испания',
     'Россия, Италия',
     'Россия, Казахстан, США',
     'Россия, Латвия, Чешская Республика',
     'Россия, Нидерланды, Финляндия',
     'Россия, Польша, Финляндия',
     'Россия, Республика Беларусь',
     'Россия, Республика Кипр',
     'Россия, Румыния',
     'Россия, Сербия',
     'Россия, Таджикистан',
     'Россия, Украина',
     'Россия, Украина, Польша',
     'Россия, Украина, Республика Беларусь, Литва',
     'Россия, Франция, Германия, Бельгия',
     'Россия, Франция, Латвия',
     'Россия-Азербайджан',
     'Россия-Беларусь',
     'Россия-Белоруссия',
     'Россия-Германия',
     'Россия-Ирландия',
     'Россия-Италия',
     'Россия-Казахстан',
     'Россия-Кипр',
     'Россия-Китай',
     'Россия-Польша',
     'Россия-Польша-Голландия-Словакия',
     'Россия-США',
     'Россия-США-Канада-Люксембург',
     'Россия-Словакия-Чехия',
     'Россия-Украина',
     'Россия-Украина-Германия',
     'Россия-Франция',
     'Румыния',
     'Румыния - Франция - Бельгия',
     'Румыния, ЮАР, Иран, Франция, Канада, Великобритания',
     'Румыния-США',
     'СССР',
     'СССР ',
     'СССР  ',
     'СССР   ',
     'СССР    ',
     'СССР     ',
     'СССР - ГДР - Польша - Италия',
     'СССР - Италия',
     'СССР - Швейцария - Франция',
     'СССР, Албания',
     'СССР, Афганистан',
     'СССР, ВНР',
     'СССР, Венгрия',
     'СССР, Венгрия, ЧССР, ГДР',
     'СССР, ГДР',
     'СССР, Италия',
     'СССР, Монголия',
     'СССР, Польша',
     'СССР, Россия',
     'СССР, Румыния, Франция',
     'СССР, ФРГ',
     'СССР, ФРГ, Западный Берлин',
     'СССР, Финляндия',
     'СССР, Франция, Англия, Куба, ГДР',
     'СССР, ЧССР, Западный Берлин, ПНР',
     'СССР, Швеция',
     'США',
     'США ',
     'США - Австралия',
     'США - Австралия - Дания',
     'США - Австралия - Индия',
     'США - Австралия - Мексика',
     'США - Австралия - Новая Зеландия - Великобритания',
     'США - Австралия - Франция',
     'США - Бельгия',
     'США - Бельгия - Великобритания',
     'США - Болгария - Мексика',
     'США - Бразилия - Великобритания - Канада',
     'США - Бразилия - Франция - Австралия - Великобритания - Германия',
     'США - Великобритания',
     'США - Великобритания ',
     'США - Великобритания - Австралия',
     'США - Великобритания - Болгария',
     'США - Великобритания - Германия',
     'США - Великобритания - Германия - - Швеция - Канада',
     'США - Великобритания - Германия - Бельгия - Дания',
     'США - Великобритания - Германия - Новая Зеландия - Бельгия - Франция',
     'США - Великобритания - Ирландия',
     'США - Великобритания - Исландия',
     'США - Великобритания - Испания',
     'США - Великобритания - Италия - Израиль - Сербия - Индия',
     'США - Великобритания - КНР',
     'США - Великобритания - Канада',
     'США - Великобритания - Канада - КНР',
     'США - Великобритания - Канада - Швеция',
     'США - Великобритания - Новая Зеландия',
     'США - Великобритания - Франция',
     'США - Великобритания - Франция - Гонконг',
     'США - Великобритания - Чехия',
     'США - Великобритания - Швейцария - Франция',
     'США - Великобритания - Швеция',
     'США - Великобритания - Япония',
     'США - Великобритания- Франция - Швеция',
     'США - Венгрия - Великобритания',
     'США - Вьетнам',
     'США - Германия',
     'США - Германия - Великобритания',
     'США - Германия - Гонконг - Сингапур',
     'США - Германия - КНР',
     'США - Германия - Канада',
     'США - Германия - Нидерланды',
     'США - Германия - Франция',
     'США - Германия - Франция - Великобритания - Канада ',
     'США - Германия - Япония',
     'США - Гонконг',
     'США - Гонконг - КНР ',
     'США - Дания',
     'США - Индия',
     'США - Индия - ОАЭ',
     'США - Ирландия - Великобритания',
     'США - Ирландия - Великобритания - Франция',
     'США - Испания',
     'США - Испания - Болгария',
     'США - Испания - Франция',
     'США - Испания - Франция - Великобритания',
     'США - Италия',
     'США - КНР',
     'США - КНР - Индия - Ю.Корея',
     'США - Канада',
     'США - Канада - Аргентина',
     'США - Канада - Афганистан - Бельгия - Франция',
     'США - Канада - Великобритания',
     'США - Канада - Германия',
     'США - Канада - Германия - Франция',
     'США - Канада - Индонезия',
     'США - Канада - КНР',
     'США - Канада - Россия - Франция - Чили - Ирландия',
     'США - Канада - Франция - Индия',
     'США - Канада - Япония - КНР',
     'США - Китай',
     'США - Колумбия',
     'США - Колумбия - Испания',
     'США - Мальта',
     'США - Мексика',
     'США - Нидерланды - Бельгия - Венгрия - Греция - Канада',
     'США - Нидерланды - Финляндия - Великобритания - Италия',
     'США - Новая Зеландия',
     'США - Новая Зеландия - Япония',
     'США - Норвегия',
     'США - ОАЭ',
     'США - Объединенные Арабские Эмираты',
     'США - Пуэрто Рико',
     'США - Пуэрто-Рико - Франция ',
     'США - Россия',
     'США - Россия - Польша - Германия - Пуэрто Рико',
     'США - Россия - Франция',
     'США - Румыния - Великобритания',
     'США - Сингапур - Малайзия - Индонезия',
     'США - Украина',
     'США - Финляндия',
     'США - Финляндия - Испания - Великобритания - Франция',
     'США - Франция',
     'США - Франция - Бельгия - Италия',
     'США - Франция - Великобритания',
     'США - Франция - Великобритания - Бразилия ',
     'США - Франция - Германия',
     'США - Франция - Германия - Канада - Австралия ',
     'США - Франция - Испания - Великобритания',
     'США - Франция - Канада - Великобритания',
     'США - Франция - Канада - Германия - Австралия - Индия',
     'США - Франция - Турция',
     'США - Франция - ЮАР',
     'США - Хорватия - Босния-Герцеговина',
     'США - Чехия - Франция',
     'США - Чили',
     'США - Швейцария - Франция',
     'США - Швеция',
     'США - ЮАР',
     'США - ЮАР - Гонконг',
     'США - Южная Корея',
     'США - Япония',
     'США - Япония - Германия',
     'США - Япония - Канада - Великобритания - Германия - Франция',
     'США - Япония - Франция - Великобритания',
     'США -Великобритания - Австралия',
     'США -Германия',
     'США, Великобритания',
     'США, Великобритания, Ирландия, Люксембург',
     'США, Великобритания, Люксембург',
     'США, Великобритания, Франция',
     'США, Германия',
     'США, Гонконг ',
     'США, Индия',
     'США, Канада',
     'США, Россия',
     'США, Украина',
     'США, Франция',
     'США, Франция, Япония',
     'США, Япония',
     'США- Ю.Корея',
     'США-Австралия',
     'США-Аргентина',
     'США-Бельгия',
     'США-Великобритания',
     'США-Великобритания-Австралия',
     'США-Великобритания-Индия',
     'США-Великобритания-Ирландия',
     'США-Великобритания-Новая Зеландия',
     'США-Великобритания-Франция',
     'США-Великобритания-Чехия-Румыния',
     'США-Венгрия',
     'США-Германия',
     'США-Германия-Австралия',
     'США-Германия-Великобритания',
     'США-Германия-Канада',
     'США-Гонконг-Китай',
     'США-Индия',
     'США-Индонезия',
     'США-Ирландия',
     'США-Испания',
     'США-Италия-Греция',
     'США-Италия-Испания',
     'США-Италия-Испания-Аргентина',
     'США-КНР',
     'США-Канада',
     'США-Канада-Австралия',
     'США-Канада-Бельгия',
     'США-Канада-Италия',
     'США-Канада-Франция',
     'США-Китай',
     'США-Колумбия',
     'США-Мальта',
     'США-Мексика',
     'США-Нидерланды',
     'США-ОАЭ',
     'США-Россия',
     'США-ФРГ-Россия',
     'США-Франция',
     'США-Франция-Великобритания-Австрия',
     'США-Франция-Ирландия',
     'США-Франция-Испания',
     'США-Франция-Канада',
     'США-ЮАР',
     'США-Южная Корея-Новая Зеландия',
     'США-Япония',
     'США-Япония-Германия-Великобритания',
     'США-Япония-Германия-Великобритания-Нидерланды',
     'СЩА',
     'Сербия - Великобритания - США',
     'Сербия - Германия - Венгрия',
     'Сербия - Словения - Хорватия - Черногория - Македония',
     'Сингапур - Великобритания - Индонезия - Канада - США',
     'Сша, Канада',
     'Таиланд',
     'Таиланд - КНР - США',
     'Таиланд - США',
     'Таиланд-Великобритания-Франция-Германия-Испания-Нидерланды',
     'Турция',
     'Турция - Германя - Франция',
     'Турция - США',
     'Украина',
     'Украина - Германия - Латвия - Эстония',
     'Украина - Нидерланды',
     'Уругвай - Аргентина - Испания',
     'Уругвай - Колумбия',
     'Уругвай-Мексика-Германия ',
     'Финляндия',
     'Финляндия - Австрия - Россия',
     'Финляндия - Великобритания - Германия',
     'Финляндия - Германия',
     'Финляндия - Дания - Германия - Ирландия',
     'Финляндия - Исландия - Швеция',
     'Финляндия - Канада',
     'Финляндия - Польша',
     'Финляндия - Франция - Германия',
     'Финляндия - Швеция - Германия',
     'Финляндия - Швеция - Норвегия',
     'Финляндия, Латвия',
     'Финляндия-Дания-Германия-Ирландия',
     'Франция',
     'Франция ',
     'Франция -  Бельгия',
     'Франция - Австрия',
     'Франция - Австрия - Германия - Италия - США',
     'Франция - Бельгия',
     'Франция - Бельгия - Великобритания - Испания - Германия - США',
     'Франция - Бельгия - Великобритания - США - Нидерланды - Канада',
     'Франция - Бельгия - Испания',
     'Франция - Бельгия - Канада',
     'Франция - Бельгия - Люксембург',
     'Франция - Бельгия - Чехия',
     'Франция - Бельгия - Япония',
     'Франция - Бенльгия',
     'Франция - Бразилия',
     'Франция - Бразилия - Италия',
     'Франция - Великобритания',
     'Франция - Великобритания - Багамские острова - США',
     'Франция - Великобритания - Камбоджа - США - КНР',
     'Франция - Великобритания - Нидерланды - Люксембург',
     'Франция - Германия',
     'Франция - Германия - Австрия',
     'Франция - Германия - Бельгия',
     'Франция - Германия - Италия',
     'Франция - Германия - Литва - Нидерланды - Россия',
     'Франция - Германия - Нидерланды',
     'Франция - Германия - США',
     'Франция - Германия - Турция - Катар',
     'Франция - Германия - Швеция - США - Чехия - Словакия - Великобритания - Нидерланды',
     'Франция - Греция',
     'Франция - Дания',
     'Франция - Дания - США',
     'Франция - Дания - Швеция - КНР',
     'Франция - Израиль - Германия',
     'Франция - Ирландия - Швеция',
     'Франция - Испания',
     'Франция - Испания - Дания - Венгрия - Швейцария',
     'Франция - Испания - Румыния - США - Бельгия',
     'Франция - Испания - Тайвань',
     'Франция - Италия',
     'Франция - Италия - Бельгия - КНР',
     'Франция - Италия - Бельгия - Люксембург',
     'Франция - Италия - Великобритания - США',
     'Франция - Италия - Иран',
     'Франция - Италия - Швейцария',
     'Франция - КНР',
     'Франция - Канада',
     'Франция - Канада - Бельгия',
     'Франция - Канада - Н.Зеландия - США - Нидерланды - Германия - Швеция - Россия',
     'Франция - Люксембург',
     'Франция - Люксембург - Бельгия',
     'Франция - Люксембург - Германия - Бельгия - Швейцария - Великобритания ',
     'Франция - Македония',
     'Франция - Мексика - США',
     'Франция - Монако',
     'Франция - Нидерланды',
     'Франция - Польша - Бельгия',
     'Франция - Португалия',
     'Франция - Россия',
     'Франция - Россия - Швейцария - Румыния - Венгрия',
     'Франция - США',
     'Франция - США - Бельгия',
     'Франция - США - Великобритания - Колумбия - Бельгия - Россия',
     'Франция - США - Норвегия - Дания',
     'Франция - Сенегал - Бельгия',
     'Франция - Украина - Грузия - Армения',
     'Франция - Финляндия',
     'Франция - Чехия - Бельгия',
     'Франция - Чехия - Великобритания',
     'Франция - Чили',
     'Франция - Швейцария',
     'Франция - Швейцария - Германия',
     'Франция - Швеция - Дания - Норвегия',
     'Франция -Бельгия',
     'Франция, Бельгия',
     'Франция, Бельгия, Люксембург',
     'Франция, Германия',
     'Франция, Канада',
     'Франция, Люксембург, Бельгия',
     'Франция, Новая Зеландия',
     'Франция, Норвегия',
     'Франция-Австралия',
     'Франция-Аргентина',
     'Франция-Бельгия',
     'Франция-Бельгия-Канада',
     'Франция-Великобритания',
     'Франция-Великобритания - Германия',
     'Франция-Великобритания-Чехия',
     'Франция-Германия',
     'Франция-Германия-Австрия',
     'Франция-Германия-Великобритания',
     'Франция-Германия-Италия',
     'Франция-Гонконг-Ирландия',
     'Франция-Грузия-Германия-Россия-Украина-Бельгия',
     'Франция-Индия',
     'Франция-Испания',
     'Франция-Испания-Бельгия-Панама',
     'Франция-Испания-Германия',
     'Франция-Испания-Швейцария',
     'Франция-Италия',
     'Франция-Италия-Испания-Венгрия',
     'Франция-КНР',
     'Франция-Канада',
     'Франция-Китай',
     'Франция-Перу',
     'Франция-Польша',
     'Франция-Россия',
     'Франция-Россия-Румыния-Италия-Бельгия',
     'Франция-США',
     'Франция-Украина',
     'Хорватия',
     'Чехия',
     'Чехия - Германия',
     'Чехия - Испания - США',
     'Чехия - Словакия - Хорватия',
     'Чехия-Великобритания-США',
     'Чехословакия',
     'Чили',
     'Чили - Испания',
     'Чили - Франция - США',
     'Швейцария',
     'Швейцария - Австрия',
     'Швейцария - Великобритания',
     'Швейцария - Израиль - Франция - Великобритания',
     'Швейцария - КНР - США - Россия - Республика Корея - Великобритания',
     'Швейцария - Люксембург',
     'Швейцария - Франция',
     'Швейцария, Великобритания, Франция, США, Ирландия',
     'Швейцария-Австрия',
     'Швейцария-Германия-ЮАР',
     'Швейцария-Франция',
     'Швеция',
     'Швеция - Германия',
     'Швеция - Германия - Дания - Норвегия',
     'Швеция - Германия - Франция - Дания',
     'Швеция - Германия - Франция - Норвегия',
     'Швеция - Дания',
     'Швеция - Дания - Финляндия',
     'Швеция - Норвегия',
     'Швеция - США',
     'Швеция - Франция - Норвегия - Дания',
     'Швеция, Норвегия, Финляндия, Франция',
     'Швеция, Франция, Великобритания',
     'Швеция-Куба',
     'Швеция-Финляндия-Франция-Норвегия',
     'Швеция-Франция',
     'Швеция-Франция-Дания',
     'Эстония',
     'Эстония - Россия',
     'ЮАР',
     'ЮАР - США',
     'Южная Корея',
     'Южная Корея - КНР',
     'Южная Корея - США',
     'Южная Корея - США - Канада',
     'Япония',
     'Япония - Великобритания - Франция',
     'Япония - Великобритания - Швейцария - Ирландия - Дания - Франция - Польша - Австралия - Канада  ',
     'Япония - КНР - Южная Корея',
     'Япония - Канада',
     'Япония - США',
     'Япония - Франция - США - Южная Корея - Турция',
     'Япония, Великобритания',
     'Япония, Великобритания, Австрия, Германия, Ю.Корея',
     'Япония, США',
     'Япония-Великобритания',
     'Япония-США-Франция']




```python
# получим длину списка по названиям картин

len(df['production_country'].unique())
```




    950




```python
df[df['production_country'] == '2019']
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>7247</th>
      <td>Дело Коллини</td>
      <td>121027219.00</td>
      <td>2019-09-19 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Константин Филм, Глобал Скрин, Севен Пикчерз Сван</td>
      <td>2019</td>
      <td>Марко Кройцпайнтнер</td>
      <td>Мартин Московиц, Кристоф Мюллер, Марсель Хартг...</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.40</td>
      <td>детектив,драма,криминал</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



Мы видим, что в названиях стран присутствуют неявные дубликаты. Так некоторые названия стран-производителей разделены при помощи " - ", а другие при помощи " , ". Определим лямбда-функцию, которая уберет символ " - " как разделитель в строках с названиями стран-производителей и также уберет лишние пробелы в названиях. Заодно можно заметить, что имеется страна-производитель со значением "2019". Это явная ошибка при вводе данных. После ручного поиска картины "Дело Коллини" на сайте Кинопоиска, заменим данное значение на "Германия".


```python
# определим лямбда-функцию и применим ее методом apply с перезаписью датафрейма

df['production_country'] = df['production_country'].dropna().apply(lambda x: 
                                                                   ', '.join([x.strip() for x in x.split('-')]))
```


```python
df.loc[7247, 'production_country'] = 'Германия'
```


```python
sorted(df['production_country'].unique().tolist())
```




    ['CША',
     'Австралия',
     'Австралия, Великобритания',
     'Австралия, Великобритания, Бельгия, Индия',
     'Австралия, Германия',
     'Австралия, Ирландия',
     'Австралия, Канада',
     'Австралия, Колумбия',
     'Австралия, США',
     'Австралия, Турция, США',
     'Австрия',
     'Австрия, Великобритания, Германия',
     'Австрия, Германия',
     'Австрия, Германия, Франция',
     'Австрия, Люксембург',
     'Австрия, Франция, Германия',
     'Азербайджан, Россия',
     'Аргентина',
     'Аргентина, Бразилия',
     'Аргентина, Испания',
     'Аргентина, Испания, Уругвай',
     'Аргентина, Мексика, Бразилия, Франция, США',
     'Аргентина, Уругвай, Россия, Германия, Франция, Нидерланды',
     'Аргентина, Франция, Испания',
     'Армения',
     'Армения, Германия',
     'Армения, Казахстан',
     'Армения, Россия',
     'Бельгия',
     'Бельгия, Великобритания, США',
     'Бельгия, Германия, Канада, Франция, США, Великобритания',
     'Бельгия, Германия, Люксембург',
     'Бельгия, Германия, Люксембург, Франция',
     'Бельгия, Испания, Канада, Нидерланды',
     'Бельгия, Италия, Франция',
     'Бельгия, Канада',
     'Бельгия, Люксембург',
     'Бельгия, Люксембург, Франция, Швейцария',
     'Бельгия, Нидерланды',
     'Бельгия, Нидерланды, Франция',
     'Бельгия, США',
     'Бельгия, Франция',
     'Бельгия, Франция, Италия',
     'Бельгия, Франция, Люксембург',
     'Болгария',
     'Болгария, США',
     'Болгария, Франция, Изриль',
     'Босния и Герцеговина, Франция, Великобритания, Германия, Словения, Бельгия, Сербия',
     'Бразилия',
     'Бразилия, Германия, Порртугалия, Франция',
     'Бразилия, Испания',
     'Бразилия, К;анада',
     'Бразилия, Канада, США',
     'Бразилия, Португалия, Франция',
     'Бразилия, США',
     'Бразилия, США, КНР',
     'Бразилия, Уругвай, Дания, Норвегия, Чили, Швеция',
     'Великобритания',
     'Великобритания, Австралия',
     'Великобритания, Австралия, США',
     'Великобритания, Австрия, Германия',
     'Великобритания, Австрия, Франция, США',
     'Великобритания, Аргентина, США, Франция, Россия, Испания',
     'Великобритания, Венгрия',
     'Великобритания, Германия',
     'Великобритания, Германия, Дания, США',
     'Великобритания, Германия, Канада, ЮАР',
     'Великобритания, Германия, Нидерланды, Дания',
     'Великобритания, Германия, США',
     'Великобритания, Германия, Франция, Кипр, США',
     'Великобритания, Гонконг, Венгрия, США, Ирландия',
     'Великобритания, Дания',
     'Великобритания, Израиль',
     'Великобритания, Израиль, Франция, Япония, США',
     'Великобритания, Ирландия',
     'Великобритания, Ирландия, США',
     'Великобритания, Исландия, Испания, Швейцария, США',
     'Великобритания, Испания',
     'Великобритания, Испания, Германия',
     'Великобритания, Испания, Италия, Латвия, Франция, Эстония',
     'Великобритания, Испания, Непал, Индия, Венгрия, Гонконг, Германия, Дания, Бахрейн',
     'Великобритания, Италия',
     'Великобритания, Италия, Испания',
     'Великобритания, Италия, Швейцария',
     'Великобритания, КНР',
     'Великобритания, Канада',
     'Великобритания, Канада, США',
     'Великобритания, Люксембург',
     'Великобритания, Мексика, США',
     'Великобритания, Нидерланды, Германия, Франция, Бельгия, Австрия',
     'Великобритания, Нидерланды, Польша, Швейцария, Франция',
     'Великобритания, Нидерланды, Франция, США',
     'Великобритания, Нидерланды, Франция, Хорватия',
     'Великобритания, Новая Зеландия',
     'Великобритания, Норвегия, Дания, Германия',
     'Великобритания, Норвегия, Кения, Хорватия',
     'Великобритания, Польша',
     'Великобритания, Польша, КНР, Индия, Норвегия',
     'Великобритания, Пуэрто, Рико',
     'Великобритания, Россия, КНР',
     'Великобритания, Россия, Украина, США',
     'Великобритания, Румыния',
     'Великобритания, США',
     'Великобритания, США, Австралия, Ирландия, Германия, Куба, Канада',
     'Великобритания, США, Германия',
     'Великобритания, США, Германия, Бельгия',
     'Великобритания, США, Германия, КНР',
     'Великобритания, США, Германия, Канада, Австралия',
     'Великобритания, США, Индия',
     'Великобритания, США, Испания',
     'Великобритания, США, Канада',
     'Великобритания, США, Канада, Бельгия, Нидерланды, Австрия, Германия',
     'Великобритания, США, Канада, Нидерланды, Франция',
     'Великобритания, США, Россия',
     'Великобритания, США, Франция',
     'Великобритания, США, Швейцария',
     'Великобритания, Франция',
     'Великобритания, Франция, Австрия, Швеция',
     'Великобритания, Франция, Бельгия',
     'Великобритания, Франция, Бельгия, Италия',
     'Великобритания, Франция, Бельгия, США',
     'Великобритания, Франция, Венгрия',
     'Великобритания, Франция, Германия',
     'Великобритания, Франция, Германия, США',
     'Великобритания, Франция, Италия',
     'Великобритания, Франция, Италия, Индия, Дания, КНР, Бангладеш, Камбоджа, Гаити, Уганда',
     'Великобритания, Франция, Италия, США',
     'Великобритания, Франция, Республика Кипр, Швейцария, США, Сербия',
     'Великобритания, Франция, США',
     'Великобритания, Франция, Швеция, Бельгия',
     'Великобритания, Чехия, Франция',
     'Великобритания, Чехия, Франция, Италия',
     'Великобритания, Швеция, США',
     'Великобритания, ЮАР',
     'Великобритания, Южная Корея, Канада, США, Индия, Китай, Япония',
     'Великобритания, Япония, США',
     'Венгрия',
     'Венгрия, Германия, Швеция',
     'Венесуэла',
     'Германия',
     'Германия, Австралия',
     'Германия, Австрия',
     'Германия, Австрия, Ирландия',
     'Германия, Австрия, Франция',
     'Германия, Австрия, Франция, Италия',
     'Германия, Аргентина, Нидерланды, Чили',
     'Германия, Бельгия',
     'Германия, Бельгия, Великобритания',
     'Германия, Бельгия, Люксембург, Ирландия',
     'Германия, Бельгия, Люксембург, Норвегия',
     'Германия, Бельгия, США, Франция',
     'Германия, Великобритания',
     'Германия, Великобритания, Австрия',
     'Германия, Великобритания, Италия, Испания',
     'Германия, Великобритания, США',
     'Германия, Дания, Испания, Швеция, Канада, Эстония, Франция',
     'Германия, Дания, Норвегия',
     'Германия, Израиль',
     'Германия, Исландия',
     'Германия, Италия',
     'Германия, Италия, США',
     'Германия, Италия, Франция',
     'Германия, Италия, Швейцария',
     'Германия, Италия, Шри, Ланка',
     'Германия, Канада',
     'Германия, Канада, Великобритания, Швейцария, Франция',
     'Германия, Канада, Франция, Бельгия',
     'Германия, Кения',
     'Германия, Китай',
     'Германия, Люксембург, Бельгия',
     'Германия, Люксембург, Дания',
     'Германия, Люксембург, Франция',
     'Германия, Нидерланды, Беларусь, Россия, Латвия',
     'Германия, Нидерланды, ЮАР',
     'Германия, Россия',
     'Германия, США',
     'Германия, США, Великобритания, Израиль',
     'Германия, США, Великобритания, Ирландия',
     'Германия, США, Франция, Испания',
     'Германия, США, Швеция, Франция',
     'Германия, Украина, Нидерланды',
     'Германия, Финляндия, Австралия',
     'Германия, Франция',
     'Германия, Франция, Австрия',
     'Германия, Франция, Бельгия',
     'Германия, Франция, Великобритания',
     'Германия, Франция, Великобритания, Польша, США',
     'Германия, Франция, Великобритания, США',
     'Германия, Франция, Канада',
     'Германия, Франция, Люксембург',
     'Германия, Франция, Польша',
     'Германия, Франция, Польша, Турция, Канада, Италия, Россия',
     'Германия, Франция, США',
     'Германия, Швейцария',
     'Германия, Швейцария, Франция, Южная Корея, США',
     'Германия, Швеция',
     'Голландия',
     'Гонконг',
     'Гонконг, КНР',
     'Гонконг, Сингапур, Таиланд, Великобритания',
     'Греция',
     'Греция, Германия, Франция',
     'Греция, Россия',
     'Грузия',
     'Грузия, Россия',
     'Грузия, Россия, Украина, Хорватия, Германия',
     'Грузия, Украина',
     'Грузия, Франция',
     'Грузия, Франция, Люксембург',
     'Дания',
     'Дания, Австрия, Ирландия, Финляндия, Норвегия, Швеция, Нидерланды',
     'Дания, Великобритания, ЮАР',
     'Дания, Германия',
     'Дания, Германия, Швеция',
     'Дания, Исландия',
     'Дания, Канада, Норвегия, Австралия, США',
     'Дания, Канада, Швеция, Франция, Германия, Великобритания, США',
     'Дания, Латвия, Россия, США',
     'Дания, Норвегия, Великобритания',
     'Дания, Норвегия, Венгрия, Чехия',
     'Дания, Норвегия, Швеция, Исландия',
     'Дания, США',
     'Дания, Франция, Бельгия, Германия, Великобритания',
     'Дания, Франция, Германия, Швеция',
     'Дания, Франция, Италия, Бельгия, Нидерланды',
     'Дания, Швейцария, Бельгия, Франция',
     'Дания, Швеция',
     'Дания, Швеция, Великобритания, Франция, Германия, Нидерланды, Норвегия, Финляндия',
     'Дания, Швеция, Великобритания, Франция, Германия, Норвегия, Финляндия, Нидерланды, Италия',
     'Дания, Швеция, Италия, Франция, Германия',
     'Дания, Швеция, Франция, Германия',
     'Израиль',
     'Израиль, Германия, Польша, Бельгия, Франция, Люксембург',
     'Израиль, Германия, Франция, Швейцария',
     'Израиль, США, Франция',
     'Израиль, Украина',
     'Израиль, Франция',
     'Израиль, Франция, Великобритания, Германия',
     'Израиль, Франция, Германия, Палестина, США, Австрия, Великобритания',
     'Индия',
     'Индия, Великобритания',
     'Индия, КНР',
     'Индия, Мексика',
     'Индия, США',
     'Индонезия',
     'Иран',
     'Иран, Франция',
     'Ирландия',
     'Ирландия, Великобритания',
     'Ирландия, Великобритания, Германия',
     'Ирландия, Великобритания, Канада',
     'Ирландия, Великобритания, США',
     'Ирландия, Великобритания, Франция, США',
     'Ирландия, Великобритания, Франция, США, Германия, Нидерланды',
     'Ирландия, Дания, Бельгия, Люксембург, Франция',
     'Ирландия, Канада',
     'Ирландия, Нидерланды, Франция, США, Великобритания',
     'Ирландия, США',
     'Ирландия, Финляндия, Бельгия, Великобритания, США, Швейцария',
     'Исландия',
     'Исландия, Бельгия',
     'Исландия, Ирландия, Германия',
     'Исландия, Финляндия',
     'Испания',
     'Испания, Аргентина',
     'Испания, Аргентина, Индия, США',
     'Испания, Бельгия, Франция, Португалия, Великобритания',
     'Испания, Болгария, США',
     'Испания, Великобритания, Франция',
     'Испания, Германия, Нидерланды',
     'Испания, Ирландия, Бельгия, Франция',
     'Испания, Италия, Франция',
     'Испания, Канада',
     'Испания, Канада, Япония',
     'Испания, Колумбия',
     'Испания, Куба',
     'Испания, Мальта',
     'Испания, Мексика',
     'Испания, США',
     'Испания, США, Великобритания, Канада',
     'Испания, США, Колумбия',
     'Испания, Уругвай, Аргентина',
     'Испания, Франция',
     'Испания, Франция, Великобритания, Дания, Бельгия, Германия',
     'Испания, Франция, Греция, Индия, США, Россия, Великобритания',
     'Испания, Франция, Италия',
     'Испания, Франция, Нидерланды, Германия, Бельгия, Великобритания, Канада',
     'Испания, Франция, США, Великобритания, Бельгия',
     'Испания, Швейцария, Великобритания, Германия, Новая Зеландия, Нидерланды, Канада',
     'Италия',
     'Италия, Аргентина, Словения',
     'Италия, Бельгия, Франция',
     'Италия, Великобритания',
     'Италия, Германия',
     'Италия, Испания',
     'Италия, Канада',
     'Италия, Россия',
     'Италия, США',
     'Италия, Франция',
     'Италия, Франция, Великобритания',
     'Италия, Франция, Германия',
     'Италия, Франция, Швейцария',
     'Италия, Франция, Швейцария, Великобритания',
     'Италия, Фрация, Бразилия, Германия',
     'Италия, Швейцария',
     'Италия, Швейцария, Германия',
     'Италия, Швейцария, Франция, Германия',
     'КНР',
     'КНР, Гонконг',
     'КНР, Гонконг, США',
     'КНР, Индия, Гонконг, США',
     'КНР, Канада, США',
     'КНР, США',
     'КНР, Сингапур',
     'КНР, Франция',
     'Казахстан',
     'Канада',
     'Канада, Бразилия, Япония',
     'Канада, Великобритания',
     'Канада, Германия',
     'Канада, Испания',
     'Канада, Италия',
     'Канада, КНР',
     'Канада, Мексика',
     'Канада, Норвегия',
     'Канада, США',
     'Канада, США, Германия, Франция',
     'Канада, США, Каймановы острова',
     'Канада, США, Нидерланды, Великобритания, Аргентина',
     'Канада, США, Норвегия',
     'Канада, Франция',
     'Канада, Франция, Великобритания',
     'Канада, Франция, Испания',
     'Канада, Франция, Италия, Швейцария, США',
     'Канада, Франция, США, ОАЭ, Великобритания',
     'Канада, ЮАР',
     'Канада, Южная Корея',
     'Канада, Южная Корея, США',
     'Кения, Германия',
     'Киргизия',
     'Киргизия, Россия',
     'Китай',
     'Китай, Гонконг',
     'Китай, Гонконг, США',
     'Китай, Канада, США',
     'Китай, США',
     'Княжество Андорра, Украина',
     'Колумбия',
     'Колумбия, США',
     'Корея',
     'Латвия, Россия',
     'Латвия, Франция',
     'Ливан, США',
     'Литва, Венгрия',
     'Литва, Россия, Украина',
     'Люксембург, Бельгия, Франция',
     'Люксембург, Нидерланды, Испания, Великобритания, США, Италия',
     'Македония, Франция, Великобритания',
     'Малайзия',
     'Малайзия, США',
     'Мексика',
     'Мексика, Аргентина',
     'Мексика, Аргентина, Великобритания',
     'Мексика, Испания',
     'Мексика, Испания, Дания, США',
     'Мексика, Нидерланды, Германия, Франция',
     'Мексика, США',
     'Мексика, Тайвань, США',
     'Мексика, Франция',
     'Мексика, Франция, Германия, Дания, Швеция',
     'Мексика, Франция, Нидерланды, Германия',
     'Мексика, Чили',
     'Мексика, Эквадор, Канада, США, Франция, Малайзия, Италия, Аргентина, Германия, Индия',
     'Монголия',
     'Нидерланды',
     'Нидерланды, Бельгия',
     'Нидерланды, Бельгия, Болгария',
     'Нидерланды, Бельгия, Германия, Ирландия',
     'Нидерланды, Бельгия, Люксембург',
     'Нидерланды, Великобритания, Бельгия',
     'Нидерланды, Великобритания, Франция, Италия, Япония',
     'Нидерланды, Россия',
     'Нидерланды, Россия, Германия',
     'Нидерланды, США, Германия, Канада, Франция, Ирландия, Великобритания',
     'Нидерланды, Франция, Германия, Бельгия, Швеция, Великобритания',
     'Новая Зеландия',
     'Новая Зеландия, КНР',
     'Новая Зеландия, США',
     'Норвегия',
     'Норвегия, Азербайджан, Россия, Колумбия, Великобритания, Венгрия, Румыния, Франция, Грузия',
     'Норвегия, Дания, Швеция',
     'Норвегия, Исландия, США, Великобритания',
     'Норвегия, Нидерланды',
     'Норвегия, США',
     'Норвегия, Швеция',
     'Норвегия, Швеция, Дания',
     'Норвегия, Швеция, Дания, Германия',
     'Норвегия, Швеция, Россия',
     'Норвения',
     'ОАЭ, США',
     'Пакистан',
     'Парагвай',
     'Перу',
     'Польша',
     'Польша, Ирландия',
     'Польша, Италия, Россия',
     'Польша, Португалия, Франция, Великобритания',
     'Польша, Франция',
     'Польша, Франция, Великобритания',
     'Польша, Франция, Испания, Бразилия, Швеция',
     'Португалия',
     'Португалия, Франция',
     'Португалия, Франция, Польша, США',
     'Пуэрто, Рико, Великобритания, США',
     'Республика Армения',
     'Республика Беларусь',
     'Республика Беларусь, Германия, США, Россия',
     'Республика Казахстан',
     'Республика Кипр',
     'Республика Кипр, Россия',
     'Республика Кипр, США, Россия',
     'Республика Корея',
     'Республика Узбекистан',
     'Россия',
     'Россия,  Испания',
     'Россия, Австрия',
     'Россия, Азербайджан',
     'Россия, Армения',
     'Россия, Беларусь',
     'Россия, Белоруссия',
     'Россия, Бельгия, Финляндия',
     'Россия, Болгария',
     'Россия, Германия',
     'Россия, Германия, Великобритания',
     'Россия, Германия, Казахстан, Польша, Китай',
     'Россия, Германия, Украина',
     'Россия, Германия, Франция, Бельгия',
     'Россия, Германия, Швейцария',
     'Россия, Грузия',
     'Россия, Грузия, Испания',
     'Россия, Грузия, Хорватия, Испания',
     'Россия, Ирландия',
     'Россия, Испания',
     'Россия, Италия',
     'Россия, Казахстан',
     'Россия, Казахстан, США',
     'Россия, Кипр',
     'Россия, Китай',
     'Россия, Латвия, Чешская Республика',
     'Россия, Нидерланды, Финляндия',
     'Россия, Польша',
     'Россия, Польша, Голландия, Словакия',
     'Россия, Польша, Финляндия',
     'Россия, Республика Беларусь',
     'Россия, Республика Кипр',
     'Россия, Румыния',
     'Россия, США',
     'Россия, США, Канада, Люксембург',
     'Россия, Сербия',
     'Россия, Словакия, Чехия',
     'Россия, Таджикистан',
     'Россия, Украина',
     'Россия, Украина, Германия',
     'Россия, Украина, Польша',
     'Россия, Украина, Республика Беларусь, Литва',
     'Россия, Франция',
     'Россия, Франция, Великобритания, Латвия',
     'Россия, Франция, Германия, Бельгия',
     'Россия, Франция, Латвия',
     'Россия, Эстония, Финляндия, Беларусь',
     'Румыния',
     'Румыния, США',
     'Румыния, Франция, Бельгия',
     'Румыния, ЮАР, Иран, Франция, Канада, Великобритания',
     'СССР',
     'СССР, Албания',
     'СССР, Афганистан',
     'СССР, ВНР',
     'СССР, Венгрия',
     'СССР, Венгрия, ЧССР, ГДР',
     'СССР, ГДР',
     'СССР, ГДР, Польша, Италия',
     'СССР, Италия',
     'СССР, Монголия',
     'СССР, Польша',
     'СССР, Россия',
     'СССР, Румыния, Франция',
     'СССР, ФРГ',
     'СССР, ФРГ, Западный Берлин',
     'СССР, Финляндия',
     'СССР, Франция, Англия, Куба, ГДР',
     'СССР, ЧССР, Западный Берлин, ПНР',
     'СССР, Швейцария, Франция',
     'СССР, Швеция',
     'США',
     'США, Австралия',
     'США, Австралия, Дания',
     'США, Австралия, Индия',
     'США, Австралия, Мексика',
     'США, Австралия, Новая Зеландия, Великобритания',
     'США, Австралия, Франция',
     'США, Аргентина',
     'США, Бельгия',
     'США, Бельгия, Великобритания',
     'США, Болгария, Мексика',
     'США, Бразилия, Великобритания, Канада',
     'США, Бразилия, Франция, Австралия, Великобритания, Германия',
     'США, Великобритания',
     'США, Великобритания, Австралия',
     'США, Великобритания, Болгария',
     'США, Великобритания, Германия',
     'США, Великобритания, Германия, , Швеция, Канада',
     'США, Великобритания, Германия, Бельгия, Дания',
     'США, Великобритания, Германия, Новая Зеландия, Бельгия, Франция',
     'США, Великобритания, Индия',
     'США, Великобритания, Ирландия',
     'США, Великобритания, Ирландия, Люксембург',
     'США, Великобритания, Исландия',
     'США, Великобритания, Испания',
     'США, Великобритания, Италия, Израиль, Сербия, Индия',
     'США, Великобритания, КНР',
     'США, Великобритания, Канада',
     'США, Великобритания, Канада, КНР',
     'США, Великобритания, Канада, Швеция',
     'США, Великобритания, Люксембург',
     'США, Великобритания, Новая Зеландия',
     'США, Великобритания, Франция',
     'США, Великобритания, Франция, Гонконг',
     'США, Великобритания, Франция, Швеция',
     'США, Великобритания, Чехия',
     'США, Великобритания, Чехия, Румыния',
     'США, Великобритания, Швейцария, Франция',
     'США, Великобритания, Швеция',
     'США, Великобритания, Япония',
     'США, Венгрия',
     'США, Венгрия, Великобритания',
     'США, Вьетнам',
     'США, Германия',
     'США, Германия, Австралия',
     'США, Германия, Великобритания',
     'США, Германия, Гонконг, Сингапур',
     'США, Германия, КНР',
     'США, Германия, Канада',
     'США, Германия, Нидерланды',
     'США, Германия, Франция',
     'США, Германия, Франция, Великобритания, Канада',
     'США, Германия, Япония',
     'США, Гонконг',
     'США, Гонконг, КНР',
     'США, Гонконг, Китай',
     'США, Дания',
     'США, Индия',
     'США, Индия, ОАЭ',
     'США, Индонезия',
     'США, Ирландия',
     'США, Ирландия, Великобритания',
     'США, Ирландия, Великобритания, Франция',
     'США, Испания',
     'США, Испания, Болгария',
     'США, Испания, Франция',
     'США, Испания, Франция, Великобритания',
     'США, Италия',
     'США, Италия, Греция',
     'США, Италия, Испания',
     'США, Италия, Испания, Аргентина',
     'США, КНР',
     'США, КНР, Индия, Ю.Корея',
     'США, Канада',
     'США, Канада, Австралия',
     'США, Канада, Аргентина',
     'США, Канада, Афганистан, Бельгия, Франция',
     'США, Канада, Бельгия',
     'США, Канада, Великобритания',
     'США, Канада, Германия',
     'США, Канада, Германия, Франция',
     'США, Канада, Индонезия',
     'США, Канада, Италия',
     'США, Канада, КНР',
     'США, Канада, Россия, Франция, Чили, Ирландия',
     'США, Канада, Франция',
     'США, Канада, Франция, Индия',
     'США, Канада, Япония, КНР',
     'США, Китай',
     'США, Колумбия',
     'США, Колумбия, Испания',
     'США, Мальта',
     'США, Мексика',
     'США, Нидерланды',
     'США, Нидерланды, Бельгия, Венгрия, Греция, Канада',
     'США, Нидерланды, Финляндия, Великобритания, Италия',
     'США, Новая Зеландия',
     'США, Новая Зеландия, Япония',
     'США, Норвегия',
     'США, ОАЭ',
     'США, Объединенные Арабские Эмираты',
     'США, Пуэрто Рико',
     'США, Пуэрто, Рико, Франция',
     'США, Россия',
     'США, Россия, Польша, Германия, Пуэрто Рико',
     'США, Россия, Франция',
     'США, Румыния, Великобритания',
     'США, Сингапур, Малайзия, Индонезия',
     'США, Украина',
     'США, ФРГ, Россия',
     'США, Финляндия',
     'США, Финляндия, Испания, Великобритания, Франция',
     'США, Франция',
     'США, Франция, Бельгия, Италия',
     'США, Франция, Великобритания',
     'США, Франция, Великобритания, Австрия',
     'США, Франция, Великобритания, Бразилия',
     'США, Франция, Германия',
     'США, Франция, Германия, Канада, Австралия',
     'США, Франция, Ирландия',
     'США, Франция, Испания',
     'США, Франция, Испания, Великобритания',
     'США, Франция, Канада',
     'США, Франция, Канада, Великобритания',
     'США, Франция, Канада, Германия, Австралия, Индия',
     'США, Франция, Турция',
     'США, Франция, ЮАР',
     'США, Франция, Япония',
     'США, Хорватия, Босния, Герцеговина',
     'США, Чехия, Франция',
     'США, Чили',
     'США, Швейцария, Франция',
     'США, Швеция',
     'США, Ю.Корея',
     'США, ЮАР',
     'США, ЮАР, Гонконг',
     'США, Южная Корея',
     'США, Южная Корея, Новая Зеландия',
     'США, Япония',
     'США, Япония, Германия',
     'США, Япония, Германия, Великобритания',
     'США, Япония, Германия, Великобритания, Нидерланды',
     'США, Япония, Канада, Великобритания, Германия, Франция',
     'США, Япония, Франция, Великобритания',
     'СЩА',
     'Сербия, Великобритания, США',
     'Сербия, Германия, Венгрия',
     'Сербия, Словения, Хорватия, Черногория, Македония',
     'Сингапур, Великобритания, Индонезия, Канада, США',
     'Сша, Канада',
     'Таиланд',
     'Таиланд, Великобритания, Франция, Германия, Испания, Нидерланды',
     'Таиланд, КНР, США',
     'Таиланд, США',
     'Турция',
     'Турция, Германя, Франция',
     'Турция, США',
     'Украина',
     'Украина, Германия, Латвия, Эстония',
     'Украина, Нидерланды',
     'Уругвай, Аргентина, Испания',
     'Уругвай, Колумбия',
     'Уругвай, Мексика, Германия',
     'Финляндия',
     'Финляндия, Австрия, Россия',
     'Финляндия, Великобритания, Германия',
     'Финляндия, Германия',
     'Финляндия, Дания, Германия, Ирландия',
     'Финляндия, Исландия, Швеция',
     'Финляндия, Канада',
     'Финляндия, Латвия',
     'Финляндия, Польша',
     'Финляндия, Франция, Германия',
     'Финляндия, Швеция, Германия',
     'Финляндия, Швеция, Норвегия',
     'Франция',
     'Франция, Австралия',
     'Франция, Австрия',
     'Франция, Австрия, Германия, Италия, США',
     'Франция, Аргентина',
     'Франция, Бельгия',
     'Франция, Бельгия, Великобритания, Испания, Германия, США',
     'Франция, Бельгия, Великобритания, США, Нидерланды, Канада',
     'Франция, Бельгия, Испания',
     'Франция, Бельгия, Канада',
     'Франция, Бельгия, Люксембург',
     'Франция, Бельгия, Чехия',
     'Франция, Бельгия, Япония',
     'Франция, Бенльгия',
     'Франция, Бразилия',
     'Франция, Бразилия, Италия',
     'Франция, Великобритания',
     'Франция, Великобритания, Багамские острова, США',
     'Франция, Великобритания, Германия',
     'Франция, Великобритания, Камбоджа, США, КНР',
     'Франция, Великобритания, Нидерланды, Люксембург',
     'Франция, Великобритания, Чехия',
     'Франция, Германия',
     'Франция, Германия, Австрия',
     'Франция, Германия, Бельгия',
     'Франция, Германия, Великобритания',
     'Франция, Германия, Италия',
     'Франция, Германия, Литва, Нидерланды, Россия',
     'Франция, Германия, Нидерланды',
     'Франция, Германия, США',
     'Франция, Германия, Турция, Катар',
     'Франция, Германия, Швеция, США, Чехия, Словакия, Великобритания, Нидерланды',
     'Франция, Гонконг, Ирландия',
     'Франция, Греция',
     'Франция, Грузия, Германия, Россия, Украина, Бельгия',
     'Франция, Дания',
     'Франция, Дания, США',
     'Франция, Дания, Швеция, КНР',
     'Франция, Израиль, Германия',
     'Франция, Индия',
     'Франция, Ирландия, Швеция',
     'Франция, Испания',
     'Франция, Испания, Бельгия, Панама',
     'Франция, Испания, Германия',
     'Франция, Испания, Дания, Венгрия, Швейцария',
     'Франция, Испания, Румыния, США, Бельгия',
     'Франция, Испания, Тайвань',
     'Франция, Испания, Швейцария',
     'Франция, Италия',
     'Франция, Италия, Бельгия, КНР',
     'Франция, Италия, Бельгия, Люксембург',
     'Франция, Италия, Великобритания, США',
     'Франция, Италия, Иран',
     'Франция, Италия, Испания, Венгрия',
     'Франция, Италия, Швейцария',
     'Франция, КНР',
     'Франция, Канада',
     'Франция, Канада, Бельгия',
     'Франция, Канада, Н.Зеландия, США, Нидерланды, Германия, Швеция, Россия',
     'Франция, Китай',
     'Франция, Люксембург',
     'Франция, Люксембург, Бельгия',
     'Франция, Люксембург, Германия, Бельгия, Швейцария, Великобритания',
     'Франция, Македония',
     'Франция, Мексика, США',
     'Франция, Монако',
     'Франция, Нидерланды',
     'Франция, Новая Зеландия',
     'Франция, Норвегия',
     'Франция, Перу',
     'Франция, Польша',
     'Франция, Польша, Бельгия',
     'Франция, Португалия',
     'Франция, Россия',
     'Франция, Россия, Румыния, Италия, Бельгия',
     'Франция, Россия, Швейцария, Румыния, Венгрия',
     'Франция, США',
     'Франция, США, Бельгия',
     'Франция, США, Великобритания, Колумбия, Бельгия, Россия',
     'Франция, США, Норвегия, Дания',
     'Франция, Сенегал, Бельгия',
     'Франция, Украина',
     'Франция, Украина, Грузия, Армения',
     'Франция, Финляндия',
     'Франция, Чехия, Бельгия',
     'Франция, Чехия, Великобритания',
     'Франция, Чили',
     'Франция, Швейцария',
     'Франция, Швейцария, Германия',
     'Франция, Швеция, Дания, Норвегия',
     'Хорватия',
     'Чехия',
     'Чехия, Великобритания, США',
     'Чехия, Германия',
     'Чехия, Испания, США',
     'Чехия, Словакия, Хорватия',
     'Чехословакия',
     'Чили',
     'Чили, Испания',
     'Чили, Франция, США',
     'Швейцария',
     'Швейцария, Австрия',
     'Швейцария, Великобритания',
     'Швейцария, Великобритания, Франция, США, Ирландия',
     'Швейцария, Германия, ЮАР',
     'Швейцария, Израиль, Франция, Великобритания',
     'Швейцария, КНР, США, Россия, Республика Корея, Великобритания',
     'Швейцария, Люксембург',
     'Швейцария, Франция',
     'Швеция',
     'Швеция, Германия',
     'Швеция, Германия, Дания, Норвегия',
     'Швеция, Германия, Франция, Дания',
     'Швеция, Германия, Франция, Норвегия',
     'Швеция, Дания',
     'Швеция, Дания, Финляндия',
     'Швеция, Куба',
     'Швеция, Норвегия',
     'Швеция, Норвегия, Финляндия, Франция',
     'Швеция, США',
     'Швеция, Финляндия, Франция, Норвегия',
     'Швеция, Франция',
     'Швеция, Франция, Великобритания',
     'Швеция, Франция, Дания',
     'Швеция, Франция, Норвегия, Дания',
     'Эстония',
     'Эстония, Россия',
     'ЮАР',
     'ЮАР, США',
     'Южная Корея',
     'Южная Корея, КНР',
     'Южная Корея, США',
     'Южная Корея, США, Канада',
     'Япония',
     'Япония, Великобритания',
     'Япония, Великобритания, Австрия, Германия, Ю.Корея',
     'Япония, Великобритания, Франция',
     'Япония, Великобритания, Швейцария, Ирландия, Дания, Франция, Польша, Австралия, Канада',
     'Япония, КНР, Южная Корея',
     'Япония, Канада',
     'Япония, США',
     'Япония, США, Франция',
     'Япония, Франция, США, Южная Корея, Турция']




```python
# длина списка уникальных названий стран-производителей фильмов сократилась
len(df['production_country'].unique())
```




    812



**Вывод:**

Явных дубликатов в нашем датасете не было обнаружено. Есть дубликаты в названиях фильмов, но это может быть обусловлено тем, что у одного фильма может быть несколько прокатных удостоверений. Данная специфика была указана изначально в описании данных. Удалить дубликаты мы не можем, так как в этом случае утеряется номер прокатного удостоверения. Есть дубликаты в номерах прокатных удостоверений, это может быть связано с тем, что под одним удостоверением выходило в прокат несколько фильмов. Устранили неявные дубликаты в названиях стран-производителей с помощью функции, сократив тем самым количество дубликатов на 138 значений.

### Категориальные значения

- Посмотрим, какая общая проблема встречается почти во всех категориальных столбцах;
- Исправим проблемные значения в поле `type`.

Для удобства визуализации выведем результаты для столбцов с категориальными значениями списком, отсортировав при этом значения в алфавитном порядке.


```python
df['age_restriction'].sort_values().unique()
```




    array(['«0+» - для любой зрительской аудитории',
           '«12+» - для детей старше 12 лет',
           '«16+» - для детей старше 16 лет', '«18+» - запрещено для детей',
           '«6+» - для детей старше 6 лет'], dtype=object)




```python
df['type'].sort_values().unique()
```




    array([' Анимационный', ' Художественный', 'Анимационный',
           'Документальный', 'Музыкально-развлекательный',
           'Научно-популярный', 'Прочие', 'Художественный'], dtype=object)




```python
df['type'].value_counts()
```




    type
    Художественный                4520
     Художественный               1389
    Анимационный                   828
    Прочие                         406
    Документальный                 288
    Научно-популярный               53
     Анимационный                    1
    Музыкально-развлекательный       1
    Name: count, dtype: int64




```python
df['genres'].value_counts()
```




    genres
    unknown                         976
    драма                           476
    комедия                         352
    мелодрама,комедия               222
    драма,мелодрама,комедия         189
                                   ... 
    мюзикл,фэнтези,семейный           1
    мюзикл,мелодрама,фэнтези          1
    документальный,новости,драма      1
    семейный,детектив,детский         1
    мелодрама,история,драма           1
    Name: count, Length: 743, dtype: int64




```python
df['financing_source'].sort_values().unique()
```




    array(['Министерство культуры', 'Министерство культуры, Фонд кино',
           'Фонд кино', nan], dtype=object)



Мы замечаем как в столбце type есть несколько значений, у которых появился пробел в начале строки. Самый простой способ это исправить используя метод .str.strip(). Этот метод удалит все пробелы, которые встречаются в начале и в конце строки. Применим метод следующим образом:


```python
df['type'] = df['type'].str.strip()
df['type'].sort_values().unique()
```




    array(['Анимационный', 'Документальный', 'Музыкально-развлекательный',
           'Научно-популярный', 'Прочие', 'Художественный'], dtype=object)



**Вывод:** 

В столбце **type** были лишние пробелы, мы исправили это с помощью метода str.strip() . В пункте 2.3.3 мы также предобработали столбец **production_country** применив к строкам метод strip() избавивишись тем самым от дубликатов. Столбец **genres** оставим так как есть, так как нам предстоит извлечь первые значения из списка жанров в дальнейшем.


```python
# удалим также из столбца production_country лишние пробелы, которые встречаются внутри строки

df['production_country']=df['production_country'].replace(' ','', regex=True)

# заменим еще в столбце production_country дефис на запятую в целях единообразия разделителей

df['production_country']=df['production_country'].replace('-',',', regex=True)
```

### Проверим количественные значения

- Проверим, обнаружились ли в таких столбцах подозрительные данные. Как с такими данными лучше поступить?


Проведем анализ количественных переменных нашего датасета, выделив столбцы с количественными значениями в отдельную переменную. Проанализируем фильмы, бюджет которых принимает нулевое значение. Несмотря на это можно заметить, что у некоторых фильмов с нулевым бюджетом сумма поддержки ненулевая. В этом случае бюджет не может быть меньше суммы поддержки, так как в описании данных сказано, что столбец budget уже включает в себя полный объём государственной поддержки. Если зайти на сайт Господдержки по фильмам ( https://ekinobilet.fond-kino.ru/government-support/ ) и посмотреть эти картины, можно увидеть что: "Данные не предоставлены правообладателем". Это могло стать причиной нулевого бюджета при наличии государственной поддержки.


```python
groups = ['refundable_support', 'nonrefundable_support',
          'budget', 'box_office', 'ratings']
df[groups].describe().T
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>refundable_support</th>
      <td>332.00</td>
      <td>11864457.83</td>
      <td>24916555.26</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>15000000.00</td>
      <td>180000000.00</td>
    </tr>
    <tr>
      <th>nonrefundable_support</th>
      <td>332.00</td>
      <td>48980988.89</td>
      <td>59980117.92</td>
      <td>0.00</td>
      <td>25000000.00</td>
      <td>30000000.00</td>
      <td>40375000.00</td>
      <td>400000000.00</td>
    </tr>
    <tr>
      <th>budget</th>
      <td>332.00</td>
      <td>127229716.68</td>
      <td>188588333.12</td>
      <td>0.00</td>
      <td>42000000.00</td>
      <td>68649916.00</td>
      <td>141985319.50</td>
      <td>2305074303.00</td>
    </tr>
    <tr>
      <th>box_office</th>
      <td>3158.00</td>
      <td>76478696.16</td>
      <td>240353122.82</td>
      <td>0.00</td>
      <td>86239.00</td>
      <td>2327987.55</td>
      <td>23979671.02</td>
      <td>3073568690.79</td>
    </tr>
    <tr>
      <th>ratings</th>
      <td>6490.00</td>
      <td>6.48</td>
      <td>1.10</td>
      <td>1.00</td>
      <td>5.90</td>
      <td>6.60</td>
      <td>7.20</td>
      <td>9.20</td>
    </tr>
  </tbody>
</table>
</div>




```python
df[df['budget'] == 0].describe().T
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>punumber</th>
      <td>17.00</td>
      <td>112067204.47</td>
      <td>1473501.27</td>
      <td>111000415.00</td>
      <td>111009615.00</td>
      <td>111017315.00</td>
      <td>114001715.00</td>
      <td>114006518.00</td>
    </tr>
    <tr>
      <th>refundable_support</th>
      <td>17.00</td>
      <td>16705882.35</td>
      <td>20064784.78</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>10000000.00</td>
      <td>20000000.00</td>
      <td>60000000.00</td>
    </tr>
    <tr>
      <th>nonrefundable_support</th>
      <td>17.00</td>
      <td>65174674.41</td>
      <td>61236204.09</td>
      <td>0.00</td>
      <td>23000000.00</td>
      <td>51000000.00</td>
      <td>75000000.00</td>
      <td>250000000.00</td>
    </tr>
    <tr>
      <th>budget</th>
      <td>17.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>ratings</th>
      <td>16.00</td>
      <td>5.72</td>
      <td>0.92</td>
      <td>4.30</td>
      <td>5.07</td>
      <td>5.70</td>
      <td>6.30</td>
      <td>7.80</td>
    </tr>
    <tr>
      <th>box_office</th>
      <td>17.00</td>
      <td>163137294.43</td>
      <td>251115991.43</td>
      <td>1334699.40</td>
      <td>50451949.00</td>
      <td>72937783.20</td>
      <td>184487551.40</td>
      <td>1038321489.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
incorrect_budget = df[df['budget'] < (df['refundable_support'] + df['nonrefundable_support'])]
incorrect_budget.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2053</th>
      <td>14+</td>
      <td>111023614.00</td>
      <td>2014-12-19 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО Киностудия  "Сентябрь"</td>
      <td>Россия</td>
      <td>А.Зайцев</td>
      <td>О.Гранина, А.Зайцев</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>23000000.00</td>
      <td>0.00</td>
      <td>Министерство культуры, Фонд кино</td>
      <td>6.60</td>
      <td>мелодрама</td>
      <td>10234016.10</td>
    </tr>
    <tr>
      <th>2058</th>
      <td>Дуxless 2</td>
      <td>111000415.00</td>
      <td>2015-01-26 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Киностудия "Слово", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>Р.Прыгунов</td>
      <td>П.Ануров, Ф.Бондарчук, Д.Рудовский</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>75000000.00</td>
      <td>0.00</td>
      <td>Фонд кино</td>
      <td>6.60</td>
      <td>драма</td>
      <td>446163511.00</td>
    </tr>
    <tr>
      <th>2472</th>
      <td>Воин (2015)</td>
      <td>111017315.00</td>
      <td>2015-09-28 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Форпост Продакшн", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>А.Андрианов</td>
      <td>ООО "Арт Пикчерс Студия"</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>10000000.00</td>
      <td>70000000.00</td>
      <td>0.00</td>
      <td>Фонд кино</td>
      <td>7.80</td>
      <td>боевик,драма,криминал</td>
      <td>196572438.40</td>
    </tr>
    <tr>
      <th>2532</th>
      <td>Бармен.</td>
      <td>111009615.00</td>
      <td>2015-05-26 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>АО "ВайТ Медиа", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>Д.Штурманова</td>
      <td>Т.Вайнштейн</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>20000000.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>Фонд кино</td>
      <td>6.20</td>
      <td>комедия,фэнтези</td>
      <td>67418974.80</td>
    </tr>
    <tr>
      <th>2615</th>
      <td>Савва. Сердце воина</td>
      <td>114001715.00</td>
      <td>2015-07-21 12:00:00+00:00</td>
      <td>Анимационный</td>
      <td>ООО "Глюкоза Продакшн", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>М.Фадеев</td>
      <td>А.Чистяков</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>60000000.00</td>
      <td>100000000.00</td>
      <td>0.00</td>
      <td>Фонд кино</td>
      <td>4.60</td>
      <td>мультфильм,приключения,фэнтези</td>
      <td>184487551.40</td>
    </tr>
    <tr>
      <th>2684</th>
      <td>Тряпичный союз</td>
      <td>111010215.00</td>
      <td>2015-06-08 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Кинокомпания "КОКТЕБЕЛЬ"</td>
      <td>Россия</td>
      <td>М.Местецкий</td>
      <td>Р.Борисевич, А.Кушаев</td>
      <td>«18+» - запрещено для детей</td>
      <td>0.00</td>
      <td>59000000.00</td>
      <td>0.00</td>
      <td>Фонд кино</td>
      <td>6.30</td>
      <td>комедия,драма</td>
      <td>1957738.51</td>
    </tr>
    <tr>
      <th>2788</th>
      <td>Срочно выйду замуж</td>
      <td>111017115.00</td>
      <td>2015-09-30 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>АО "ВайТ Медиа", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>С Чекалов</td>
      <td>Ф.Бондарчук, Т.Вайнштейн, Д.Рудовский</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>35000000.00</td>
      <td>0.00</td>
      <td>Фонд кино</td>
      <td>5.10</td>
      <td>комедия,мелодрама</td>
      <td>72937783.20</td>
    </tr>
    <tr>
      <th>2874</th>
      <td>Помню - не помню!</td>
      <td>111004916.00</td>
      <td>2016-03-01 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "КиноФирма"</td>
      <td>Россия</td>
      <td>В.Ровенский</td>
      <td>ООО "КиноФирма"</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>6000000.00</td>
      <td>0.00</td>
      <td>Министерство культуры</td>
      <td>4.30</td>
      <td>комедия</td>
      <td>15362931.43</td>
    </tr>
    <tr>
      <th>3047</th>
      <td>Любовь с ограничениями</td>
      <td>111008216.00</td>
      <td>2016-04-29 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>АО "ВайТ Медиа", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>Д.Тюрин</td>
      <td>Ф.Бондарчук, Т.Вайнштейн, Д.Рудовский</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>19000000.00</td>
      <td>51000000.00</td>
      <td>0.00</td>
      <td>Фонд кино</td>
      <td>6.30</td>
      <td>комедия,мелодрама</td>
      <td>70299052.00</td>
    </tr>
    <tr>
      <th>3565</th>
      <td>Притяжение (2016)</td>
      <td>111018116.00</td>
      <td>2016-12-16 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Водород 2011",  ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>Ф.Бондарчук</td>
      <td>ООО "Арт Пикчерс Студия"</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>250000000.00</td>
      <td>0.00</td>
      <td>Фонд кино</td>
      <td>5.60</td>
      <td>фантастика</td>
      <td>1038321489.00</td>
    </tr>
  </tbody>
</table>
</div>



**Вывод:** 

Значений с данными аномалиями в данных немного - 17 штук. Попробуем заполнить значения нулевого бюджета установив зависимость общего бюджета от размера господдержки (суммы возвратных средств и невозвратных средств) и восстановим данные исходя из этого.

#### Подсчет средней доли господдержки в общем бюджете фильмов


```python
df['support_percentage'] = (df['refundable_support'] + df['nonrefundable_support']) / df['budget']
df['support_percentage'] = df['support_percentage'].replace(np.inf, np.nan)

print('Средняя доля господдержки в общем бюджете фильма составляет:', df['support_percentage'].mean())
```

    Средняя доля господдержки в общем бюджете фильма составляет: 0.517385819769894
    


```python
df.loc[incorrect_budget.index, 'budget'] = (df.loc[incorrect_budget.index, 'refundable_support'] + df.loc[incorrect_budget.index, 'nonrefundable_support']) / df['support_percentage'].mean()
df.loc[incorrect_budget.index].head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
      <th>support_percentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2053</th>
      <td>14+</td>
      <td>111023614.00</td>
      <td>2014-12-19 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО Киностудия  "Сентябрь"</td>
      <td>Россия</td>
      <td>А.Зайцев</td>
      <td>О.Гранина, А.Зайцев</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>23000000.00</td>
      <td>44454252.75</td>
      <td>Министерство культуры, Фонд кино</td>
      <td>6.60</td>
      <td>мелодрама</td>
      <td>10234016.10</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2058</th>
      <td>Дуxless 2</td>
      <td>111000415.00</td>
      <td>2015-01-26 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Киностудия "Слово", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>Р.Прыгунов</td>
      <td>П.Ануров, Ф.Бондарчук, Д.Рудовский</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>75000000.00</td>
      <td>144959519.83</td>
      <td>Фонд кино</td>
      <td>6.60</td>
      <td>драма</td>
      <td>446163511.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2472</th>
      <td>Воин (2015)</td>
      <td>111017315.00</td>
      <td>2015-09-28 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Форпост Продакшн", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>А.Андрианов</td>
      <td>ООО "Арт Пикчерс Студия"</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>10000000.00</td>
      <td>70000000.00</td>
      <td>154623487.82</td>
      <td>Фонд кино</td>
      <td>7.80</td>
      <td>боевик,драма,криминал</td>
      <td>196572438.40</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2532</th>
      <td>Бармен.</td>
      <td>111009615.00</td>
      <td>2015-05-26 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>АО "ВайТ Медиа", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>Д.Штурманова</td>
      <td>Т.Вайнштейн</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>20000000.00</td>
      <td>0.00</td>
      <td>38655871.95</td>
      <td>Фонд кино</td>
      <td>6.20</td>
      <td>комедия,фэнтези</td>
      <td>67418974.80</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2615</th>
      <td>Савва. Сердце воина</td>
      <td>114001715.00</td>
      <td>2015-07-21 12:00:00+00:00</td>
      <td>Анимационный</td>
      <td>ООО "Глюкоза Продакшн", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>М.Фадеев</td>
      <td>А.Чистяков</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>60000000.00</td>
      <td>100000000.00</td>
      <td>309246975.63</td>
      <td>Фонд кино</td>
      <td>4.60</td>
      <td>мультфильм,приключения,фэнтези</td>
      <td>184487551.40</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2684</th>
      <td>Тряпичный союз</td>
      <td>111010215.00</td>
      <td>2015-06-08 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Кинокомпания "КОКТЕБЕЛЬ"</td>
      <td>Россия</td>
      <td>М.Местецкий</td>
      <td>Р.Борисевич, А.Кушаев</td>
      <td>«18+» - запрещено для детей</td>
      <td>0.00</td>
      <td>59000000.00</td>
      <td>114034822.27</td>
      <td>Фонд кино</td>
      <td>6.30</td>
      <td>комедия,драма</td>
      <td>1957738.51</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2788</th>
      <td>Срочно выйду замуж</td>
      <td>111017115.00</td>
      <td>2015-09-30 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>АО "ВайТ Медиа", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>С Чекалов</td>
      <td>Ф.Бондарчук, Т.Вайнштейн, Д.Рудовский</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>35000000.00</td>
      <td>67647775.92</td>
      <td>Фонд кино</td>
      <td>5.10</td>
      <td>комедия,мелодрама</td>
      <td>72937783.20</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2874</th>
      <td>Помню - не помню!</td>
      <td>111004916.00</td>
      <td>2016-03-01 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "КиноФирма"</td>
      <td>Россия</td>
      <td>В.Ровенский</td>
      <td>ООО "КиноФирма"</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>6000000.00</td>
      <td>11596761.59</td>
      <td>Министерство культуры</td>
      <td>4.30</td>
      <td>комедия</td>
      <td>15362931.43</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3047</th>
      <td>Любовь с ограничениями</td>
      <td>111008216.00</td>
      <td>2016-04-29 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>АО "ВайТ Медиа", ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>Д.Тюрин</td>
      <td>Ф.Бондарчук, Т.Вайнштейн, Д.Рудовский</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>19000000.00</td>
      <td>51000000.00</td>
      <td>135295551.84</td>
      <td>Фонд кино</td>
      <td>6.30</td>
      <td>комедия,мелодрама</td>
      <td>70299052.00</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3565</th>
      <td>Притяжение (2016)</td>
      <td>111018116.00</td>
      <td>2016-12-16 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Водород 2011",  ООО "Арт Пикчерс Студия"</td>
      <td>Россия</td>
      <td>Ф.Бондарчук</td>
      <td>ООО "Арт Пикчерс Студия"</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>250000000.00</td>
      <td>483198399.43</td>
      <td>Фонд кино</td>
      <td>5.60</td>
      <td>фантастика</td>
      <td>1038321489.00</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



**Вывод:** 

Выявили аномалии в столбце budget у тех картин, где бюджет составлял 0 руб, несмотря на существующую возвратную и/или невозвратную господдержку которая исходя из описания данных должна была войти в сумму бюджета. Исходя из информации представленной на сайте Государственная поддержка фильмов, данные нулевые значения могут соответствовать случаям когда данные не предоставлены правообладателем. 

Мною было предложено заменить небольшое количество аномалий в нулевом бюджете, посчитав долю господдержки в общем бюджете каждого фильма по нашему датасету. Ручной поиск по бюджетам фильмов на сайте Кинопоиск показал что результаты такой замены могут быть близки к реальному.

### Добавление новых столбцов

- Создадим столбец с информацией о годе проката. Выделите год из даты премьеры фильма.


```python
# используем метод dt.year для формата дата-время

df['show_year'] = df['show_start_date'].dt.year
df.sample(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
      <th>support_percentage</th>
      <th>show_year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>5227</th>
      <td>38-я параллель</td>
      <td>221059311.00</td>
      <td>2011-04-27 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Кан Чжэ Гю Филм Компани</td>
      <td>РеспубликаКорея</td>
      <td>Кан Чжэ Гю</td>
      <td>Сем Хан Ли</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.90</td>
      <td>военный,боевик,драма</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2011</td>
    </tr>
    <tr>
      <th>2650</th>
      <td>Иррациональный человек</td>
      <td>121015515.00</td>
      <td>2015-07-20 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Гравье Продакшнз</td>
      <td>США</td>
      <td>Вуди Аллен</td>
      <td>Летти Аронсон, Стивен Тененбаум, Эдвард Уолсон</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.80</td>
      <td>драма,мелодрама,комедия</td>
      <td>44077507.80</td>
      <td>NaN</td>
      <td>2015</td>
    </tr>
    <tr>
      <th>1623</th>
      <td>По признакам совместимости</td>
      <td>121028013.00</td>
      <td>2013-11-01 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Вижн Филмз, Квартц Филмз, Упс Донатс Продакшнз...</td>
      <td>США</td>
      <td>Брайан Фогель</td>
      <td>Дэн Кестон, Кортни Мизел, Павлина Хатупис</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5.40</td>
      <td>мелодрама,комедия</td>
      <td>1240.00</td>
      <td>NaN</td>
      <td>2013</td>
    </tr>
    <tr>
      <th>284</th>
      <td>Сомнение /По одноименной пьесе Джона Патрика Ш...</td>
      <td>221059114.00</td>
      <td>2014-10-15 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Скотт Рудин Продакшнз, Гудспид Продакшнз</td>
      <td>США</td>
      <td>Джон Патрик Шэнли</td>
      <td>Марк Ройбал, Скотт Рудин</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.40</td>
      <td>драма,детектив</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2014</td>
    </tr>
    <tr>
      <th>3443</th>
      <td>Космос между нами</td>
      <td>121035516.00</td>
      <td>2016-12-30 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Лос Анджелес Медиа Фанд, Эс Ти Икс Интертейнме...</td>
      <td>США</td>
      <td>Питер Челсом</td>
      <td>Джон Албанис, Ричард Бартон Льюис, Робби Бреннер</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.50</td>
      <td>фантастика,драма,мелодрама</td>
      <td>32894785.00</td>
      <td>NaN</td>
      <td>2016</td>
    </tr>
  </tbody>
</table>
</div>



- Создадим два столбца: с именем и фамилией главного режиссёра и основным жанром фильма. В столбцы войдут первые значения из списка режиссёров и жанров соответственно.



```python
# создадим столбец с именем главного режиссера

df_director=df['director'].str.split(',',expand=True)
df['director_first']=df_director[0]

# создадим столбец с названием главного жанра

df_genres=df['genres'].str.split(',',expand=True)
df['genres_first']=df_genres[0]
df.sample(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
      <th>support_percentage</th>
      <th>show_year</th>
      <th>director_first</th>
      <th>genres_first</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3342</th>
      <td>Уедем к чертовой бабушке</td>
      <td>121010817.00</td>
      <td>2017-06-05 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Трамп</td>
      <td>Италия</td>
      <td>Валентино Пиконе, Сальваторе Фикарра</td>
      <td>NaN</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.20</td>
      <td>комедия</td>
      <td>1455562.00</td>
      <td>NaN</td>
      <td>2017</td>
      <td>Валентино Пиконе</td>
      <td>комедия</td>
    </tr>
    <tr>
      <th>5313</th>
      <td>Ключ от всех дверей</td>
      <td>221088210.00</td>
      <td>2010-09-10 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Брик Даст Продакшнз, Дэниэл Бобкер Продакшнз, ...</td>
      <td>США</td>
      <td>Йен Софтли</td>
      <td>Дэниэл Бобкер, Йен Софтли,  Майкл Шамберг, Сте...</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.40</td>
      <td>ужасы,триллер,драма</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2010</td>
      <td>Йен Софтли</td>
      <td>ужасы</td>
    </tr>
    <tr>
      <th>2489</th>
      <td>Последний вагон. Весна</td>
      <td>111004115.00</td>
      <td>2015-04-15 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "ТАН Фильм"</td>
      <td>Россия</td>
      <td>А.Калинкин</td>
      <td>Д.Ефремов, В.Пономаренко</td>
      <td>«18+» - запрещено для детей</td>
      <td>0.00</td>
      <td>25000000.00</td>
      <td>35760060.00</td>
      <td>Министерство культуры</td>
      <td>5.10</td>
      <td>триллер</td>
      <td>61193.00</td>
      <td>0.70</td>
      <td>2015</td>
      <td>А.Калинкин</td>
      <td>триллер</td>
    </tr>
    <tr>
      <th>2464</th>
      <td>Наваждение (2015)</td>
      <td>126002815.00</td>
      <td>2015-09-11 12:00:00+00:00</td>
      <td>Прочие</td>
      <td>Джугсоу Продакшнз, Скай Атлантик, Эйч Би Оу До...</td>
      <td>США</td>
      <td>Алекс Гибни</td>
      <td>Кристин Ваурио, Алекс Гибни, Лоуренс Райт</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.30</td>
      <td>документальный</td>
      <td>1954807.00</td>
      <td>NaN</td>
      <td>2015</td>
      <td>Алекс Гибни</td>
      <td>документальный</td>
    </tr>
    <tr>
      <th>2896</th>
      <td>Громче, чем бомбы</td>
      <td>121007516.00</td>
      <td>2016-04-01 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>Мотлис, Энимал Кингдом, Арт Франс Синема, Бичс...</td>
      <td>Франция,США,Норвегия,Дания</td>
      <td>Йоаким Триер</td>
      <td>Джошуа Астрачан, , Альберт Бергер, Рон Йеркса,...</td>
      <td>«18+» - запрещено для детей</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.50</td>
      <td>драма</td>
      <td>2925092.01</td>
      <td>NaN</td>
      <td>2016</td>
      <td>Йоаким Триер</td>
      <td>драма</td>
    </tr>
  </tbody>
</table>
</div>



#### Посчитаем, какую долю от общего бюджета фильма составляет государственная поддержка


```python
# долю господдержки вычислим как отношение суммы возвратных и невозвратных средств
# господдержки к общему бюджету; используем замену бесконечных значений на NaN из-за деления на ноль

df['support_percentage'] = (df['refundable_support'] + df['nonrefundable_support']) / df['budget']
df['support_percentage'] = df['support_percentage'].replace(np.inf, np.nan)

print('Средняя доля господдержки от общего бюджета фильма составляет:', df['support_percentage'].mean())
```

    Средняя доля господдержки от общего бюджета фильма составляет: 0.5173858197698938
    

**Вывод:** 

Медианная величина бюджета фильма с гос. поддержкой составляет около 71 млн руб, в то время как средняя величина составляет 133 млн руб. Это свидетельствует о том, что есть некоторые фильмы, снятые с гос. поддержкой, с очень значительным бюджетом. Их бюджет повлиял на среднюю величину, но не затронул значение медианного бюджета.

Объем средств гос. поддержки в среднем составляет около 35 млн руб, т.е. около 52% от бюджета фильма. Причем гос. поддержка в основном представляет собой именно невозвратные средства в размере около 30 млн руб.

## Исследовательский анализ данных


- Посмотрим, сколько фильмов выходило в прокат каждый год. Обратим внимание, что данные о прокате в кинотеатрах известны не для всех фильмов. Посчитаем, какую долю составляют фильмы с указанной информацией о прокате в кинотеатрах. Проанализируем, как эта доля менялась по годам. Сделаем вывод о том, какой период полнее всего представлен в данных.


```python
# строим сводную таблицу для всех фильмов где известны данные о прокате

df_pivot = df.loc[df['box_office'].notna(), ['show_year', 'box_office']] \
                .groupby('show_year') \
                .agg(['count', 'sum', 'mean', 'median'])

# избавляемся от мультииндекса

df_pivot.columns = df_pivot.columns.get_level_values(1)
df_pivot.reset_index()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>show_year</th>
      <th>count</th>
      <th>sum</th>
      <th>mean</th>
      <th>median</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2010</td>
      <td>105</td>
      <td>2428654.00</td>
      <td>23130.04</td>
      <td>1700.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2011</td>
      <td>109</td>
      <td>14102765.00</td>
      <td>129383.17</td>
      <td>3000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2012</td>
      <td>128</td>
      <td>6955423.00</td>
      <td>54339.24</td>
      <td>5660.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013</td>
      <td>184</td>
      <td>29799706.20</td>
      <td>161954.92</td>
      <td>3522.50</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014</td>
      <td>279</td>
      <td>7444951859.20</td>
      <td>26684415.27</td>
      <td>18160.00</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2015</td>
      <td>465</td>
      <td>39497365196.40</td>
      <td>84940570.31</td>
      <td>4920933.00</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2016</td>
      <td>526</td>
      <td>47866299741.91</td>
      <td>91000569.85</td>
      <td>3846679.41</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2017</td>
      <td>357</td>
      <td>48563707217.51</td>
      <td>136032793.33</td>
      <td>9968340.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2018</td>
      <td>475</td>
      <td>49668403134.32</td>
      <td>104565059.23</td>
      <td>8891102.21</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2019</td>
      <td>530</td>
      <td>48425708779.59</td>
      <td>91369261.85</td>
      <td>4627798.34</td>
    </tr>
  </tbody>
</table>
</div>




```python
# сгруппируем данные и визуализируем количество фильмов по годам
# используем удобный для визуалиции стиль и настроим параметры сетки, цвета и размера шрифта

plt.style.use('ggplot')

# среднее пропущенных значений с сортировкой по убыванию

df.groupby('show_year')['box_office'].count().plot(
    kind='bar', figsize=(12,6), 
    grid=True, color='midnightblue', 
    edgecolor='black', linewidth=1,
)
plt.title('Количество фильмов в прокате по годам',fontsize=14, fontweight="bold")
plt.xticks(rotation = 45, fontsize = 13)
plt.xlabel('Год показа',fontweight="bold")
plt.ylabel('Количество фильмов', fontweight="bold")
plt.show()
```


    
![png](output_120_0.png)
    



```python
# исключим значения NaN при подсчете доли

print(f'Доля фильмов с указанной информацией о прокате в кинотеатрах составляет: {df.box_office.notna().mean():.2f}')
```

    Доля фильмов с указанной информацией о прокате в кинотеатрах составляет: 0.42
    


```python
# посмотрим, сколько фильмов выходило в прокат В КИНОТЕАТРАХ каждый год

cinema=df.groupby('show_year')['box_office'].count()
cinema=cinema.to_frame().reset_index()
cinema.rename(columns={'box_office':'number_of_films_cinema'}, inplace=True)
cinema
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>show_year</th>
      <th>number_of_films_cinema</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2010</td>
      <td>105</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2011</td>
      <td>109</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2012</td>
      <td>128</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013</td>
      <td>184</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014</td>
      <td>279</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2015</td>
      <td>465</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2016</td>
      <td>526</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2017</td>
      <td>357</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2018</td>
      <td>475</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2019</td>
      <td>530</td>
    </tr>
  </tbody>
</table>
</div>




```python
# посмотрим, сколько фильмов выходило в целом в прокат каждый год и объединим с данными в кинотеатрах

films=df.groupby('show_year')['title'].count()
films=films.to_frame().reset_index()
films.rename(columns={'title':'number_of_films'}, inplace=True)
films['number_of_films_cinema']=cinema['number_of_films_cinema']
films['%_of_cinema']=films['number_of_films_cinema']/films['number_of_films']
display(films)

# рассчитаем среднее количество фильмов в год

print('Cреднее количество фильмов в год: %.0f' % films['number_of_films'].mean())
print('Cреднее количество фильмов в кинотеатрах в год: %.0f' % cinema['number_of_films_cinema'].mean())
print('Доля фильмов с указанной информацией о прокате в кинотеатрах: %.2f' % films['%_of_cinema'].mean())
```


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>show_year</th>
      <th>number_of_films</th>
      <th>number_of_films_cinema</th>
      <th>%_of_cinema</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2010</td>
      <td>985</td>
      <td>105</td>
      <td>0.11</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2011</td>
      <td>622</td>
      <td>109</td>
      <td>0.18</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2012</td>
      <td>593</td>
      <td>128</td>
      <td>0.22</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013</td>
      <td>630</td>
      <td>184</td>
      <td>0.29</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014</td>
      <td>807</td>
      <td>279</td>
      <td>0.35</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2015</td>
      <td>705</td>
      <td>465</td>
      <td>0.66</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2016</td>
      <td>818</td>
      <td>526</td>
      <td>0.64</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2017</td>
      <td>505</td>
      <td>357</td>
      <td>0.71</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2018</td>
      <td>891</td>
      <td>475</td>
      <td>0.53</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2019</td>
      <td>930</td>
      <td>530</td>
      <td>0.57</td>
    </tr>
  </tbody>
</table>
</div>


    Cреднее количество фильмов в год: 749
    Cреднее количество фильмов в кинотеатрах в год: 316
    Доля фильмов с указанной информацией о прокате в кинотеатрах: 0.42
    


```python
# построим барчарт по данным о прокате в целом, и о прокате В КИНОТЕАТРАХ

films.plot(x='show_year', kind='bar', figsize = (10, 5), grid = True, title='Количество фильмов по годам')
```




    <Axes: title={'center': 'Количество фильмов по годам'}, xlabel='show_year'>




    
![png](output_124_1.png)
    



```python
films.plot(x='show_year', y='%_of_cinema', figsize = (10, 5), grid = True, title='Доля фильмов с указанной информацией о прокате в кинотеатрах')
```




    <Axes: title={'center': 'Доля фильмов с указанной информацией о прокате в кинотеатрах'}, xlabel='show_year'>




    
![png](output_125_1.png)
    


**Вывод**

Данные о прокате в кинотеатрах известны не для всех фильмов, это означает, что часть фильмов получили удостоверение на прокат на ТВ. В среднем, в прокат в целом выходило около 749 фильмов в год, а в прокат В КИНОТЕАТРЫ выходило в 2 раза меньше - 316 фильмов в год. В целом, количество фильмов, выходивших в прокат стабильно, чего не скажешь про количество фильмов, выходивших в прокат В КИНОТЕАТРАХ - оно стабильно растет. Меньше всего фильмов вышло в прокат В КИНОТЕАТРАХ в 2010 году (это начало исследуемого периода) - всего 105 фильмов. Затем это количество постепенно увеличивалось до 526 в 2016 году. На следующий год количество фильмов упало до 357, а затем в течение еще 3 лет постепенно увеличивалось до 530 фильмов в 2019 году (это максимум). В целом, можно утверждать, что и количество фильмов, вышедших в прокат В КИНОТЕАТРАХ, и доля фильмов с указанной информацией о прокате в кинотеатрах стабильно растет. 
Это, может быть, связано со следующими факторами:

- начиная с 2014-2015 активно начали развиваться он-лайн кинотеатры (типа Okko, Ivi и т.д.), благодаря чему выросло количество кассовых сборов кинотеатров;
- также благодаря цифровым технологиям даёт свои плоды многолетняя борьба с пиратством - людям проще заплатить теперь за фильм в хорошем качестве, чем пытаться найти его для росмотра на бесплатном ресурсе;
- как вариант, можно рассмотреть влияние стоимости прокатных удостоверений - возможно в последние годы стоиомость прокатного удостоверения в кинотеатры могла снизиться.

**Изучим, как менялась динамика проката по годам. В каком году сумма сборов была минимальной? А максимальной?**


```python
# сгруппируем данные по годам и применим суммирование вырученых средств от проката
# используем удобный для визуалиции стиль и настроим параметры сетки, цвета и размера шрифта

df.groupby('show_year')['box_office'].agg('sum').plot(
    x='year', style='o-', figsize=(15, 6), legend = True, color='midnightblue')

plt.ticklabel_format(style='plain')

plt.title('Изменение проката фильмов по годам', fontsize=14, fontweight="bold")
plt.xlabel('Год проката', fontweight="bold")
plt.ylabel('Сборы от проката в руб.', fontweight="bold" )
plt.show()

print(f"В {df_pivot['sum'].idxmin()} году сумма сборов была минимальной, в {df_pivot['sum'].idxmax()} максимальной.")
```


    
![png](output_128_0.png)
    


    В 2010 году сумма сборов была минимальной, в 2018 максимальной.
    

**Вывод:** 

Учитывая сумму сборов по годам, из графика видим как максимум приходится на 2018 год. Года с 2010 по 2013 в расчет не берем, так как по ним меньше всего значений в данных. Будем считать что минимум сборов приходится на 2014 год. В России каждый год растет число кинотеатров и кинозалов, а вместе с ними — число новых релизов. Стимулировал этот рост также переход прокатчиков от пленки к цифровому показу, завершившийся в 2015 году.

 **С помощью сводной таблицы посчитайте среднюю и медианную сумму сборов для каждого года**


```python
df_pivot[['mean','median']].reset_index()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>show_year</th>
      <th>mean</th>
      <th>median</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2010</td>
      <td>23130.04</td>
      <td>1700.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2011</td>
      <td>129383.17</td>
      <td>3000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2012</td>
      <td>54339.24</td>
      <td>5660.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2013</td>
      <td>161954.92</td>
      <td>3522.50</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2014</td>
      <td>26684415.27</td>
      <td>18160.00</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2015</td>
      <td>84940570.31</td>
      <td>4920933.00</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2016</td>
      <td>91000569.85</td>
      <td>3846679.41</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2017</td>
      <td>136032793.33</td>
      <td>9968340.00</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2018</td>
      <td>104565059.23</td>
      <td>8891102.21</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2019</td>
      <td>91369261.85</td>
      <td>4627798.34</td>
    </tr>
  </tbody>
</table>
</div>




```python
# используем удобный для визуалиции стиль и настроим параметры сетки, цвета и размера шрифта

plt.style.use('ggplot')

df_pivot.plot(y=['median','mean'], style='-o', figsize=(12, 6), color=['midnightblue','orange'],legend = True)

plt.ticklabel_format(style='plain')

plt.title('Средняя и медиана сборов для каждого года', fontsize=14, fontweight="bold")
plt.xlabel('Год проката', fontweight="bold")
plt.ylabel('Сборы от проката в руб.', fontweight="bold" )
plt.show()
```


    
![png](output_132_0.png)
    


**Вывод:**

Наблюдаем что для сборов каждого года очень большой разброс данных. Это можно заметить из разницы между средней и медианой. Это означает, что в данных присутствуют значения с очень большими сборами по сравнению с остальными. Для кино это нормальное явление. В среднем, самый прибыльный год может считаться 2017. Это видно и по медиане, и по средней.

**Определим, влияет ли возрастное ограничение аудитории («6+», «12+», «16+», «18+» и т. д.) на сборы фильма в прокате в период с 2015 по 2019 год? Фильмы с каким возрастным ограничением собрали больше всего денег в прокате? Меняется ли картина в зависимости от года? Если да, предположите, с чем это может быть связано.**

Посмотрим фильмы с каким возрастным ограничением собрали больше всего денег в прокате? Менялась ли картина в зависимости от года? Если да, с чем это могло быть связано?


```python
# построим сводную таблицу отфильтровав значения методом query

df.query('show_year >= 2015').groupby('age_restriction')['box_office'].sum().round().to_frame().reset_index()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age_restriction</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>809077426.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>«12+» - для детей старше 12 лет</td>
      <td>60619446628.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>«16+» - для детей старше 16 лет</td>
      <td>76034733644.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>«18+» - запрещено для детей</td>
      <td>40759615572.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>«6+» - для детей старше 6 лет</td>
      <td>55798610800.00</td>
    </tr>
  </tbody>
</table>
</div>




```python
age_restriction_data = df.query('show_year>2014').groupby('age_restriction')['box_office'].sum()
age_restriction_data = age_restriction_data.sort_values()
age_restriction_data.plot(kind='barh', grid=True)
plt.title('Кассовые сборы по возрастной категории')
plt.xlabel('Года')
plt.ylabel('Кассовые сборы')
```




    Text(0, 0.5, 'Кассовые сборы')




    
![png](output_137_1.png)
    


**Вывод:** 

Из полученной сводной таблицы видим, что в период с 2015 по 2019 год больше всего кассовых сборов у фильмов категории «16+» - для детей старше 16 лет.

**Посмотрим как менялась картина в зависимости от года c помощью сводной таблицы.**


```python
# отфильтруем значения от 2015 года и позднее и сгруппируем данные по возрастной категории

df_age = df.query('2015 <= show_year').groupby(['show_year', 'age_restriction'])['box_office'] \
                             .agg('sum').reset_index()
df_age
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>show_year</th>
      <th>age_restriction</th>
      <th>box_office</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2015</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>379054578.37</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2015</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>13616082008.91</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2015</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>11368120870.27</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2015</td>
      <td>«18+» - запрещено для детей</td>
      <td>5432308367.44</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2015</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>8701799371.41</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2016</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>150228848.67</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2016</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>12204446524.39</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2016</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>16664548541.74</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2016</td>
      <td>«18+» - запрещено для детей</td>
      <td>6793929818.87</td>
    </tr>
    <tr>
      <th>9</th>
      <td>2016</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>12053146008.24</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2017</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>229598930.00</td>
    </tr>
    <tr>
      <th>11</th>
      <td>2017</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>7851427660.67</td>
    </tr>
    <tr>
      <th>12</th>
      <td>2017</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>18745042900.06</td>
    </tr>
    <tr>
      <th>13</th>
      <td>2017</td>
      <td>«18+» - запрещено для детей</td>
      <td>9651495581.02</td>
    </tr>
    <tr>
      <th>14</th>
      <td>2017</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>12086142145.76</td>
    </tr>
    <tr>
      <th>15</th>
      <td>2018</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>32449002.11</td>
    </tr>
    <tr>
      <th>16</th>
      <td>2018</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>14267291660.69</td>
    </tr>
    <tr>
      <th>17</th>
      <td>2018</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>16503602346.96</td>
    </tr>
    <tr>
      <th>18</th>
      <td>2018</td>
      <td>«18+» - запрещено для детей</td>
      <td>8760085501.15</td>
    </tr>
    <tr>
      <th>19</th>
      <td>2018</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>10104974623.41</td>
    </tr>
    <tr>
      <th>20</th>
      <td>2019</td>
      <td>«0+» - для любой зрительской аудитории</td>
      <td>17746066.82</td>
    </tr>
    <tr>
      <th>21</th>
      <td>2019</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>12680198773.67</td>
    </tr>
    <tr>
      <th>22</th>
      <td>2019</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>12753418984.60</td>
    </tr>
    <tr>
      <th>23</th>
      <td>2019</td>
      <td>«18+» - запрещено для детей</td>
      <td>10121796303.64</td>
    </tr>
    <tr>
      <th>24</th>
      <td>2019</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>12852548650.86</td>
    </tr>
  </tbody>
</table>
</div>




```python
# визуализируем данные с помощью столбчатых диаграмм по возрастным категориям

plt.style.use("dark_background")
sns.color_palette("Set2")

sns.catplot(x='show_year', y='box_office', hue='age_restriction', data=df_age, kind='bar', height=8);

plt.ticklabel_format(axis="y", style="plain")
plt.title('Влияние возрастного ограничения на сумму сборов', fontweight="bold");
plt.xlabel('Год', fontweight="bold");
plt.ylabel('Сумма сборов в рублях', fontweight="bold");
```

    C:\Users\gella\anaconda3\Lib\site-packages\seaborn\axisgrid.py:118: UserWarning: The figure layout has changed to tight
      self._figure.tight_layout(*args, **kwargs)
    


    
![png](output_141_1.png)
    


**Вывод:** 

После полученной визуализации мы наблюдаем что в 2016-2018 гг наибольшее количество сборов было получено от картин попадающих в возрастную категорию «16+» - для детей старше 16 лет, а в 2015 в лидерах оказалось кино 12+. В 2019 году динамика немного изменилась и все категории оказались примерно на одинаковом уровне. Можно предположить что у фильмов, рассчитанных на молодую аудиторию, возрастные ограничения могли сыграть важную роль и отразиться на сборах. И разница между "16+" и "18+" будет уже существенной. При этом возрастной рейтинг может сильно осложнить жизнь как прокатчикам, так и зрителям. 

Раз на раз не приходится, но во многих кинотеатрах, особенно в провинциях, распоряжения Минкульта соблюдаются крайне строго, и 11-летним детям, например, не продают билеты на «Доктора Стрэнджа», а родителей, пришедших на «Стражей Галактики» с 9-летними детьми заставляют у кассы писать расписку, дескать, они осознают, на что они ведут своего ребенка. Возможными причинами могут являться также изменения в законодательстве и поправки к возрастным ограничениям, которые принимались в период 2015-2019 гг.

## Исследование фильмов, получившие государственную поддержку

Выявим интересные закономерности в данных на которые стоит обратить внимание. Посмотрим, сколько выделяют средств на поддержку кино. Проверм, хорошо ли окупаются такие фильмы, какой у них рейтинг.

### Поищем интересные закономерности в данных. Посмотрим, сколько выделяют средств на поддержку кино. Проверим, хорошо ли окупаются такие фильмы, какой у них рейтинг


```python
# выделим фильмы как с наличием возвратной так и невозвратной суммы господдержки; сохраним в отдельную переменную

df_financed = df[df['budget'].isna() == False]
df_financed = df_financed.drop(['punumber', 'show_start_date', 'film_studio', 'production_country', 'director', 'producer','genres'], axis=1)
df_financed
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>type</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>box_office</th>
      <th>support_percentage</th>
      <th>show_year</th>
      <th>director_first</th>
      <th>genres_first</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1281</th>
      <td>Пока еще жива</td>
      <td>Художественный</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>26500000.00</td>
      <td>79411900.00</td>
      <td>Министерство культуры</td>
      <td>8.10</td>
      <td>365353.60</td>
      <td>0.33</td>
      <td>2013</td>
      <td>А.Атанесян</td>
      <td>драма</td>
    </tr>
    <tr>
      <th>1448</th>
      <td>Бесславные придурки</td>
      <td>Художественный</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>26000000.00</td>
      <td>37142857.00</td>
      <td>Министерство культуры</td>
      <td>NaN</td>
      <td>28140.00</td>
      <td>0.70</td>
      <td>2014</td>
      <td>А.Якимчук</td>
      <td>unknown</td>
    </tr>
    <tr>
      <th>1498</th>
      <td>Невидимки</td>
      <td>Художественный</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>107847945.00</td>
      <td>176023490.00</td>
      <td>Фонд кино</td>
      <td>5.30</td>
      <td>19957031.50</td>
      <td>0.61</td>
      <td>2013</td>
      <td>Р.Давлетьяров</td>
      <td>комедия</td>
    </tr>
    <tr>
      <th>1524</th>
      <td>БЕРЦЫ</td>
      <td>Художественный</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>28000000.00</td>
      <td>40574140.00</td>
      <td>Министерство культуры</td>
      <td>4.20</td>
      <td>55917.50</td>
      <td>0.69</td>
      <td>2014</td>
      <td>Е.Миндадзе (псевдоним Катя Шагалова)</td>
      <td>драма</td>
    </tr>
    <tr>
      <th>1792</th>
      <td>Братья Ч</td>
      <td>Художественный</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>25000000.00</td>
      <td>40015122.00</td>
      <td>Министерство культуры</td>
      <td>6.40</td>
      <td>232100.00</td>
      <td>0.62</td>
      <td>2014</td>
      <td>М.Угаров</td>
      <td>драма</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>7464</th>
      <td>Союз спасения</td>
      <td>Художественный</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>100000000.00</td>
      <td>400000000.00</td>
      <td>980000000.00</td>
      <td>Фонд кино</td>
      <td>6.00</td>
      <td>717703185.53</td>
      <td>0.51</td>
      <td>2019</td>
      <td>А.Кравчук</td>
      <td>история</td>
    </tr>
    <tr>
      <th>7466</th>
      <td>Иван Царевич и Серый Волк 4</td>
      <td>Анимационный</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>100000000.00</td>
      <td>0.00</td>
      <td>190000000.00</td>
      <td>Фонд кино</td>
      <td>6.70</td>
      <td>501069235.00</td>
      <td>0.53</td>
      <td>2019</td>
      <td>Д.Шмидт</td>
      <td>мультфильм</td>
    </tr>
    <tr>
      <th>7474</th>
      <td>Вторжение</td>
      <td>Художественный</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>100000000.00</td>
      <td>400000000.00</td>
      <td>944000000.00</td>
      <td>Фонд кино</td>
      <td>5.70</td>
      <td>NaN</td>
      <td>0.53</td>
      <td>2019</td>
      <td>Ф.Бондарчук</td>
      <td>фантастика</td>
    </tr>
    <tr>
      <th>7476</th>
      <td>Я свободен</td>
      <td>Художественный</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>30000000.00</td>
      <td>46154000.00</td>
      <td>Министерство культуры</td>
      <td>5.90</td>
      <td>NaN</td>
      <td>0.65</td>
      <td>2019</td>
      <td>И.Северов</td>
      <td>драма</td>
    </tr>
    <tr>
      <th>7478</th>
      <td>(Не)идеальный мужчина</td>
      <td>Художественный</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>40000000.00</td>
      <td>60000000.00</td>
      <td>150147502.00</td>
      <td>Фонд кино</td>
      <td>4.50</td>
      <td>NaN</td>
      <td>0.67</td>
      <td>2019</td>
      <td>М.Бальчюнас (псевдоним М.Вайсберг)</td>
      <td>комедия</td>
    </tr>
  </tbody>
</table>
<p>332 rows × 13 columns</p>
</div>




```python
# создадим столбец с общей суммой государственной поддержки

df_financed['total_support'] = df_financed['refundable_support'] + df_financed['nonrefundable_support']
```


```python
# создадим столбец окупаемости картины как разницу между кассовыми сборами и бюджетом фильма

df_financed['payback'] = df_financed['box_office'] - df_financed['budget']
df_financed.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 332 entries, 1281 to 7478
    Data columns (total 15 columns):
     #   Column                 Non-Null Count  Dtype  
    ---  ------                 --------------  -----  
     0   title                  332 non-null    object 
     1   type                   332 non-null    object 
     2   age_restriction        332 non-null    object 
     3   refundable_support     332 non-null    float64
     4   nonrefundable_support  332 non-null    float64
     5   budget                 332 non-null    float64
     6   financing_source       332 non-null    object 
     7   ratings                314 non-null    float64
     8   box_office             318 non-null    float64
     9   support_percentage     315 non-null    float64
     10  show_year              332 non-null    int32  
     11  director_first         332 non-null    object 
     12  genres_first           332 non-null    object 
     13  total_support          332 non-null    float64
     14  payback                318 non-null    float64
    dtypes: float64(8), int32(1), object(6)
    memory usage: 40.2+ KB
    

### Исследуем поведение окупаемости фильмов с государственной поддержкой


```python
df_financed.describe().T
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>refundable_support</th>
      <td>332.00</td>
      <td>11864457.83</td>
      <td>24916555.26</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>15000000.00</td>
      <td>180000000.00</td>
    </tr>
    <tr>
      <th>nonrefundable_support</th>
      <td>332.00</td>
      <td>48980988.89</td>
      <td>59980117.92</td>
      <td>0.00</td>
      <td>25000000.00</td>
      <td>30000000.00</td>
      <td>40375000.00</td>
      <td>400000000.00</td>
    </tr>
    <tr>
      <th>budget</th>
      <td>332.00</td>
      <td>135333300.03</td>
      <td>188343992.03</td>
      <td>11596761.59</td>
      <td>46153971.75</td>
      <td>75000067.50</td>
      <td>151172048.25</td>
      <td>2305074303.00</td>
    </tr>
    <tr>
      <th>ratings</th>
      <td>314.00</td>
      <td>6.00</td>
      <td>1.12</td>
      <td>1.00</td>
      <td>5.30</td>
      <td>6.20</td>
      <td>6.70</td>
      <td>8.50</td>
    </tr>
    <tr>
      <th>box_office</th>
      <td>318.00</td>
      <td>132432420.05</td>
      <td>334837856.99</td>
      <td>1550.00</td>
      <td>1236675.50</td>
      <td>15720067.71</td>
      <td>106373008.27</td>
      <td>3073568690.79</td>
    </tr>
    <tr>
      <th>support_percentage</th>
      <td>315.00</td>
      <td>0.52</td>
      <td>0.17</td>
      <td>0.04</td>
      <td>0.37</td>
      <td>0.59</td>
      <td>0.66</td>
      <td>0.78</td>
    </tr>
    <tr>
      <th>show_year</th>
      <td>332.00</td>
      <td>2016.72</td>
      <td>1.64</td>
      <td>2013.00</td>
      <td>2015.00</td>
      <td>2017.00</td>
      <td>2018.00</td>
      <td>2019.00</td>
    </tr>
    <tr>
      <th>total_support</th>
      <td>332.00</td>
      <td>60845446.72</td>
      <td>72755459.47</td>
      <td>3000000.00</td>
      <td>25333750.00</td>
      <td>35000000.00</td>
      <td>60000000.00</td>
      <td>500000000.00</td>
    </tr>
    <tr>
      <th>payback</th>
      <td>318.00</td>
      <td>-3657384.44</td>
      <td>314572384.58</td>
      <td>-1971477243.41</td>
      <td>-73159279.50</td>
      <td>-42585869.50</td>
      <td>-11217966.87</td>
      <td>2913568690.79</td>
    </tr>
  </tbody>
</table>
</div>




```python
# построим  график, отражающий прибыльность фильмов с гос.поддержкой по годам

df_financed.groupby('show_year')['payback'].sum().plot(kind='bar', grid=True)
plt.title('Финансовый результат субсидируемых фильмов')
plt.xlabel('Годы')
plt.ylabel('Результат, млрд руб');
```


    
![png](output_151_0.png)
    


**Вывод**

Проведя предварительную оценку, из столбца **support_percentage** который мы рассчитывали ранее, можем заметить, что соотношение государственной поддержки к бюджету фильмов в среднем составляет 52%. Получается, что около половины бюджета картины финансируется государством. 

Как видно, в среднем на поддержку фильма выделалось 60,000,000 руб. При этом средняя окупаемость фильмов с государственной поддержкой имела отрицательное значение -139,747,188 руб, а 75% процентиль данных имел значение -70,968,828 руб. То есть в большинстве случаев, фильмы получившую государственную поддержку были убыточными. 

В подтверждение моему исследованию можем привести данные из общедоступных статей 2019 года: https://www.proekt.media/research/fond-kino/, https://www.rbc.ru/technology_and_media/14/12/2019/5df2610f9a79476d48fb1685 где также говорится о малом количестве окупившихся фильмов которые получили финансирование от государства.

#### Построим график показывающий количество фильмов получивших государственную поддержку по годам


```python
plt.style.use('ggplot')

df_financed.groupby('show_year')['total_support'].count().plot(x='year', style='o-', figsize=(15, 6), legend = True, color='midnightblue');

plt.title('Фильмы с гос. поддержкой', fontsize=14, fontweight="bold", color='black');
plt.xlabel('Год', fontweight="bold");
plt.ylabel('Количество фильмов', fontweight="bold");
```


    
![png](output_154_0.png)
    



```python
df_financed.groupby('show_year')['total_support'].sum()
```




    show_year
    2013    134347945.00
    2014    572002299.00
    2015   3656241459.00
    2016   4303155482.00
    2017   3183971662.00
    2018   3446969465.00
    2019   4904000000.00
    Name: total_support, dtype: float64



**Вывод:** 

Исходя из графика мы видим, что наибольшее количество фильмов получивших государственную поддержку пришлось на 2015 год. Далее по количеству господдержки следует 2019 год с рекордным финансированием фильмов в размере 4,9 млрд. руб.

#### Какие жанры фильмов оказались наиболее популярными при получении государственной поддержки?


```python
df_financed.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 332 entries, 1281 to 7478
    Data columns (total 15 columns):
     #   Column                 Non-Null Count  Dtype  
    ---  ------                 --------------  -----  
     0   title                  332 non-null    object 
     1   type                   332 non-null    object 
     2   age_restriction        332 non-null    object 
     3   refundable_support     332 non-null    float64
     4   nonrefundable_support  332 non-null    float64
     5   budget                 332 non-null    float64
     6   financing_source       332 non-null    object 
     7   ratings                314 non-null    float64
     8   box_office             318 non-null    float64
     9   support_percentage     315 non-null    float64
     10  show_year              332 non-null    int32  
     11  director_first         332 non-null    object 
     12  genres_first           332 non-null    object 
     13  total_support          332 non-null    float64
     14  payback                318 non-null    float64
    dtypes: float64(8), int32(1), object(6)
    memory usage: 40.2+ KB
    


```python
# используем удобный для визуалиции стиль и настроим параметры сетки, цвета и размера шрифта

plt.style.use('ggplot')

df_financed['genres_first'].value_counts().plot(
    kind='bar', figsize=(14,6), 
    grid=True, color='midnightblue', 
    edgecolor='black', linewidth=1
)
plt.xticks(rotation = 80, fontsize = 13)
plt.title('Количество фильмов с господдержкой по жанрам',fontsize=14, fontweight="bold", color="black")
plt.xlabel('Жанр фильма',fontweight="bold")
plt.ylabel('Количество фильмов', fontweight="bold")
plt.show()
```


    
![png](output_159_0.png)
    


**Вывод:** 

Можем заметить, что наиболее популярными жанрами среди фильмов получивших государственную поддержку в 2013-2019 годах являлись драмы, комедии и мультфильмы. А наименьшее количество поддержки от государства получали картины связанные с реальным телевидением и спортом.

### Посмотрим окупаемость фильмов в зависимости от жанров


```python
# создадим стобцы которые будут отражать прибыльность фильмов

df_financed['profitable'] = df_financed['payback'] > 0
df_financed['not_profitable'] = df_financed['payback'] < 0

# сгруппируем данные и построим столбчатую диаграмму в обе стороны

df_financed.groupby('genres_first') \
            .agg({'title': 'count',
                  'profitable': 'sum',
                  'not_profitable': lambda x: 0 - x.sum()}) \
            .sort_values(by='title',
                         ascending=False) \
            .plot(kind='bar', figsize=(14,6), 
                  grid=True, stacked=True, color=['midnightblue','orange'],
                  y=['profitable', 'not_profitable'])
plt.xticks(fontsize = 13)
plt.title('Окупаемость фильмов с господдержкой по жанрам',fontsize=14, fontweight="bold", color="black")
plt.xlabel('Жанр фильма',fontweight="bold")
plt.ylabel('Количество фильмов', fontweight="bold")
plt.show()
pass
```


    
![png](output_162_0.png)
    


**Вывод:** 

Исходя из построенной столбчатой диаграммы видим, что неприбыльных фильмов гораздо больше тех, что окупились (где кассовые сборы превышали общий бюджет в 2 раза). Это доказывает наше предположение о неокупаемости в п.3.1.2.


```python
df_financed.sample(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>type</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>box_office</th>
      <th>support_percentage</th>
      <th>show_year</th>
      <th>director_first</th>
      <th>genres_first</th>
      <th>total_support</th>
      <th>payback</th>
      <th>profitable</th>
      <th>not_profitable</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2542</th>
      <td>ОРЛЕАН</td>
      <td>Художественный</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>30000000.00</td>
      <td>92500000.00</td>
      <td>Фонд кино</td>
      <td>6.10</td>
      <td>18780020.90</td>
      <td>0.32</td>
      <td>2015</td>
      <td>А.Прошкин</td>
      <td>комедия</td>
      <td>30000000.00</td>
      <td>-73719979.10</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3462</th>
      <td>Защитники</td>
      <td>Художественный</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>50000000.00</td>
      <td>150000000.00</td>
      <td>323232109.00</td>
      <td>Фонд кино</td>
      <td>3.00</td>
      <td>262040254.00</td>
      <td>0.62</td>
      <td>2017</td>
      <td>С.Андреасян</td>
      <td>фантастика</td>
      <td>200000000.00</td>
      <td>-61191855.00</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>7137</th>
      <td>Трудности выживания</td>
      <td>Художественный</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>25000000.00</td>
      <td>35000000.00</td>
      <td>101659240.00</td>
      <td>Фонд кино</td>
      <td>5.00</td>
      <td>24101208.37</td>
      <td>0.59</td>
      <td>2019</td>
      <td>Е.Невский (псевдоним Е.Торрес)</td>
      <td>комедия</td>
      <td>60000000.00</td>
      <td>-77558031.63</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>3047</th>
      <td>Любовь с ограничениями</td>
      <td>Художественный</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>19000000.00</td>
      <td>51000000.00</td>
      <td>135295551.84</td>
      <td>Фонд кино</td>
      <td>6.30</td>
      <td>70299052.00</td>
      <td>NaN</td>
      <td>2016</td>
      <td>Д.Тюрин</td>
      <td>комедия</td>
      <td>70000000.00</td>
      <td>-64996499.84</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>6676</th>
      <td>Айка</td>
      <td>Художественный</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>28000000.00</td>
      <td>108518988.00</td>
      <td>Министерство культуры</td>
      <td>6.20</td>
      <td>2446886.00</td>
      <td>0.26</td>
      <td>2019</td>
      <td>С.Дворцевой</td>
      <td>мелодрама</td>
      <td>28000000.00</td>
      <td>-106072102.00</td>
      <td>False</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>



### Рейтинг фильмов и поиск зависимостей

Визуализируем рейтинг основных жанров фильмов и посмотрим какой жанр фильма лидиует по средней оценке рейтинга среди фильмов получивших государственную поддержку.


```python
# сгруппируем данные по основному жанру и посчитаем среднее значение рейтингов

df_financed[['genres_first', 'ratings']].groupby('genres_first') \
                                        .agg('mean') \
                                        .sort_values(by='ratings', ascending=False) \
                                        .plot(kind='bar', figsize=(14,6), 
    grid=True, color='midnightblue', 
    edgecolor='black', linewidth=1
)
plt.xticks(rotation = 80, fontsize = 13)
plt.title('Рейтинг фильмов с государственной поддержкой по жанрам',fontsize=14, fontweight="bold", color="black")
plt.xlabel('Жанр фильма',fontweight="bold")
plt.ylabel('Средний рейтинг', fontweight="bold")
plt.show()
```


    
![png](output_167_0.png)
    


**Вывод:** 

К фильмам с наиболее высоким рейтингом можно отнести криминальные и детские картины. А наименее популярными будут являться фильмы ужасов.

### Зависимость рейтинга от суммы государственной поддержки


```python
# посмотрим диаграмму рассеивания настроив визуализацию

fig = plt.figure(figsize=(12, 8))

sns.scatterplot(x=df_financed["ratings"], y=df_financed["total_support"], alpha=0.6, color='midnightblue')

plt.ticklabel_format(axis="y", style="plain")
plt.xticks(fontsize = 13)
plt.title('Зависимость рейтинга фильма от суммы поддержки',fontsize=14, fontweight="bold", color="black")
plt.xlabel('Рейтинг фильма',fontweight="bold")
plt.ylabel('Общая гос. поддержка, руб.', fontweight="bold")
plt.show()
```


    
![png](output_170_0.png)
    



```python
print('Корреляция рейтинга фильма от суммы поддежки составляет', df_financed["ratings"].corr(df_financed["total_support"]))
```

    Корреляция рейтинга фильма от суммы поддежки составляет 0.11828746275619725
    

**Вывод:** 

Из диаграммы рассеивания видим, что в нашей выборке преобладают картины с объемом государственной поддержки до 100 млн рублей. Фильмы с общей суммой поддержки более 200 млн рублей как правило не имели оценок ниже 5 баллов. Фильмы которые получали размер государственной поддержки более 300 миллионов рублей не имеют тенденции в повышении рейтингов. 

Какое-либо конкретное влияние суммы гос. поддержки на рейтинг фильма обнаружить не удалось. Из нашей диаграммы рассеивания можем найти подтерждение п.3.1.7 (таблица корреляции), что от увеличения государственной поддержки фильма его рейтинг далеко не всегда линейно увеличивается.


```python
# посмотрим диаграмму рассеивания настроив визуализацию

fig = plt.figure(figsize=(12, 8))

sns.scatterplot(x=df_financed["ratings"], y=df_financed["payback"], alpha=0.6, color='midnightblue')
plt.ylim(-1000000000, 1000000000);

plt.ticklabel_format(axis="y", style="plain")
plt.xticks(fontsize = 13)
plt.title('Зависимость окупаемости от рейтинга фильма',fontsize=14, fontweight="bold", color="black")
plt.xlabel('Рейтинг фильма',fontweight="bold")
plt.ylabel('Окупаемость в руб.', fontweight="bold")
plt.show()
```


    
![png](output_173_0.png)
    



```python
print('Корреляция окупаемости от рейтинга фильма состаялет', df_financed["ratings"].corr(df_financed["payback"]))
```

    Корреляция окупаемости от рейтинга фильма состаялет 0.09888368077532816
    


```python
# скопируем изначальный датафрейм со срезом по всем Русским фильмам (по нему мы будем вычислять тренды)

rus_cinema = df.query('production_country == "Россия"')
```


```python
# возьмём срез данных, в котором non-null значения столбца nonrefundable_support или refundable_support 
#(по нему мы будем исследовать фильмы с гос. поддержкой)
gover_sup = df.loc[(df['nonrefundable_support'].isna() == False) | (df['refundable_support'].isna() == False)].reset_index(drop=True)
rus_cinema.info()
print('-------------------------------------------')
gover_sup.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 1823 entries, 336 to 7479
    Data columns (total 20 columns):
     #   Column                 Non-Null Count  Dtype              
    ---  ------                 --------------  -----              
     0   title                  1823 non-null   object             
     1   punumber               1822 non-null   float64            
     2   show_start_date        1823 non-null   datetime64[ns, UTC]
     3   type                   1823 non-null   object             
     4   film_studio            1806 non-null   object             
     5   production_country     1823 non-null   object             
     6   director               1823 non-null   object             
     7   producer               1785 non-null   object             
     8   age_restriction        1823 non-null   object             
     9   refundable_support     316 non-null    float64            
     10  nonrefundable_support  316 non-null    float64            
     11  budget                 316 non-null    float64            
     12  financing_source       316 non-null    object             
     13  ratings                1281 non-null   float64            
     14  genres                 1823 non-null   object             
     15  box_office             779 non-null    float64            
     16  support_percentage     299 non-null    float64            
     17  show_year              1823 non-null   int32              
     18  director_first         1823 non-null   object             
     19  genres_first           1823 non-null   object             
    dtypes: datetime64[ns, UTC](1), float64(7), int32(1), object(11)
    memory usage: 292.0+ KB
    -------------------------------------------
    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 332 entries, 0 to 331
    Data columns (total 20 columns):
     #   Column                 Non-Null Count  Dtype              
    ---  ------                 --------------  -----              
     0   title                  332 non-null    object             
     1   punumber               332 non-null    float64            
     2   show_start_date        332 non-null    datetime64[ns, UTC]
     3   type                   332 non-null    object             
     4   film_studio            332 non-null    object             
     5   production_country     332 non-null    object             
     6   director               332 non-null    object             
     7   producer               330 non-null    object             
     8   age_restriction        332 non-null    object             
     9   refundable_support     332 non-null    float64            
     10  nonrefundable_support  332 non-null    float64            
     11  budget                 332 non-null    float64            
     12  financing_source       332 non-null    object             
     13  ratings                314 non-null    float64            
     14  genres                 332 non-null    object             
     15  box_office             318 non-null    float64            
     16  support_percentage     315 non-null    float64            
     17  show_year              332 non-null    int32              
     18  director_first         332 non-null    object             
     19  genres_first           332 non-null    object             
    dtypes: datetime64[ns, UTC](1), float64(7), int32(1), object(11)
    memory usage: 50.7+ KB
    


```python
# создадим столбец, который наглядно будет показывать число box_office и сумму за этот период

support_statistic = gover_sup.groupby('show_year')['box_office'].agg(['count', 'sum']).reset_index()
support_statistic
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>show_year</th>
      <th>count</th>
      <th>sum</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2013</td>
      <td>2</td>
      <td>20322385.10</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2014</td>
      <td>16</td>
      <td>1017422166.60</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2015</td>
      <td>85</td>
      <td>5785285418.14</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2016</td>
      <td>60</td>
      <td>6081707839.10</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2017</td>
      <td>39</td>
      <td>10865075300.96</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2018</td>
      <td>56</td>
      <td>9934069010.25</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2019</td>
      <td>60</td>
      <td>8409627454.63</td>
    </tr>
  </tbody>
</table>
</div>




```python
sns.barplot(x = 'show_year', y = 'count', data = support_statistic)
plt.title('Кол-во фильмов с государственной поддержкой')
plt.show()
sns.barplot(x = 'show_year', y = 'sum', data = support_statistic)
plt.title('Сумма сборов у фильмов с государственной поддержкой')
plt.show()
```


    
![png](output_178_0.png)
    



    
![png](output_178_1.png)
    


**Вывод**

При исследовании кол-ва фильмов с государственной поддержкой - внимание сразу привлекает 2015 год, с количесвенным пиком равным 85. Такое ощущение, что быстрое возрастание графика с 2014 до 2015 прямо кричит нам о том, что ранее был кризис в киноотросли и вот в 2014-2015 годах началась "Новая эра" российского кино. Однако, видимо этот год не дал особо хороших результатов, поэтому финансирование сократили, однако, начиная с 2017 года, график имеет положительное стремление, что не может не радовать.

Сумма сборов у фильмов с государственной поддержкой - внимательно просмотрев первый график мы можем увидеть, насколько второй зависит от него. К примеру, мы правильно определили, что в 2015 году, несмотря на самое большое кол-во поддержки, сумма сборов не дошла даже до 6 млрд., но при этом в 2017 году сумма сборов имела свой максимум в 10 млрд., несмотря на то, что кол-во поддержки было равным 39. Поэтому мы и видим положительное стремление первого графика после 2017 года, однако отрицательное стремление второго. Не известно что могло произойти, может у Бондарчука был отпуск, кто знает...


```python
# пришло время составить список режисёров
# создадим столбец с разность выручки и государственной поддержки
gover_sup['revenue_gover'] = gover_sup['box_office'] - (gover_sup['refundable_support'] + gover_sup['nonrefundable_support'])

# создадим столбец с разность выручки и бюджета
gover_sup['revenue'] = gover_sup['box_office'] - gover_sup['budget']

# создадим столбец суммарной государственной поддержки
gover_sup['total_support'] = gover_sup['refundable_support'] + gover_sup['nonrefundable_support']
gover_sup
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>punumber</th>
      <th>show_start_date</th>
      <th>type</th>
      <th>film_studio</th>
      <th>production_country</th>
      <th>director</th>
      <th>producer</th>
      <th>age_restriction</th>
      <th>refundable_support</th>
      <th>nonrefundable_support</th>
      <th>budget</th>
      <th>financing_source</th>
      <th>ratings</th>
      <th>genres</th>
      <th>box_office</th>
      <th>support_percentage</th>
      <th>show_year</th>
      <th>director_first</th>
      <th>genres_first</th>
      <th>revenue_gover</th>
      <th>revenue</th>
      <th>total_support</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Пока еще жива</td>
      <td>111005313.00</td>
      <td>2013-10-11 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>АНО содействия развитию кинематографии "Ангел-...</td>
      <td>Россия</td>
      <td>А.Атанесян</td>
      <td>А.Атанесян, М.Бабаханов, Р.Бутко</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>26500000.00</td>
      <td>79411900.00</td>
      <td>Министерство культуры</td>
      <td>8.10</td>
      <td>драма,мелодрама</td>
      <td>365353.60</td>
      <td>0.33</td>
      <td>2013</td>
      <td>А.Атанесян</td>
      <td>драма</td>
      <td>-26134646.40</td>
      <td>-79046546.40</td>
      <td>26500000.00</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Бесславные придурки</td>
      <td>111003314.00</td>
      <td>2014-03-28 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Компания "АТК-Студио"</td>
      <td>Россия</td>
      <td>А.Якимчук</td>
      <td>А.Тютрюмов</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>26000000.00</td>
      <td>37142857.00</td>
      <td>Министерство культуры</td>
      <td>NaN</td>
      <td>unknown</td>
      <td>28140.00</td>
      <td>0.70</td>
      <td>2014</td>
      <td>А.Якимчук</td>
      <td>unknown</td>
      <td>-25971860.00</td>
      <td>-37114717.00</td>
      <td>26000000.00</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Невидимки</td>
      <td>111004213.00</td>
      <td>2013-09-10 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Компания "РЕАЛ-ДАКОТА"</td>
      <td>Россия</td>
      <td>Р.Давлетьяров, С.Комаров</td>
      <td>Р.Давлетьяров, А.Котелевский, А.Олейников</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>107847945.00</td>
      <td>176023490.00</td>
      <td>Фонд кино</td>
      <td>5.30</td>
      <td>комедия,фантастика</td>
      <td>19957031.50</td>
      <td>0.61</td>
      <td>2013</td>
      <td>Р.Давлетьяров</td>
      <td>комедия</td>
      <td>-87890913.50</td>
      <td>-156066458.50</td>
      <td>107847945.00</td>
    </tr>
    <tr>
      <th>3</th>
      <td>БЕРЦЫ</td>
      <td>111004314.00</td>
      <td>2014-05-05 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Студия "Пассажир"</td>
      <td>Россия</td>
      <td>Е.Миндадзе (псевдоним Катя Шагалова)</td>
      <td>Л.Антонова</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>28000000.00</td>
      <td>40574140.00</td>
      <td>Министерство культуры</td>
      <td>4.20</td>
      <td>драма</td>
      <td>55917.50</td>
      <td>0.69</td>
      <td>2014</td>
      <td>Е.Миндадзе (псевдоним Катя Шагалова)</td>
      <td>драма</td>
      <td>-27944082.50</td>
      <td>-40518222.50</td>
      <td>28000000.00</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Братья Ч</td>
      <td>111004414.00</td>
      <td>2014-04-23 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Студия "Пассажир"</td>
      <td>Россия</td>
      <td>М.Угаров</td>
      <td>А.Миндадзе, Л.Антонова</td>
      <td>«16+» - для детей старше 16 лет</td>
      <td>0.00</td>
      <td>25000000.00</td>
      <td>40015122.00</td>
      <td>Министерство культуры</td>
      <td>6.40</td>
      <td>драма</td>
      <td>232100.00</td>
      <td>0.62</td>
      <td>2014</td>
      <td>М.Угаров</td>
      <td>драма</td>
      <td>-24767900.00</td>
      <td>-39783022.00</td>
      <td>25000000.00</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>327</th>
      <td>Союз спасения</td>
      <td>111022019.00</td>
      <td>2019-12-26 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ЗАО "Дирекция кино"</td>
      <td>Россия</td>
      <td>А.Кравчук</td>
      <td>А.Максимов, К.Эрнст</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>100000000.00</td>
      <td>400000000.00</td>
      <td>980000000.00</td>
      <td>Фонд кино</td>
      <td>6.00</td>
      <td>история,биография,драма</td>
      <td>717703185.53</td>
      <td>0.51</td>
      <td>2019</td>
      <td>А.Кравчук</td>
      <td>история</td>
      <td>217703185.53</td>
      <td>-262296814.47</td>
      <td>500000000.00</td>
    </tr>
    <tr>
      <th>328</th>
      <td>Иван Царевич и Серый Волк 4</td>
      <td>114005019.00</td>
      <td>2019-12-20 12:00:00+00:00</td>
      <td>Анимационный</td>
      <td>ООО "Студия анимационного кино "Мельница"</td>
      <td>Россия</td>
      <td>Д.Шмидт, К.Феоктистов</td>
      <td>С.Сельянов, А.Боярский</td>
      <td>«6+» - для детей старше 6 лет</td>
      <td>100000000.00</td>
      <td>0.00</td>
      <td>190000000.00</td>
      <td>Фонд кино</td>
      <td>6.70</td>
      <td>мультфильм,приключения,семейный</td>
      <td>501069235.00</td>
      <td>0.53</td>
      <td>2019</td>
      <td>Д.Шмидт</td>
      <td>мультфильм</td>
      <td>401069235.00</td>
      <td>311069235.00</td>
      <td>100000000.00</td>
    </tr>
    <tr>
      <th>329</th>
      <td>Вторжение</td>
      <td>111022519.00</td>
      <td>2019-12-23 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Арт Пикчерс Студия", ООО "Водород 2011"</td>
      <td>Россия</td>
      <td>Ф.Бондарчук</td>
      <td>Ф.Бондарчук, М.Врубель, А.Андрющенко, Д.Рудовский</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>100000000.00</td>
      <td>400000000.00</td>
      <td>944000000.00</td>
      <td>Фонд кино</td>
      <td>5.70</td>
      <td>фантастика,боевик</td>
      <td>NaN</td>
      <td>0.53</td>
      <td>2019</td>
      <td>Ф.Бондарчук</td>
      <td>фантастика</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>500000000.00</td>
    </tr>
    <tr>
      <th>330</th>
      <td>Я свободен</td>
      <td>111023019.00</td>
      <td>2019-12-26 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>АО "ТПО "Киностудия им. М.Горького"</td>
      <td>Россия</td>
      <td>И.Северов</td>
      <td>С.Зернов</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>0.00</td>
      <td>30000000.00</td>
      <td>46154000.00</td>
      <td>Министерство культуры</td>
      <td>5.90</td>
      <td>драма</td>
      <td>NaN</td>
      <td>0.65</td>
      <td>2019</td>
      <td>И.Северов</td>
      <td>драма</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>30000000.00</td>
    </tr>
    <tr>
      <th>331</th>
      <td>(Не)идеальный мужчина</td>
      <td>111023119.00</td>
      <td>2019-12-24 12:00:00+00:00</td>
      <td>Художественный</td>
      <td>ООО "Нон-Стоп Продакшн"</td>
      <td>Россия</td>
      <td>М.Бальчюнас (псевдоним М.Вайсберг)</td>
      <td>С.Мелькумов, А.Роднянский, М.Вайсберг, Р.Минас...</td>
      <td>«12+» - для детей старше 12 лет</td>
      <td>40000000.00</td>
      <td>60000000.00</td>
      <td>150147502.00</td>
      <td>Фонд кино</td>
      <td>4.50</td>
      <td>комедия,фантастика,мелодрама</td>
      <td>NaN</td>
      <td>0.67</td>
      <td>2019</td>
      <td>М.Бальчюнас (псевдоним М.Вайсберг)</td>
      <td>комедия</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>100000000.00</td>
    </tr>
  </tbody>
</table>
<p>332 rows × 23 columns</p>
</div>




```python
# разберёмся с режисёрами

table = gover_sup.pivot_table(index='director_first', values=['total_support', 'revenue','revenue_gover', 'ratings'])
print('Toп режиссёров по государственной помощи')
display(table.sort_values(by='total_support', ascending=False).head(3))
print('Toп режиссёров по прибыли с фильма')
display(table.sort_values(by='revenue', ascending=False).head(5))
print('Toп режиссёров по рейтингам фильма')
display(table.sort_values(by='ratings', ascending=False).head(3))
```

    Toп режиссёров по государственной помощи
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ratings</th>
      <th>revenue</th>
      <th>revenue_gover</th>
      <th>total_support</th>
    </tr>
    <tr>
      <th>director_first</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Ф.Бондарчук</th>
      <td>5.70</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>500000000.00</td>
    </tr>
    <tr>
      <th>А.Кравчук</th>
      <td>6.00</td>
      <td>-262296814.47</td>
      <td>217703185.53</td>
      <td>500000000.00</td>
    </tr>
    <tr>
      <th>А.Мизгирев</th>
      <td>6.60</td>
      <td>-319915396.40</td>
      <td>-85714860.40</td>
      <td>450000000.00</td>
    </tr>
  </tbody>
</table>
</div>


    Toп режиссёров по прибыли с фильма
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ratings</th>
      <th>revenue</th>
      <th>revenue_gover</th>
      <th>total_support</th>
    </tr>
    <tr>
      <th>director_first</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>А.Мегердичев</th>
      <td>7.50</td>
      <td>2189493953.00</td>
      <td>2379686144.00</td>
      <td>400000000.00</td>
    </tr>
    <tr>
      <th>А.Сидоров</th>
      <td>6.50</td>
      <td>1707969287.52</td>
      <td>2091754004.52</td>
      <td>180000000.00</td>
    </tr>
    <tr>
      <th>О.Трофим</th>
      <td>NaN</td>
      <td>1297146575.89</td>
      <td>1360731797.89</td>
      <td>85000000.00</td>
    </tr>
    <tr>
      <th>К.Шипенко</th>
      <td>6.83</td>
      <td>1040947183.26</td>
      <td>1171924072.60</td>
      <td>104000000.00</td>
    </tr>
    <tr>
      <th>Н.Лебедев</th>
      <td>7.60</td>
      <td>766971523.00</td>
      <td>960150908.00</td>
      <td>442104482.00</td>
    </tr>
  </tbody>
</table>
</div>


    Toп режиссёров по рейтингам фильма
    


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ratings</th>
      <th>revenue</th>
      <th>revenue_gover</th>
      <th>total_support</th>
    </tr>
    <tr>
      <th>director_first</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>А.Атанесян</th>
      <td>8.10</td>
      <td>-79046546.40</td>
      <td>-26134646.40</td>
      <td>26500000.00</td>
    </tr>
    <tr>
      <th>А.Попова</th>
      <td>8.00</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3000000.00</td>
    </tr>
    <tr>
      <th>К.Оганисян</th>
      <td>7.90</td>
      <td>-77128657.96</td>
      <td>52871342.04</td>
      <td>120000000.00</td>
    </tr>
  </tbody>
</table>
</div>


**Вывод по режиссёрам:**

Тройка лидеров по "займам" - Ф. Бондарчук, который суммарно занял 500.000.000 рублей, столько же занял и А. Кравчук, А. Мизгирев - 450.000.000. Однако средний рейтинг равен 6, к сожалению сборы Бандарчука мы не знаем, но у двух оставшихся отрицательных доход с фильма. Что может говорить о том, что их картины, к сожалению, не оправдали своих ожиданий.

Тройка лидеров по прибыли - А. Мегердичев, А. Сидоров, О. Трофим.

Пятёрка лидеров по рейтингу - А. Атанесян, А. Попова, К. Оганисян, А. Андрианов, В. Татарский. Хотелось бы отметить, что лишь один человек из всех 5 вышеперечисленных смог "выйти в плюс" с показов своего фильма. Скорее всего остальные сделали всё супер: качественная картинка, сценарий, спецэффекты, для хорошей оценки от пользователь этого было достаточно, однако проект получился слишком затратным и они ушли в минус.

## Общий вывод

В ходе проделанной работы были обнаружены следующие ошибки: 
- тип данных в столбце puNumber в csv файле **mkrf_shows** изначально был str (object pandas), изменил тип на int64 и смог обьединить две таблицы в одну;
- в столбце **ratings** некоторые данные были не в float64, а в процентах, сообразить что это увы не смог, пришлось заменить все подобные некорректные данные на NaN;
- некоторые значения столбца **budget** были некорректны, тк спонсированный бюджет был больше самого бюжета, пришлось создавать функцию, которая сделает новую колонку корректного бюджета; 
- в ходе изучения категориальных значений я смог заметить, что в столбце **type** есть ненужные пробелы, они были удалены;
- в столбце **production_country** обнаружил, что есть некоторые одинаковые сочетания стран, однако они были написаны по-разному, к примеру 'Германия - Франция' и 'Германия-Франция' - все поднобные ошибки были исправлены(удалил пробелы между '-').

Также было большое кол-во пропуков в данных, к примеру столбец **ratings**, они могли возникнуть по технической причине, либо подобных данных не было на сервесе, откуда мы их брали, в нашем случае с Кинопоиска. Также были обнаружены значительные пропуски, которые нам были необходимы при анализе в столбце genres, по-моему мнению всё по тем же причинам. Можно было подвизать это всё через API по сервесу ivi, но насколько мне известно, разные сервисы дают разные данные, это было бы некорректно, поэтому оставил всё как есть и анализировал на корректных данных.

Для удобства исследования были добавлены новые столбцы: 
- информация о годе проката;
- главный жанр фильма;
- главный режисёр фильма;
- доля от общего бюджета фильма, которая составляет государственная поддержка;
- столбец с разность выручки и государственной поддержки;
- столбец с разность выручки и общего бюджета и столбец суммарной государственной поддержки.

Это позволило мне сделать более детальную и гибкую аналитику, рассмотреть дополнительные графики, таблицы и сделать по ним определённые выводы. Говоря об аналитике, хочется подчеркнуть, что с каждым годом сумма сборов возрастает (положительная корреляция, в районе 0.9), при этом минимальный сумма сборов была зафиксирована в 2016 году, а максимальная в 2017. Если говорить о возрастном ограничении, можно с уверенностью сказать, что фильмы 18+ имеют положительную корреляцию сквозь года, лидирующие позиции по сборам занимают кинокартины 16+, при этом в плотной борьюе находятся фильмы 12+ и 6+, а 0+ практически ничего не собирают.

Однако моей задачей было не просто рассмотреть общие графики, а выявить текущие тренды российского кинематографа, а также углубиться в фильмы, которые имеют государственную поддержку, но обо всём по порядку. Самым худшим годом для поддержки российского кинематографа из всех представленных (2013-2019) стал 2015, в котором было максимальное кол-во поддержки, однако маленькая сумма сборов, после этого года гос. поддержка сократилась вдвое. Его антиподом стал 2017 год, самое интересное, что именно в этот год зафиксировано минимальное кол-во государственной поддержки. Удачно спрогнозированные по заработку фильмы. После этого события кол-во гос. поддержки потихоньку ползёт вверх, однако сумма сборов опять покатилась вниз. В среднем государственная поддержка занимает от 55 до 60%, однако "окупиться" картина может с вероятностью всего в 24% (правда это не мешает суммарно окупать свои вложения). Однако публика оценивает подобные картины, к сожалению, лишь иногда чуть выше 7 быллов, что по меркам кинопоиска "3+".

**ФИЛЬМЫ С ГОСУДАРСТВЕННОЙ ПОДДЕРЖКОЙ**

Количество фильмов, снятых с участием государства составляет около 5% от всех фильмов, выпущенных в прокат за весь рассматриваемый период. Количество фильмов, вышедших в прокат за период с 2010-2019, снятых с гос. поддержкой, составляет 332. Всего за период с 2013-2019 была оказана гос. поддержка на сумму 20,2 млрд руб. Медианное значение гос. поддержки одного фильма за весь период с 2013-2019 составляет 35 млн руб. Минимальное значение гос. поддержки составило 3 млн руб. Общая сумма кассовых сборов за весь рассматриваемый период по фильмам, снятым с гос. поддержкой, составляет 42 млрд руб, что всего на 1,5 млрд превышает бюджет данных фильмов. Однако за весь рассматриваемый период лишь в 2017 и в 2018 годах фильмы с гос. поддержкой себя окупили. В остальные годы фильмы с гос. поддержкой себя не окупали. Я выяснил, что фильмы, снятые без участия государства, пользуются большей любовью у зрителей, чем фильмы, снятые с гом. поддержкой.

Самая распространенная возрастная категория как среди фильмов с гос. поддержкой так и без неё – это категория 16+.

Фильмы, снятые с гос.поддержкой не отличаются разнообразием жанров: 90% всех фильмов с гос.поддержкой представляют собой художественные фильмы, а оставшиеся 10% фильмов это мультфильмы. Однако, жанры фильмов, снятых без участия государства очень разнообразны. Несмотря на то, что художественные фильмы и мультфильмы также наиболее распространены, было снято много документальных, научно-популярных и прочих фильмов.

**Давайте поговорим о трендах:** 

в качестве основы я взял два, по-моему мнению, важных фактора - сумму сборов и рейтинги. Первый будет рассказывать нам о востребованности (желании посмотреть) тот или иной жанр, а второй покажет как хорошо снимают фильмы, нравятся ли они людям. 
Кратко говоря: 
- деньги - востребованность, 
- рейтинги - конечные эмоции. 

Говоря о сочетании этих двух факторов - всё неоднозначно, обычно у фильмов с хорошими сборами не собо хорошие рейтинги. Чаще всего снимают фильмы в жанре комедии и драмы, однако это не приносит свои плоды. Скорее всего русская публика перенасытилась от данных жанров, сколько там частей ёлок вышло? Именно поэтому они не попадают в топ по сумме сборов (желанию зрителя посмотреть). 

Верхушку рейтинга по желанию к просмотру занимают следующие жанры: военный, мультфильм, также в текущие тренды добавился новый жанр, который полюбила публика - история, семейный, а самым последними идут ужасы. Но, вот что интересно, если помотреть на лидеров жанра по рейтингам зрителей: семейный,  докуменальный, стал популизироваться новый жанр киноиндустрии - аниме (с каждым годом он набирает обороты), триллер, а также криминал, то у этих двух списков нет пересечений. Соответственно из этого можно сделать один простой вывод: зритель редко получает востребованные эмоции от желанного жанра.

**Подводя итог,**

хотелось бы выдвинуть некий список трендов: чаще всего это фильмы с категорией 6+ или 16+, сюда попадает и детская и взрослая аудитория, если говорить про жанры: военный, мультфильм, история, семейный, ужасы. Однако Российский кинематограф хорошо снимает совсем другое кино... Следует обратить внимание именно на вышеперечисленные жанры, уменьшить затраты на такие направления, как комедия и драма, т. к. русский зритель перенасыщен ими двумя.


```python

```
