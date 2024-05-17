<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Открываем-файл-с-данными-и-изучаем-общую-информацию" data-toc-modified-id="Открываем-файл-с-данными-и-изучаем-общую-информацию-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Открываем файл с данными и изучаем общую информацию</a></span><ul class="toc-item"><li><span><a href="#Импортируем-библиотеки-для-работы-с-файлами" data-toc-modified-id="Импортируем-библиотеки-для-работы-с-файлами-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Импортируем библиотеки для работы с файлами</a></span></li><li><span><a href="#Загружаем-данные-из-csv-файла-в-датафрейм-c-помощью-библиотеки-pandas." data-toc-modified-id="Загружаем-данные-из-csv-файла-в-датафрейм-c-помощью-библиотеки-pandas.-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>Загружаем данные из csv-файла в датафрейм c помощью библиотеки pandas.</a></span></li><li><span><a href="#Первичный-взгляд-на-полученные-данные" data-toc-modified-id="Первичный-взгляд-на-полученные-данные-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Первичный взгляд на полученные данные</a></span></li><li><span><a href="#Выведем-статистику-по-исходным-данным" data-toc-modified-id="Выведем-статистику-по-исходным-данным-1.4"><span class="toc-item-num">1.4&nbsp;&nbsp;</span>Выведем статистику по исходным данным</a></span></li><li><span><a href="#Проверим-таблицу-на-наличие-явных-дубликатов." data-toc-modified-id="Проверим-таблицу-на-наличие-явных-дубликатов.-1.5"><span class="toc-item-num">1.5&nbsp;&nbsp;</span>Проверим таблицу на наличие явных дубликатов.</a></span></li><li><span><a href="#Проверим-количество-пропусков" data-toc-modified-id="Проверим-количество-пропусков-1.6"><span class="toc-item-num">1.6&nbsp;&nbsp;</span>Проверим количество пропусков</a></span></li><li><span><a href="#Построим-гистограмму-для-всех-числовых-столбцов-таблицы-на-одном-графике" data-toc-modified-id="Построим-гистограмму-для-всех-числовых-столбцов-таблицы-на-одном-графике-1.7"><span class="toc-item-num">1.7&nbsp;&nbsp;</span>Построим гистограмму для всех числовых столбцов таблицы на одном графике</a></span></li></ul></li><li><span><a href="#Предобработка-данных" data-toc-modified-id="Предобработка-данных-2"><span class="toc-item-num">2&nbsp;&nbsp;</span>Предобработка данных</a></span><ul class="toc-item"><li><span><a href="#Приведем-имена-столбцов-к-единому-стилю" data-toc-modified-id="Приведем-имена-столбцов-к-единому-стилю-2.1"><span class="toc-item-num">2.1&nbsp;&nbsp;</span>Приведем имена столбцов к единому стилю</a></span></li><li><span><a href="#Обрабатаем-пропуски-в-данных" data-toc-modified-id="Обрабатаем-пропуски-в-данных-2.2"><span class="toc-item-num">2.2&nbsp;&nbsp;</span>Обрабатаем пропуски в данных</a></span></li><li><span><a href="#Преобразуем-типы-данных" data-toc-modified-id="Преобразуем-типы-данных-2.3"><span class="toc-item-num">2.3&nbsp;&nbsp;</span>Преобразуем типы данных</a></span></li><li><span><a href="#Обрабатываем-дубликаты" data-toc-modified-id="Обрабатываем-дубликаты-2.4"><span class="toc-item-num">2.4&nbsp;&nbsp;</span>Обрабатываем дубликаты</a></span><ul class="toc-item"><li><span><a href="#Явные-дубликаты" data-toc-modified-id="Явные-дубликаты-2.4.1"><span class="toc-item-num">2.4.1&nbsp;&nbsp;</span>Явные дубликаты</a></span></li><li><span><a href="#Неявные-дубликаты" data-toc-modified-id="Неявные-дубликаты-2.4.2"><span class="toc-item-num">2.4.2&nbsp;&nbsp;</span>Неявные дубликаты</a></span></li><li><span><a href="#Далее-посморим-на-столбец-с-высотой-потолков-ceiling_height:-минимальная-высота-потолков-1-метр,-максимальная---100-метров." data-toc-modified-id="Далее-посморим-на-столбец-с-высотой-потолков-ceiling_height:-минимальная-высота-потолков-1-метр,-максимальная---100-метров.-2.4.3"><span class="toc-item-num">2.4.3&nbsp;&nbsp;</span>Далее посморим на столбец с высотой потолков ceiling_height: минимальная высота потолков 1 метр, максимальная - 100 метров.</a></span></li></ul></li></ul></li><li><span><a href="#Расчёты-и-добавление-результатов-в-таблицу" data-toc-modified-id="Расчёты-и-добавление-результатов-в-таблицу-3"><span class="toc-item-num">3&nbsp;&nbsp;</span>Расчёты и добавление результатов в таблицу</a></span><ul class="toc-item"><li><span><a href="#Произведем-расчет-данных-и-добавим-их-в-таблицу-для-дальнейшего-исследования:" data-toc-modified-id="Произведем-расчет-данных-и-добавим-их-в-таблицу-для-дальнейшего-исследования:-3.1"><span class="toc-item-num">3.1&nbsp;&nbsp;</span>Произведем расчет данных и добавим их в таблицу для дальнейшего исследования:</a></span><ul class="toc-item"><li><span><a href="#Добавим-столбец-price_one_square_meter" data-toc-modified-id="Добавим-столбец-price_one_square_meter-3.1.1"><span class="toc-item-num">3.1.1&nbsp;&nbsp;</span>Добавим столбец price_one_square_meter</a></span></li><li><span><a href="#Добавим-столбец-exposition_weekday,-exposition_month,-exposition_year" data-toc-modified-id="Добавим-столбец-exposition_weekday,-exposition_month,-exposition_year-3.1.2"><span class="toc-item-num">3.1.2&nbsp;&nbsp;</span>Добавим столбец exposition_weekday, exposition_month, exposition_year</a></span></li><li><span><a href="#Добавим-столбец-с-категоризацией-по-этажам-floor_category" data-toc-modified-id="Добавим-столбец-с-категоризацией-по-этажам-floor_category-3.1.3"><span class="toc-item-num">3.1.3&nbsp;&nbsp;</span>Добавим столбец с категоризацией по этажам floor_category</a></span></li><li><span><a href="#Добавим-столбец-city_centers_nearest_km" data-toc-modified-id="Добавим-столбец-city_centers_nearest_km-3.1.4"><span class="toc-item-num">3.1.4&nbsp;&nbsp;</span>Добавим столбец city_centers_nearest_km</a></span></li></ul></li></ul></li><li><span><a href="#Проведение-исследовательского-анализа-данных:" data-toc-modified-id="Проведение-исследовательского-анализа-данных:-4"><span class="toc-item-num">4&nbsp;&nbsp;</span>Проведение исследовательского анализа данных:</a></span><ul class="toc-item"><li><span><a href="#Общая-площадь" data-toc-modified-id="Общая-площадь-4.1"><span class="toc-item-num">4.1&nbsp;&nbsp;</span>Общая площадь</a></span></li><li><span><a href="#Жилая-площадь" data-toc-modified-id="Жилая-площадь-4.2"><span class="toc-item-num">4.2&nbsp;&nbsp;</span>Жилая площадь</a></span></li><li><span><a href="#Площадь-кухни" data-toc-modified-id="Площадь-кухни-4.3"><span class="toc-item-num">4.3&nbsp;&nbsp;</span>Площадь кухни</a></span></li><li><span><a href="#Цена-объекта" data-toc-modified-id="Цена-объекта-4.4"><span class="toc-item-num">4.4&nbsp;&nbsp;</span>Цена объекта</a></span></li><li><span><a href="#Количество-комнат" data-toc-modified-id="Количество-комнат-4.5"><span class="toc-item-num">4.5&nbsp;&nbsp;</span>Количество комнат</a></span></li><li><span><a href="#Высота-потолков" data-toc-modified-id="Высота-потолков-4.6"><span class="toc-item-num">4.6&nbsp;&nbsp;</span>Высота потолков</a></span></li><li><span><a href="#Этаж-квартиры" data-toc-modified-id="Этаж-квартиры-4.7"><span class="toc-item-num">4.7&nbsp;&nbsp;</span>Этаж квартиры</a></span></li><li><span><a href="#Тип-этажа-квартиры-(«первый»,-«последний»,-«другой»)" data-toc-modified-id="Тип-этажа-квартиры-(«первый»,-«последний»,-«другой»)-4.8"><span class="toc-item-num">4.8&nbsp;&nbsp;</span>Тип этажа квартиры («первый», «последний», «другой»)</a></span></li><li><span><a href="#Общее-количество-этажей-в-доме" data-toc-modified-id="Общее-количество-этажей-в-доме-4.9"><span class="toc-item-num">4.9&nbsp;&nbsp;</span>Общее количество этажей в доме</a></span></li><li><span><a href="#Расстояние-до-центра-города-в-метрах" data-toc-modified-id="Расстояние-до-центра-города-в-метрах-4.10"><span class="toc-item-num">4.10&nbsp;&nbsp;</span>Расстояние до центра города в метрах</a></span></li><li><span><a href="#Расстояние-до-ближайшего-аэропорта" data-toc-modified-id="Расстояние-до-ближайшего-аэропорта-4.11"><span class="toc-item-num">4.11&nbsp;&nbsp;</span>Расстояние до ближайшего аэропорта</a></span></li><li><span><a href="#Расстояние-до-ближайшего-парка-в-метрах" data-toc-modified-id="Расстояние-до-ближайшего-парка-в-метрах-4.12"><span class="toc-item-num">4.12&nbsp;&nbsp;</span>Расстояние до ближайшего парка в метрах</a></span></li><li><span><a href="#День-и-месяц-публикации-объявления" data-toc-modified-id="День-и-месяц-публикации-объявления-4.13"><span class="toc-item-num">4.13&nbsp;&nbsp;</span>День и месяц публикации объявления</a></span></li><li><span><a href="#Месяц-публикации-объявления" data-toc-modified-id="Месяц-публикации-объявления-4.14"><span class="toc-item-num">4.14&nbsp;&nbsp;</span>Месяц публикации объявления</a></span></li><li><span><a href="#Изучим,-как-быстро-продавались-квартиры-(столбец-days_exposition)" data-toc-modified-id="Изучим,-как-быстро-продавались-квартиры-(столбец-days_exposition)-4.15"><span class="toc-item-num">4.15&nbsp;&nbsp;</span>Изучим, как быстро продавались квартиры (столбец days_exposition)</a></span></li><li><span><a href="#Проанализируем-факторы-влияющие-на-общую-стоимость-объекта" data-toc-modified-id="Проанализируем-факторы-влияющие-на-общую-стоимость-объекта-4.16"><span class="toc-item-num">4.16&nbsp;&nbsp;</span>Проанализируем факторы влияющие на общую стоимость объекта</a></span></li><li><span><a href="#Расчитать-среднюю-цену-одного-квадратного-метра-в-10-населённых-пунктах-с-наибольшим-числом-объявлений." data-toc-modified-id="Расчитать-среднюю-цену-одного-квадратного-метра-в-10-населённых-пунктах-с-наибольшим-числом-объявлений.-4.17"><span class="toc-item-num">4.17&nbsp;&nbsp;</span>Расчитать среднюю цену одного квадратного метра в 10 населённых пунктах с наибольшим числом объявлений.</a></span></li></ul></li><li><span><a href="#Общий-вывод" data-toc-modified-id="Общий-вывод-5"><span class="toc-item-num">5&nbsp;&nbsp;</span>Общий вывод</a></span></li></ul></div>

# Исследование объявлений о продаже квартир

В нашем распоряжении данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. В процессе проведения исследования необходимо определить рыночную стоимость объектов недвижимости. Основная задача исседования — установить параметры, влияющие на продажу квартир. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность.

По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма.

**Описание данных:**

- **airports_nearest**    — расстояние до ближайшего аэропорта в метрах (м)
- **balcony**             — число балконов
- **ceiling_height** — высота потолков (м)
- **cityCenters_nearest** — расстояние до центра города (м)
- **days_exposition** — сколько дней было размещено объявление (от публикации до снятия)
- **first_day_exposition** — дата публикации
- **floor** — этаж
- **floors_total** — всего этажей в доме
- **is_apartment** — апартаменты (булев тип)
- **kitchen_area** — площадь кухни в квадратных метрах (м²)
- **last_price** — цена на момент снятия с публикации
- **living_area** — жилая площадь в квадратных метрах (м²)
- **locality_name** — название населённого пункта
- **open_plan** — свободная планировка (булев тип)
- **parks_around3000** — число парков в радиусе 3 км
- **parks_nearest** — расстояние до ближайшего парка (м)
- **ponds_around3000** — число водоёмов в радиусе 3 км
- **ponds_nearest** — расстояние до ближайшего водоёма (м)
- **rooms** — число комнат
- **studio** — квартира-студия (булев тип)
- **total_area** — общая площадь квартиры в квадратных метрах (м²)
- **total_images** — число фотографий квартиры в объявлении

**Цель исследования:**

- Получить информацию о времени продажи квартиры.
- Найти факторы, которые большего всего влияют на стоимость квартиры.
- Изучить предложение квартир по локации.
- Выделить и получить информацию по квартирам в центре Санкт-Петербурга.

**Ход исследования:**

В файле **"real_estate_data.csv"** содержится архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктах за несколько лет. 

**По каждой квартире на продажу доступны два вида данных:**

1) пользовательские; 

2) получены автоматически на основе картографических данных.

Т. к. часть данных записаны пользователями, они могут содержать ошибки. Ошибки также могут быть и в данных, полученных автоматически на основе картографических данных. Для начала нужен обзор данных. Далее, буду делать предобработку данных. Искать аномалии, пропущенные значения и т.д..

**Для решения поставленных задач необходимо рассчитать и добавить в таблицу несколько показателей:**

- цена за 1 квадратный метр,
- день недели, месяц и год публикации объявления,
- этаж квартиры (первый, последний, другой).
    
**Таким образом, исследование пройдёт в 5 этапов:**

- Обзор данных.
- Предобработка данных.
- Расчёты и добавление результатов в таблицу.
- Исследовательский анализ данных.
- Выводы

## Открываем файл с данными и изучаем общую информацию

### Импортируем библиотеки для работы с файлами


```python
# импортируем необходимые дляработы библиотеки

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### Загружаем данные из csv-файла в датафрейм c помощью библиотеки pandas.


```python
# для исключения ошибок загрузки данных воспльзуемя методом "try - except"

try:
    data = pd.read_csv('/datasets/real_estate_data.csv', sep='\t')
except:
    data = pd.read_csv('https://code.s3.yandex.net/datasets/real_estate_data.csv', sep='\t')
```

### Первичный взгляд на полученные данные


```python
# выведем на экран 5 строк таблицы для ознакомления

pd.set_option('display.max_columns', None)
data['last_price'] = data['last_price']/1000000
data.head()
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>cityCenters_nearest</th>
      <th>parks_around3000</th>
      <th>parks_nearest</th>
      <th>ponds_around3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20</td>
      <td>13.000</td>
      <td>108.0</td>
      <td>2019-03-07T00:00:00</td>
      <td>3</td>
      <td>2.70</td>
      <td>16.0</td>
      <td>51.0</td>
      <td>8</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>25.0</td>
      <td>NaN</td>
      <td>Санкт-Петербург</td>
      <td>18863.0</td>
      <td>16028.0</td>
      <td>1.0</td>
      <td>482.0</td>
      <td>2.0</td>
      <td>755.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>3.350</td>
      <td>40.4</td>
      <td>2018-12-04T00:00:00</td>
      <td>1</td>
      <td>NaN</td>
      <td>11.0</td>
      <td>18.6</td>
      <td>1</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>11.0</td>
      <td>2.0</td>
      <td>посёлок Шушары</td>
      <td>12817.0</td>
      <td>18603.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>81.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>10</td>
      <td>5.196</td>
      <td>56.0</td>
      <td>2015-08-20T00:00:00</td>
      <td>2</td>
      <td>NaN</td>
      <td>5.0</td>
      <td>34.3</td>
      <td>4</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>8.3</td>
      <td>0.0</td>
      <td>Санкт-Петербург</td>
      <td>21741.0</td>
      <td>13933.0</td>
      <td>1.0</td>
      <td>90.0</td>
      <td>2.0</td>
      <td>574.0</td>
      <td>558.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>64.900</td>
      <td>159.0</td>
      <td>2015-07-24T00:00:00</td>
      <td>3</td>
      <td>NaN</td>
      <td>14.0</td>
      <td>NaN</td>
      <td>9</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>Санкт-Петербург</td>
      <td>28098.0</td>
      <td>6800.0</td>
      <td>2.0</td>
      <td>84.0</td>
      <td>3.0</td>
      <td>234.0</td>
      <td>424.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>10.000</td>
      <td>100.0</td>
      <td>2018-06-19T00:00:00</td>
      <td>2</td>
      <td>3.03</td>
      <td>14.0</td>
      <td>32.0</td>
      <td>13</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>41.0</td>
      <td>NaN</td>
      <td>Санкт-Петербург</td>
      <td>31856.0</td>
      <td>8098.0</td>
      <td>2.0</td>
      <td>112.0</td>
      <td>1.0</td>
      <td>48.0</td>
      <td>121.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# выведем на экран 10 случайных строк таблицы

data.sample(10)
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>cityCenters_nearest</th>
      <th>parks_around3000</th>
      <th>parks_nearest</th>
      <th>ponds_around3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>16076</th>
      <td>1</td>
      <td>6.30000</td>
      <td>88.0</td>
      <td>2018-11-02T00:00:00</td>
      <td>3</td>
      <td>2.60</td>
      <td>9.0</td>
      <td>40.0</td>
      <td>1</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Всеволожск</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>107.0</td>
    </tr>
    <tr>
      <th>9951</th>
      <td>11</td>
      <td>16.55000</td>
      <td>180.6</td>
      <td>2017-07-14T00:00:00</td>
      <td>3</td>
      <td>3.50</td>
      <td>10.0</td>
      <td>83.5</td>
      <td>10</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>48.0</td>
      <td>1.0</td>
      <td>Санкт-Петербург</td>
      <td>39892.0</td>
      <td>15176.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9542</th>
      <td>8</td>
      <td>4.10000</td>
      <td>46.0</td>
      <td>2017-09-10T00:00:00</td>
      <td>2</td>
      <td>2.55</td>
      <td>9.0</td>
      <td>28.5</td>
      <td>9</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>7.0</td>
      <td>2.0</td>
      <td>Санкт-Петербург</td>
      <td>32103.0</td>
      <td>12696.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>91.0</td>
    </tr>
    <tr>
      <th>10361</th>
      <td>5</td>
      <td>28.80000</td>
      <td>187.0</td>
      <td>2017-04-09T00:00:00</td>
      <td>3</td>
      <td>NaN</td>
      <td>15.0</td>
      <td>92.5</td>
      <td>3</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>34.0</td>
      <td>0.0</td>
      <td>Санкт-Петербург</td>
      <td>31744.0</td>
      <td>4836.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>3.0</td>
      <td>153.0</td>
      <td>176.0</td>
    </tr>
    <tr>
      <th>11078</th>
      <td>1</td>
      <td>2.39100</td>
      <td>39.9</td>
      <td>2018-08-02T00:00:00</td>
      <td>1</td>
      <td>NaN</td>
      <td>25.0</td>
      <td>18.6</td>
      <td>18</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>9.7</td>
      <td>NaN</td>
      <td>посёлок Парголово</td>
      <td>55827.0</td>
      <td>21502.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>25.0</td>
    </tr>
    <tr>
      <th>21418</th>
      <td>1</td>
      <td>2.52757</td>
      <td>42.4</td>
      <td>2016-11-25T00:00:00</td>
      <td>1</td>
      <td>2.56</td>
      <td>18.0</td>
      <td>19.9</td>
      <td>16</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Никольское</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>549.0</td>
    </tr>
    <tr>
      <th>12145</th>
      <td>10</td>
      <td>5.30000</td>
      <td>62.0</td>
      <td>2016-09-01T00:00:00</td>
      <td>3</td>
      <td>2.60</td>
      <td>8.0</td>
      <td>36.0</td>
      <td>6</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>9.0</td>
      <td>2.0</td>
      <td>Санкт-Петербург</td>
      <td>24926.0</td>
      <td>16005.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>134.0</td>
    </tr>
    <tr>
      <th>16725</th>
      <td>9</td>
      <td>6.40000</td>
      <td>35.0</td>
      <td>2019-04-27T00:00:00</td>
      <td>1</td>
      <td>NaN</td>
      <td>18.0</td>
      <td>18.0</td>
      <td>5</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>10.0</td>
      <td>1.0</td>
      <td>Санкт-Петербург</td>
      <td>11187.0</td>
      <td>13491.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3561</th>
      <td>5</td>
      <td>12.30000</td>
      <td>115.0</td>
      <td>2017-08-09T00:00:00</td>
      <td>3</td>
      <td>2.70</td>
      <td>20.0</td>
      <td>45.0</td>
      <td>16</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>60.0</td>
      <td>1.0</td>
      <td>Санкт-Петербург</td>
      <td>33386.0</td>
      <td>14234.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>63.0</td>
    </tr>
    <tr>
      <th>253</th>
      <td>17</td>
      <td>3.34000</td>
      <td>37.0</td>
      <td>2018-03-28T00:00:00</td>
      <td>1</td>
      <td>NaN</td>
      <td>5.0</td>
      <td>19.0</td>
      <td>4</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>10.0</td>
      <td>NaN</td>
      <td>Санкт-Петербург</td>
      <td>47303.0</td>
      <td>25866.0</td>
      <td>1.0</td>
      <td>251.0</td>
      <td>1.0</td>
      <td>350.0</td>
      <td>75.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# посмотрим min, max, среднее и т.д.

data.describe().T
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
      <th>total_images</th>
      <td>23699.0</td>
      <td>9.858475</td>
      <td>5.682529</td>
      <td>0.00000</td>
      <td>6.00</td>
      <td>9.00</td>
      <td>14.0</td>
      <td>50.0</td>
    </tr>
    <tr>
      <th>last_price</th>
      <td>23699.0</td>
      <td>6.541549</td>
      <td>10.887013</td>
      <td>0.01219</td>
      <td>3.40</td>
      <td>4.65</td>
      <td>6.8</td>
      <td>763.0</td>
    </tr>
    <tr>
      <th>total_area</th>
      <td>23699.0</td>
      <td>60.348651</td>
      <td>35.654083</td>
      <td>12.00000</td>
      <td>40.00</td>
      <td>52.00</td>
      <td>69.9</td>
      <td>900.0</td>
    </tr>
    <tr>
      <th>rooms</th>
      <td>23699.0</td>
      <td>2.070636</td>
      <td>1.078405</td>
      <td>0.00000</td>
      <td>1.00</td>
      <td>2.00</td>
      <td>3.0</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>ceiling_height</th>
      <td>14504.0</td>
      <td>2.771499</td>
      <td>1.261056</td>
      <td>1.00000</td>
      <td>2.52</td>
      <td>2.65</td>
      <td>2.8</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>floors_total</th>
      <td>23613.0</td>
      <td>10.673824</td>
      <td>6.597173</td>
      <td>1.00000</td>
      <td>5.00</td>
      <td>9.00</td>
      <td>16.0</td>
      <td>60.0</td>
    </tr>
    <tr>
      <th>living_area</th>
      <td>21796.0</td>
      <td>34.457852</td>
      <td>22.030445</td>
      <td>2.00000</td>
      <td>18.60</td>
      <td>30.00</td>
      <td>42.3</td>
      <td>409.7</td>
    </tr>
    <tr>
      <th>floor</th>
      <td>23699.0</td>
      <td>5.892358</td>
      <td>4.885249</td>
      <td>1.00000</td>
      <td>2.00</td>
      <td>4.00</td>
      <td>8.0</td>
      <td>33.0</td>
    </tr>
    <tr>
      <th>kitchen_area</th>
      <td>21421.0</td>
      <td>10.569807</td>
      <td>5.905438</td>
      <td>1.30000</td>
      <td>7.00</td>
      <td>9.10</td>
      <td>12.0</td>
      <td>112.0</td>
    </tr>
    <tr>
      <th>balcony</th>
      <td>12180.0</td>
      <td>1.150082</td>
      <td>1.071300</td>
      <td>0.00000</td>
      <td>0.00</td>
      <td>1.00</td>
      <td>2.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>airports_nearest</th>
      <td>18157.0</td>
      <td>28793.672193</td>
      <td>12630.880622</td>
      <td>0.00000</td>
      <td>18585.00</td>
      <td>26726.00</td>
      <td>37273.0</td>
      <td>84869.0</td>
    </tr>
    <tr>
      <th>cityCenters_nearest</th>
      <td>18180.0</td>
      <td>14191.277833</td>
      <td>8608.386210</td>
      <td>181.00000</td>
      <td>9238.00</td>
      <td>13098.50</td>
      <td>16293.0</td>
      <td>65968.0</td>
    </tr>
    <tr>
      <th>parks_around3000</th>
      <td>18181.0</td>
      <td>0.611408</td>
      <td>0.802074</td>
      <td>0.00000</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>parks_nearest</th>
      <td>8079.0</td>
      <td>490.804555</td>
      <td>342.317995</td>
      <td>1.00000</td>
      <td>288.00</td>
      <td>455.00</td>
      <td>612.0</td>
      <td>3190.0</td>
    </tr>
    <tr>
      <th>ponds_around3000</th>
      <td>18181.0</td>
      <td>0.770255</td>
      <td>0.938346</td>
      <td>0.00000</td>
      <td>0.00</td>
      <td>1.00</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>ponds_nearest</th>
      <td>9110.0</td>
      <td>517.980900</td>
      <td>277.720643</td>
      <td>13.00000</td>
      <td>294.00</td>
      <td>502.00</td>
      <td>729.0</td>
      <td>1344.0</td>
    </tr>
    <tr>
      <th>days_exposition</th>
      <td>20518.0</td>
      <td>180.888634</td>
      <td>219.727988</td>
      <td>1.00000</td>
      <td>45.00</td>
      <td>95.00</td>
      <td>232.0</td>
      <td>1580.0</td>
    </tr>
  </tbody>
</table>
</div>



### Выведем статистику по исходным данным


```python
data.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 23699 entries, 0 to 23698
    Data columns (total 22 columns):
     #   Column                Non-Null Count  Dtype  
    ---  ------                --------------  -----  
     0   total_images          23699 non-null  int64  
     1   last_price            23699 non-null  float64
     2   total_area            23699 non-null  float64
     3   first_day_exposition  23699 non-null  object 
     4   rooms                 23699 non-null  int64  
     5   ceiling_height        14504 non-null  float64
     6   floors_total          23613 non-null  float64
     7   living_area           21796 non-null  float64
     8   floor                 23699 non-null  int64  
     9   is_apartment          2775 non-null   object 
     10  studio                23699 non-null  bool   
     11  open_plan             23699 non-null  bool   
     12  kitchen_area          21421 non-null  float64
     13  balcony               12180 non-null  float64
     14  locality_name         23650 non-null  object 
     15  airports_nearest      18157 non-null  float64
     16  cityCenters_nearest   18180 non-null  float64
     17  parks_around3000      18181 non-null  float64
     18  parks_nearest         8079 non-null   float64
     19  ponds_around3000      18181 non-null  float64
     20  ponds_nearest         9110 non-null   float64
     21  days_exposition       20518 non-null  float64
    dtypes: bool(2), float64(14), int64(3), object(3)
    memory usage: 3.7+ MB
    

**Вывод на основе описательных данных:**

1. **last_price:** - минимальная цена квартиры 12190 руб., что явно не характерно для рынка СПб и ЛО. Похоже на ошибку. Максимальная цена 763 000 000 руб. очень большая, но для исторических/элитных объектов возможна. НО! Такие значения могут плохо влиять на среднее значение, вероятно, большие данные тоже стоит исключить.

2. **rooms:** - минимальное число комнат 0 - ошибка. Как вариант это может быть квартира-студия. Нужно проверить.

3. **ceiling_height:** - минимальная высота потолков 1 метр, максимальная - 100 метров. Явно ошибка. Такие значения будем удалять.

4. **floors_total:** - max количество этажей 60 - похоже на ошибку, самое высокое здание в Санкт-Петербурге и окретностях - Лахта имеет 35 этажей. Такие объекты следует удалить.

5. **living_area:** - min жилая площадь 2 м² невозможна - ошибка. Такие объекты следует удалить.

6. **kitchen_area:** - min площадь кухни 1,3 м² невозможна - ошибка. Такие объекты следует удалить.

7. **airports_nearest:** - min расстояние до аэропорта 0 м невозможно. Два варианта событий: либо нет данных и заполнили нулем, либо ошибка. Такие объекты следует удалить.

8. **days_exposition:** - минимальное количество дней размещения объявления - 1. Продажа недвижимости за 1 день или снятие объявления по другой причине - допустимый вариант, но, если таких объявлений много, то такие данные могут негативно влиять на среднее. Максимальное значение - 1580 дней (больше 4-х лет) также может негативно влиять на среднее время.

### Проверим таблицу на наличие явных дубликатов.


```python
print('\033[1m' + 'Количество явных дубликатов в таблице:' + '\033[0m', data.duplicated().sum())
```

    [1mКоличество явных дубликатов в таблице:[0m 0
    

### Проверим количество пропусков


```python
data.isna().sum()
```




    total_images                0
    last_price                  0
    total_area                  0
    first_day_exposition        0
    rooms                       0
    ceiling_height           9195
    floors_total               86
    living_area              1903
    floor                       0
    is_apartment            20924
    studio                      0
    open_plan                   0
    kitchen_area             2278
    balcony                 11519
    locality_name              49
    airports_nearest         5542
    cityCenters_nearest      5519
    parks_around3000         5518
    parks_nearest           15620
    ponds_around3000         5518
    ponds_nearest           14589
    days_exposition          3181
    dtype: int64




```python
pd.DataFrame(round(data.isna().mean()*100,)).style.background_gradient('coolwarm')
```




<style type="text/css">
#T_bcc74_row0_col0, #T_bcc74_row1_col0, #T_bcc74_row2_col0, #T_bcc74_row3_col0, #T_bcc74_row4_col0, #T_bcc74_row6_col0, #T_bcc74_row8_col0, #T_bcc74_row10_col0, #T_bcc74_row11_col0, #T_bcc74_row14_col0 {
  background-color: #3b4cc0;
  color: #f1f1f1;
}
#T_bcc74_row5_col0 {
  background-color: #cdd9ec;
  color: #000000;
}
#T_bcc74_row7_col0 {
  background-color: #5673e0;
  color: #f1f1f1;
}
#T_bcc74_row9_col0 {
  background-color: #b40426;
  color: #f1f1f1;
}
#T_bcc74_row12_col0 {
  background-color: #5e7de7;
  color: #f1f1f1;
}
#T_bcc74_row13_col0 {
  background-color: #ead4c8;
  color: #000000;
}
#T_bcc74_row15_col0, #T_bcc74_row16_col0, #T_bcc74_row17_col0, #T_bcc74_row19_col0 {
  background-color: #90b2fe;
  color: #000000;
}
#T_bcc74_row18_col0 {
  background-color: #f4987a;
  color: #000000;
}
#T_bcc74_row20_col0 {
  background-color: #f7aa8c;
  color: #000000;
}
#T_bcc74_row21_col0 {
  background-color: #688aef;
  color: #f1f1f1;
}
</style>
<table id="T_bcc74">
  <thead>
    <tr>
      <th class="blank level0" >&nbsp;</th>
      <th id="T_bcc74_level0_col0" class="col_heading level0 col0" >0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th id="T_bcc74_level0_row0" class="row_heading level0 row0" >total_images</th>
      <td id="T_bcc74_row0_col0" class="data row0 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row1" class="row_heading level0 row1" >last_price</th>
      <td id="T_bcc74_row1_col0" class="data row1 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row2" class="row_heading level0 row2" >total_area</th>
      <td id="T_bcc74_row2_col0" class="data row2 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row3" class="row_heading level0 row3" >first_day_exposition</th>
      <td id="T_bcc74_row3_col0" class="data row3 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row4" class="row_heading level0 row4" >rooms</th>
      <td id="T_bcc74_row4_col0" class="data row4 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row5" class="row_heading level0 row5" >ceiling_height</th>
      <td id="T_bcc74_row5_col0" class="data row5 col0" >39.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row6" class="row_heading level0 row6" >floors_total</th>
      <td id="T_bcc74_row6_col0" class="data row6 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row7" class="row_heading level0 row7" >living_area</th>
      <td id="T_bcc74_row7_col0" class="data row7 col0" >8.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row8" class="row_heading level0 row8" >floor</th>
      <td id="T_bcc74_row8_col0" class="data row8 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row9" class="row_heading level0 row9" >is_apartment</th>
      <td id="T_bcc74_row9_col0" class="data row9 col0" >88.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row10" class="row_heading level0 row10" >studio</th>
      <td id="T_bcc74_row10_col0" class="data row10 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row11" class="row_heading level0 row11" >open_plan</th>
      <td id="T_bcc74_row11_col0" class="data row11 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row12" class="row_heading level0 row12" >kitchen_area</th>
      <td id="T_bcc74_row12_col0" class="data row12 col0" >10.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row13" class="row_heading level0 row13" >balcony</th>
      <td id="T_bcc74_row13_col0" class="data row13 col0" >49.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row14" class="row_heading level0 row14" >locality_name</th>
      <td id="T_bcc74_row14_col0" class="data row14 col0" >0.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row15" class="row_heading level0 row15" >airports_nearest</th>
      <td id="T_bcc74_row15_col0" class="data row15 col0" >23.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row16" class="row_heading level0 row16" >cityCenters_nearest</th>
      <td id="T_bcc74_row16_col0" class="data row16 col0" >23.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row17" class="row_heading level0 row17" >parks_around3000</th>
      <td id="T_bcc74_row17_col0" class="data row17 col0" >23.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row18" class="row_heading level0 row18" >parks_nearest</th>
      <td id="T_bcc74_row18_col0" class="data row18 col0" >66.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row19" class="row_heading level0 row19" >ponds_around3000</th>
      <td id="T_bcc74_row19_col0" class="data row19 col0" >23.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row20" class="row_heading level0 row20" >ponds_nearest</th>
      <td id="T_bcc74_row20_col0" class="data row20 col0" >62.000000</td>
    </tr>
    <tr>
      <th id="T_bcc74_level0_row21" class="row_heading level0 row21" >days_exposition</th>
      <td id="T_bcc74_row21_col0" class="data row21 col0" >13.000000</td>
    </tr>
  </tbody>
</table>




### Построим гистограмму для всех числовых столбцов таблицы на одном графике


```python
# для построения гистограмм используем команду: data.hist(figsize=(20, 25)

data.hist(figsize= (20, 25))
plt.show()
```


    
![png](output_24_0.png)
    


**Вывод:**

1. Прочитал файл.
2. Необходимо изменить тип данных в столбцах:


- **last_price:** вещественное число float64 → int64
- **first_day_exposition:** строка object → datetime
- **floors_total:** вещественное число float64, по вводным данным целое число (этажей) → int64
- **is_apartment:** строка object, по вводным данным булев тип → bool
- **balcony:** вещественное число float64, по вводным данным целое число (балконов) → int64
- **parks_around3000:** вещественное число float64, по вводным данным целое число (парков) → int64
- **ponds_around3000:** вещественное число float64, по вводным данным целое число (водоемов) → int64
- **days_exposition:** вещественное число float64, по вводным данным целое число (дней) → int64

3. Большое количество пропусков в большинстве столбцов. Необходимо исправлять.
4. На основе вывода по описательным данным, буду корректировать некоторые значения.
5. Приведем названия столбцов к единому стилю.

## Предобработка данных

### Приведем имена столбцов к единому стилю


```python
# переименовываем столбцы

data = data.rename(columns={'cityCenters_nearest': 'city_centers_nearest', 
                            'parks_around3000': 'parks_around_3000', 
                            'ponds_around3000': 'ponds_around_3000'})
# проверим

data.head()
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>city_centers_nearest</th>
      <th>parks_around_3000</th>
      <th>parks_nearest</th>
      <th>ponds_around_3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20</td>
      <td>13.000</td>
      <td>108.0</td>
      <td>2019-03-07T00:00:00</td>
      <td>3</td>
      <td>2.70</td>
      <td>16.0</td>
      <td>51.0</td>
      <td>8</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>25.0</td>
      <td>NaN</td>
      <td>Санкт-Петербург</td>
      <td>18863.0</td>
      <td>16028.0</td>
      <td>1.0</td>
      <td>482.0</td>
      <td>2.0</td>
      <td>755.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>3.350</td>
      <td>40.4</td>
      <td>2018-12-04T00:00:00</td>
      <td>1</td>
      <td>NaN</td>
      <td>11.0</td>
      <td>18.6</td>
      <td>1</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>11.0</td>
      <td>2.0</td>
      <td>посёлок Шушары</td>
      <td>12817.0</td>
      <td>18603.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>81.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>10</td>
      <td>5.196</td>
      <td>56.0</td>
      <td>2015-08-20T00:00:00</td>
      <td>2</td>
      <td>NaN</td>
      <td>5.0</td>
      <td>34.3</td>
      <td>4</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>8.3</td>
      <td>0.0</td>
      <td>Санкт-Петербург</td>
      <td>21741.0</td>
      <td>13933.0</td>
      <td>1.0</td>
      <td>90.0</td>
      <td>2.0</td>
      <td>574.0</td>
      <td>558.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>64.900</td>
      <td>159.0</td>
      <td>2015-07-24T00:00:00</td>
      <td>3</td>
      <td>NaN</td>
      <td>14.0</td>
      <td>NaN</td>
      <td>9</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>Санкт-Петербург</td>
      <td>28098.0</td>
      <td>6800.0</td>
      <td>2.0</td>
      <td>84.0</td>
      <td>3.0</td>
      <td>234.0</td>
      <td>424.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>10.000</td>
      <td>100.0</td>
      <td>2018-06-19T00:00:00</td>
      <td>2</td>
      <td>3.03</td>
      <td>14.0</td>
      <td>32.0</td>
      <td>13</td>
      <td>NaN</td>
      <td>False</td>
      <td>False</td>
      <td>41.0</td>
      <td>NaN</td>
      <td>Санкт-Петербург</td>
      <td>31856.0</td>
      <td>8098.0</td>
      <td>2.0</td>
      <td>112.0</td>
      <td>1.0</td>
      <td>48.0</td>
      <td>121.0</td>
    </tr>
  </tbody>
</table>
</div>



### Обрабатаем пропуски в данных


```python
# посмотрим еще раз количество пропусков

data.isna().sum()
```




    total_images                0
    last_price                  0
    total_area                  0
    first_day_exposition        0
    rooms                       0
    ceiling_height           9195
    floors_total               86
    living_area              1903
    floor                       0
    is_apartment            20924
    studio                      0
    open_plan                   0
    kitchen_area             2278
    balcony                 11519
    locality_name              49
    airports_nearest         5542
    city_centers_nearest     5519
    parks_around_3000        5518
    parks_nearest           15620
    ponds_around_3000        5518
    ponds_nearest           14589
    days_exposition          3181
    dtype: int64



В 14 столбцах из 22 присутствуют пропуски:

1. **ceiling_height:** - 9195 пропусков. Почти 40% объявлений не имеют информацию о высоте потолков, это очень большое количество. Данные по этому столбцу для нашего исследования не так важны. Но, следует принять, что для более чем трети объектов он не указан. Пропуски оставляем.
    
2. **floors_total:** - 86 пропусков. Пропусков мало, на исследование не повлияют. Пропуски оставляем.
    
3. **living_area:** - 1903 пропуска. Вероятно, пользователи не помнят точную площадь, поэтому не пишут ее. Кол-во пропусков менее 10%, но данные по этому столбцу нужны нам для исследования. Однако, заполнить значения нечем, оставим пропуски.
    
4. **is_apartment:** -  20924 пропусков. Вероятно, пользователи часто не указывают тип недвижимости, если он просто жилой. Т.к. в этом столбце булев тип данных, пропуски можно заменить на False.
    
5. **kitchen_area:** - 2278 пропусков. Вероятно, пользователи не указывают точный метраж кухни, т.к. не знают его. Кол-во пропусков менее 10%, но нам важны эти данные для исследования. Заполнить значения нечем, оставим пропуски.
    
6. **balcony:** - 11519 пропусков. Вероятно, пользователи при отсутствии балконов их не указывают. В таком случае заменим пропуски нулями.
    
7. **locality_name:** - 49 пропусков. Кол-во пропусков мало, на исследование не повлияют, оставим пропуски.
    
8. **airports_nearest:** - 5542 пропусков. Вероятно, пропуски возникли в связи с отсутствием информации на картографических данных. Поэтому пропуски оставим.
    
9. **city_centers_nearest:** - 5519 пропусков. Вероятно, пропуски возникли в связи с отсутствием информации на картографических данных. Пропуски в столбце на исследование не повлияют. Поэтому пропуски оставим.
    
10. **parks_around_3000:** - 5518 пропусков. Число пропусков совпадает с числом пропусков в ponds_around_3000, что подозрительно. Возможно, для этих объектов не была получена информация на основе картографических данных. Пропуски в столбце на задачи исследования не влияют, оставим их.
    
11. **parks_nearest:** - 15620 пропусков. Более половины объектов не имеют информации о ближайшем парке. Скорее всего, информация на основе картографических данных не была получена. Пропуски в столбце на задачи исследования не влияют, оставим их.
    
12. **ponds_around_3000:** - 5518 пропусков. Число совпадает с числом пропусков parks_around_3000, что выглядит подозрительно. Скорее всего, для этих объектов не была получена информация на основе картографических данных. Пропуски в столбце на исследование не влияют, оставим их.
    
13. **ponds_nearest:** - 14589 пропусков. Больше половины объектов не имеют информации о ближайшем парке. Скорее всего, информация на основе картографических данных не была получена. Пропуски в столбце на задачи исследования не влияют, оставим их.
    
14. **days_exposition:** - 3181 пропусков. 13% объявлений не содержат информации о количестве дней размещения объявления, подозрительно, т.к. эти данные должны быть получены автоматом. Возможно, это техническая ошибка, которая произошла в момент сбора/выгрузки данных. Данные этого столбца важны для исследования. Заполнить значения нечем, оставим пропуски.

**Итог:**

*Обработаем пропуски в столбцах is_apartment (меняем на False) и balcony (меняем на 0).*


```python
# заменяем пропуски на False

data['is_apartment'].fillna(False, inplace=True)

# проверим

print('\033[1m' + 'Количество пропусков в столбце "is_apartment" :' + '\033[0m', data['is_apartment'].isna().sum())
```

    [1mКоличество пропусков в столбце "is_apartment" :[0m 0
    


```python
# заменяем пропуски на 0

data['balcony'].fillna(0, inplace=True)

# проверим

print('\033[1m' + 'Количество пропусков в столбце "balcony" :' + '\033[0m', data['balcony'].isna().sum())
```

    [1mКоличество пропусков в столбце "balcony" :[0m 0
    

Пропуски в столбцах **is_apartment** и **balcony** - отсутствуют.


```python
# заполним пропуски по высоте потолков медианным значением относительно населенных пунктов

for locality in data['locality_name'].unique():
    median_value = data.loc[data['locality_name'] == locality, 'ceiling_height'].median()
    data.loc[(data['ceiling_height'].isna()) & (data['locality_name'] == locality), 'ceiling_height'].median()

data.loc[data['ceiling_height'].isna(), 'ceiling_height'] = data['ceiling_height'].median()
```

### Преобразуем типы данных

Изначально мы выделили столбцы, в которых нужно преобразовать один тип данных в другой. В ходе обработки пропусков получили, 
что некоторые пропуски убрать не удалось => преобразовать в другой тип(int64) также не получится. Для этих случаев оставим 
тип float64.

Меняем тип в следующих столбцах last_price(int64), first_day_exposition(datetime), is_apartment(boolean), balcony(int64)


```python
# преобразуем столбцы 'last_price', 'balcony' к типу данных int

data[['last_price', 'balcony']] = data[['last_price', 'balcony']].apply(lambda x: x.astype('int64'))

# проверим

data[['last_price', 'balcony']].dtypes
```




    last_price    int64
    balcony       int64
    dtype: object




```python
# преобразуем first_day_exposition к типу datetime с помощью pd.to_datetime

data['first_day_exposition'] = pd.to_datetime(data['first_day_exposition'], format='%Y-%m-%dT%H:%M:%S')

# проверяем

data.dtypes
```




    total_images                     int64
    last_price                       int64
    total_area                     float64
    first_day_exposition    datetime64[ns]
    rooms                            int64
    ceiling_height                 float64
    floors_total                   float64
    living_area                    float64
    floor                            int64
    is_apartment                      bool
    studio                            bool
    open_plan                         bool
    kitchen_area                   float64
    balcony                          int64
    locality_name                   object
    airports_nearest               float64
    city_centers_nearest           float64
    parks_around_3000              float64
    parks_nearest                  float64
    ponds_around_3000              float64
    ponds_nearest                  float64
    days_exposition                float64
    dtype: object




```python
# преобразуем к булевому типу

data['is_apartment'] = data['is_apartment'].astype('boolean')

# проверим

data['is_apartment'].dtypes
```




    BooleanDtype




```python
# заменяем тип данных с float64 на float32 для экономии памяти

float64_cols = list(data.select_dtypes(include='float64'))
data[float64_cols] = data[float64_cols].astype('float32')
data.dtypes
```




    total_images                     int64
    last_price                       int64
    total_area                     float32
    first_day_exposition    datetime64[ns]
    rooms                            int64
    ceiling_height                 float32
    floors_total                   float32
    living_area                    float32
    floor                            int64
    is_apartment                   boolean
    studio                            bool
    open_plan                         bool
    kitchen_area                   float32
    balcony                          int64
    locality_name                   object
    airports_nearest               float32
    city_centers_nearest           float32
    parks_around_3000              float32
    parks_nearest                  float32
    ponds_around_3000              float32
    ponds_nearest                  float32
    days_exposition                float32
    dtype: object



### Обрабатываем дубликаты

#### Явные дубликаты


```python
# проверим еще раз дубликаты и выведем их сумму

print('\033[1m' + 'Количество явных дубликатов в таблице :' + '\033[0m', data.duplicated().sum())
```

    [1mКоличество явных дубликатов в таблице :[0m 0
    

*Явных дубликатов не обнаружено*

#### Неявные дубликаты


```python
# выведем уникальные значения столбца locality_name

data['locality_name'].sort_values().unique()
```




    array(['Бокситогорск', 'Волосово', 'Волхов', 'Всеволожск', 'Выборг',
           'Высоцк', 'Гатчина', 'Зеленогорск', 'Ивангород', 'Каменногорск',
           'Кингисепп', 'Кириши', 'Кировск', 'Колпино', 'Коммунар',
           'Красное Село', 'Кронштадт', 'Кудрово', 'Лодейное Поле',
           'Ломоносов', 'Луга', 'Любань', 'Мурино', 'Никольское',
           'Новая Ладога', 'Отрадное', 'Павловск', 'Петергоф', 'Пикалёво',
           'Подпорожье', 'Приморск', 'Приозерск', 'Пушкин', 'Санкт-Петербург',
           'Светогорск', 'Сертолово', 'Сестрорецк', 'Сланцы', 'Сосновый Бор',
           'Сясьстрой', 'Тихвин', 'Тосно', 'Шлиссельбург',
           'городской поселок Большая Ижора', 'городской поселок Янино-1',
           'городской посёлок Будогощь', 'городской посёлок Виллози',
           'городской посёлок Лесогорский', 'городской посёлок Мга',
           'городской посёлок Назия', 'городской посёлок Новоселье',
           'городской посёлок Павлово', 'городской посёлок Рощино',
           'городской посёлок Свирьстрой', 'городской посёлок Советский',
           'городской посёлок Фёдоровское', 'городской посёлок Янино-1',
           'деревня Агалатово', 'деревня Аро', 'деревня Батово',
           'деревня Бегуницы', 'деревня Белогорка', 'деревня Большая Вруда',
           'деревня Большая Пустомержа', 'деревня Большие Колпаны',
           'деревня Большое Рейзино', 'деревня Большой Сабск', 'деревня Бор',
           'деревня Борисова Грива', 'деревня Ваганово', 'деревня Вартемяги',
           'деревня Вахнова Кара', 'деревня Выскатка', 'деревня Гарболово',
           'деревня Глинка', 'деревня Горбунки', 'деревня Гостилицы',
           'деревня Заклинье', 'деревня Заневка', 'деревня Зимитицы',
           'деревня Извара', 'деревня Иссад', 'деревня Калитино',
           'деревня Кальтино', 'деревня Камышовка', 'деревня Каськово',
           'деревня Келози', 'деревня Кипень', 'деревня Кисельня',
           'деревня Колтуши', 'деревня Коркино', 'деревня Котлы',
           'деревня Кривко', 'деревня Кудрово', 'деревня Кузьмолово',
           'деревня Курковицы', 'деревня Куровицы', 'деревня Куттузи',
           'деревня Лаврики', 'деревня Лаголово', 'деревня Лампово',
           'деревня Лесколово', 'деревня Лопухинка', 'деревня Лупполово',
           'деревня Малая Романовка', 'деревня Малое Верево',
           'деревня Малое Карлино', 'деревня Малые Колпаны',
           'деревня Мануйлово', 'деревня Меньково', 'деревня Мины',
           'деревня Мистолово', 'деревня Ненимяки', 'деревня Нижние Осельки',
           'деревня Нижняя', 'деревня Низино', 'деревня Новое Девяткино',
           'деревня Новолисино', 'деревня Нурма', 'деревня Оржицы',
           'деревня Парицы', 'деревня Пельгора', 'деревня Пеники',
           'деревня Пижма', 'деревня Пикколово', 'деревня Пудомяги',
           'деревня Пустынка', 'деревня Пчева', 'деревня Рабитицы',
           'деревня Разбегаево', 'деревня Раздолье', 'деревня Разметелево',
           'деревня Рапполово', 'деревня Реброво', 'деревня Русско',
           'деревня Сижно', 'деревня Снегирёвка', 'деревня Старая',
           'деревня Старая Пустошь', 'деревня Старое Хинколово',
           'деревня Старополье', 'деревня Старосиверская',
           'деревня Старые Бегуницы', 'деревня Суоранда',
           'деревня Сяськелево', 'деревня Тарасово', 'деревня Терпилицы',
           'деревня Тихковицы', 'деревня Тойворово', 'деревня Торосово',
           'деревня Торошковичи', 'деревня Трубников Бор',
           'деревня Фалилеево', 'деревня Фёдоровское', 'деревня Хапо-Ое',
           'деревня Хязельки', 'деревня Чудской Бор', 'деревня Шпаньково',
           'деревня Щеглово', 'деревня Юкки', 'деревня Ялгино',
           'деревня Яльгелево', 'деревня Ям-Тесово',
           'коттеджный поселок Кивеннапа Север', 'коттеджный поселок Счастье',
           'коттеджный посёлок Лесное', 'поселок Аннино', 'поселок Барышево',
           'поселок Бугры', 'поселок Возрождение', 'поселок Войсковицы',
           'поселок Володарское', 'поселок Гаврилово', 'поселок Гарболово',
           'поселок Гладкое', 'поселок Глажево', 'поселок Глебычево',
           'поселок Гончарово', 'поселок Громово', 'поселок Дружноселье',
           'поселок Елизаветино', 'поселок Жилгородок', 'поселок Жилпосёлок',
           'поселок Житково', 'поселок Заводской', 'поселок Запорожское',
           'поселок Зимитицы', 'поселок Ильичёво', 'поселок Калитино',
           'поселок Каложицы', 'поселок Кингисеппский', 'поселок Кирпичное',
           'поселок Кобралово', 'поселок Кобринское', 'поселок Коммунары',
           'поселок Коробицыно', 'поселок Котельский',
           'поселок Красная Долина', 'поселок Красносельское',
           'поселок Лесное', 'поселок Лисий Нос', 'поселок Лукаши',
           'поселок Любань', 'поселок Мельниково', 'поселок Мичуринское',
           'поселок Молодцово', 'поселок Мурино', 'поселок Новый Свет',
           'поселок Новый Учхоз', 'поселок Оредеж',
           'поселок Пансионат Зелёный Бор', 'поселок Первомайское',
           'поселок Перово', 'поселок Петровское', 'поселок Победа',
           'поселок Поляны', 'поселок Почап', 'поселок Починок',
           'поселок Пушное', 'поселок Пчевжа', 'поселок Рабитицы',
           'поселок Романовка', 'поселок Ромашки', 'поселок Рябово',
           'поселок Севастьяново', 'поселок Селезнёво', 'поселок Сельцо',
           'поселок Семиозерье', 'поселок Семрино', 'поселок Серебрянский',
           'поселок Совхозный', 'поселок Старая Малукса',
           'поселок Стеклянный', 'поселок Сумино', 'поселок Суходолье',
           'поселок Тельмана', 'поселок Терволово', 'поселок Торковичи',
           'поселок Тёсово-4', 'поселок Углово', 'поселок Усть-Луга',
           'поселок Ушаки', 'поселок Цвелодубово', 'поселок Цвылёво',
           'поселок городского типа Большая Ижора',
           'поселок городского типа Вырица',
           'поселок городского типа Дружная Горка',
           'поселок городского типа Дубровка',
           'поселок городского типа Ефимовский',
           'поселок городского типа Кондратьево',
           'поселок городского типа Красный Бор',
           'поселок городского типа Кузьмоловский',
           'поселок городского типа Лебяжье',
           'поселок городского типа Лесогорский',
           'поселок городского типа Назия',
           'поселок городского типа Никольский',
           'поселок городского типа Приладожский',
           'поселок городского типа Рахья', 'поселок городского типа Рощино',
           'поселок городского типа Рябово',
           'поселок городского типа Синявино',
           'поселок городского типа Советский',
           'поселок городского типа Токсово',
           'поселок городского типа Форносово',
           'поселок городского типа имени Свердлова',
           'поселок станции Вещево', 'поселок станции Корнево',
           'поселок станции Лужайка', 'поселок станции Приветнинское',
           'посёлок Александровская', 'посёлок Алексеевка', 'посёлок Аннино',
           'посёлок Белоостров', 'посёлок Бугры', 'посёлок Возрождение',
           'посёлок Войскорово', 'посёлок Высокоключевой',
           'посёлок Гаврилово', 'посёлок Дзержинского', 'посёлок Жилгородок',
           'посёлок Ильичёво', 'посёлок Кикерино', 'посёлок Кобралово',
           'посёлок Коробицыно', 'посёлок Левашово', 'посёлок Ленинское',
           'посёлок Лисий Нос', 'посёлок Мельниково', 'посёлок Металлострой',
           'посёлок Мичуринское', 'посёлок Молодёжное', 'посёлок Мурино',
           'посёлок Мыза-Ивановка', 'посёлок Новогорелово',
           'посёлок Новый Свет', 'посёлок Пансионат Зелёный Бор',
           'посёлок Парголово', 'посёлок Перово', 'посёлок Песочный',
           'посёлок Петро-Славянка', 'посёлок Петровское',
           'посёлок Платформа 69-й километр', 'посёлок Плодовое',
           'посёлок Плоское', 'посёлок Победа', 'посёлок Поляны',
           'посёлок Понтонный', 'посёлок Пригородный', 'посёлок Пудость',
           'посёлок Репино', 'посёлок Ропша', 'посёлок Сапёрное',
           'посёлок Сапёрный', 'посёлок Сосново', 'посёлок Старая Малукса',
           'посёлок Стеклянный', 'посёлок Стрельна', 'посёлок Суйда',
           'посёлок Сумино', 'посёлок Тельмана', 'посёлок Терволово',
           'посёлок Торфяное', 'посёлок Усть-Ижора', 'посёлок Усть-Луга',
           'посёлок Форт Красная Горка', 'посёлок Шугозеро', 'посёлок Шушары',
           'посёлок Щеглово', 'посёлок городского типа Важины',
           'посёлок городского типа Вознесенье',
           'посёлок городского типа Вырица',
           'посёлок городского типа Красный Бор',
           'посёлок городского типа Кузнечное',
           'посёлок городского типа Кузьмоловский',
           'посёлок городского типа Лебяжье', 'посёлок городского типа Мга',
           'посёлок городского типа Павлово',
           'посёлок городского типа Рощино', 'посёлок городского типа Рябово',
           'посёлок городского типа Сиверский',
           'посёлок городского типа Тайцы', 'посёлок городского типа Токсово',
           'посёлок городского типа Ульяновка',
           'посёлок городского типа Форносово',
           'посёлок городского типа имени Морозова',
           'посёлок городского типа имени Свердлова',
           'посёлок при железнодорожной станции Вещево',
           'посёлок при железнодорожной станции Приветнинское',
           'посёлок станции Громово', 'посёлок станции Свирь',
           'садоводческое некоммерческое товарищество Лесная Поляна',
           'садовое товарищество Новая Ропша',
           'садовое товарищество Приладожский', 'садовое товарищество Рахья',
           'садовое товарищество Садко', 'село Копорье', 'село Никольское',
           'село Павлово', 'село Паша', 'село Путилово', 'село Рождествено',
           'село Русско-Высоцкое', 'село Старая Ладога', 'село Шум', nan],
          dtype=object)



Можно заметить что '**поселок**' и '**посёлок**' дублируют значения.


```python
# заменяем поселок на посёлок через replace

data['locality_name'] = data['locality_name'].str.replace('поселок','посёлок')
```


```python
# проверим результаты изменений
data['locality_name'].sort_values().unique()
```




    array(['Бокситогорск', 'Волосово', 'Волхов', 'Всеволожск', 'Выборг',
           'Высоцк', 'Гатчина', 'Зеленогорск', 'Ивангород', 'Каменногорск',
           'Кингисепп', 'Кириши', 'Кировск', 'Колпино', 'Коммунар',
           'Красное Село', 'Кронштадт', 'Кудрово', 'Лодейное Поле',
           'Ломоносов', 'Луга', 'Любань', 'Мурино', 'Никольское',
           'Новая Ладога', 'Отрадное', 'Павловск', 'Петергоф', 'Пикалёво',
           'Подпорожье', 'Приморск', 'Приозерск', 'Пушкин', 'Санкт-Петербург',
           'Светогорск', 'Сертолово', 'Сестрорецк', 'Сланцы', 'Сосновый Бор',
           'Сясьстрой', 'Тихвин', 'Тосно', 'Шлиссельбург',
           'городской посёлок Большая Ижора', 'городской посёлок Будогощь',
           'городской посёлок Виллози', 'городской посёлок Лесогорский',
           'городской посёлок Мга', 'городской посёлок Назия',
           'городской посёлок Новоселье', 'городской посёлок Павлово',
           'городской посёлок Рощино', 'городской посёлок Свирьстрой',
           'городской посёлок Советский', 'городской посёлок Фёдоровское',
           'городской посёлок Янино-1', 'деревня Агалатово', 'деревня Аро',
           'деревня Батово', 'деревня Бегуницы', 'деревня Белогорка',
           'деревня Большая Вруда', 'деревня Большая Пустомержа',
           'деревня Большие Колпаны', 'деревня Большое Рейзино',
           'деревня Большой Сабск', 'деревня Бор', 'деревня Борисова Грива',
           'деревня Ваганово', 'деревня Вартемяги', 'деревня Вахнова Кара',
           'деревня Выскатка', 'деревня Гарболово', 'деревня Глинка',
           'деревня Горбунки', 'деревня Гостилицы', 'деревня Заклинье',
           'деревня Заневка', 'деревня Зимитицы', 'деревня Извара',
           'деревня Иссад', 'деревня Калитино', 'деревня Кальтино',
           'деревня Камышовка', 'деревня Каськово', 'деревня Келози',
           'деревня Кипень', 'деревня Кисельня', 'деревня Колтуши',
           'деревня Коркино', 'деревня Котлы', 'деревня Кривко',
           'деревня Кудрово', 'деревня Кузьмолово', 'деревня Курковицы',
           'деревня Куровицы', 'деревня Куттузи', 'деревня Лаврики',
           'деревня Лаголово', 'деревня Лампово', 'деревня Лесколово',
           'деревня Лопухинка', 'деревня Лупполово',
           'деревня Малая Романовка', 'деревня Малое Верево',
           'деревня Малое Карлино', 'деревня Малые Колпаны',
           'деревня Мануйлово', 'деревня Меньково', 'деревня Мины',
           'деревня Мистолово', 'деревня Ненимяки', 'деревня Нижние Осельки',
           'деревня Нижняя', 'деревня Низино', 'деревня Новое Девяткино',
           'деревня Новолисино', 'деревня Нурма', 'деревня Оржицы',
           'деревня Парицы', 'деревня Пельгора', 'деревня Пеники',
           'деревня Пижма', 'деревня Пикколово', 'деревня Пудомяги',
           'деревня Пустынка', 'деревня Пчева', 'деревня Рабитицы',
           'деревня Разбегаево', 'деревня Раздолье', 'деревня Разметелево',
           'деревня Рапполово', 'деревня Реброво', 'деревня Русско',
           'деревня Сижно', 'деревня Снегирёвка', 'деревня Старая',
           'деревня Старая Пустошь', 'деревня Старое Хинколово',
           'деревня Старополье', 'деревня Старосиверская',
           'деревня Старые Бегуницы', 'деревня Суоранда',
           'деревня Сяськелево', 'деревня Тарасово', 'деревня Терпилицы',
           'деревня Тихковицы', 'деревня Тойворово', 'деревня Торосово',
           'деревня Торошковичи', 'деревня Трубников Бор',
           'деревня Фалилеево', 'деревня Фёдоровское', 'деревня Хапо-Ое',
           'деревня Хязельки', 'деревня Чудской Бор', 'деревня Шпаньково',
           'деревня Щеглово', 'деревня Юкки', 'деревня Ялгино',
           'деревня Яльгелево', 'деревня Ям-Тесово',
           'коттеджный посёлок Кивеннапа Север', 'коттеджный посёлок Лесное',
           'коттеджный посёлок Счастье', 'посёлок Александровская',
           'посёлок Алексеевка', 'посёлок Аннино', 'посёлок Барышево',
           'посёлок Белоостров', 'посёлок Бугры', 'посёлок Возрождение',
           'посёлок Войсковицы', 'посёлок Войскорово', 'посёлок Володарское',
           'посёлок Высокоключевой', 'посёлок Гаврилово', 'посёлок Гарболово',
           'посёлок Гладкое', 'посёлок Глажево', 'посёлок Глебычево',
           'посёлок Гончарово', 'посёлок Громово', 'посёлок Дзержинского',
           'посёлок Дружноселье', 'посёлок Елизаветино', 'посёлок Жилгородок',
           'посёлок Жилпосёлок', 'посёлок Житково', 'посёлок Заводской',
           'посёлок Запорожское', 'посёлок Зимитицы', 'посёлок Ильичёво',
           'посёлок Калитино', 'посёлок Каложицы', 'посёлок Кикерино',
           'посёлок Кингисеппский', 'посёлок Кирпичное', 'посёлок Кобралово',
           'посёлок Кобринское', 'посёлок Коммунары', 'посёлок Коробицыно',
           'посёлок Котельский', 'посёлок Красная Долина',
           'посёлок Красносельское', 'посёлок Левашово', 'посёлок Ленинское',
           'посёлок Лесное', 'посёлок Лисий Нос', 'посёлок Лукаши',
           'посёлок Любань', 'посёлок Мельниково', 'посёлок Металлострой',
           'посёлок Мичуринское', 'посёлок Молодцово', 'посёлок Молодёжное',
           'посёлок Мурино', 'посёлок Мыза-Ивановка', 'посёлок Новогорелово',
           'посёлок Новый Свет', 'посёлок Новый Учхоз', 'посёлок Оредеж',
           'посёлок Пансионат Зелёный Бор', 'посёлок Парголово',
           'посёлок Первомайское', 'посёлок Перово', 'посёлок Песочный',
           'посёлок Петро-Славянка', 'посёлок Петровское',
           'посёлок Платформа 69-й километр', 'посёлок Плодовое',
           'посёлок Плоское', 'посёлок Победа', 'посёлок Поляны',
           'посёлок Понтонный', 'посёлок Почап', 'посёлок Починок',
           'посёлок Пригородный', 'посёлок Пудость', 'посёлок Пушное',
           'посёлок Пчевжа', 'посёлок Рабитицы', 'посёлок Репино',
           'посёлок Романовка', 'посёлок Ромашки', 'посёлок Ропша',
           'посёлок Рябово', 'посёлок Сапёрное', 'посёлок Сапёрный',
           'посёлок Севастьяново', 'посёлок Селезнёво', 'посёлок Сельцо',
           'посёлок Семиозерье', 'посёлок Семрино', 'посёлок Серебрянский',
           'посёлок Совхозный', 'посёлок Сосново', 'посёлок Старая Малукса',
           'посёлок Стеклянный', 'посёлок Стрельна', 'посёлок Суйда',
           'посёлок Сумино', 'посёлок Суходолье', 'посёлок Тельмана',
           'посёлок Терволово', 'посёлок Торковичи', 'посёлок Торфяное',
           'посёлок Тёсово-4', 'посёлок Углово', 'посёлок Усть-Ижора',
           'посёлок Усть-Луга', 'посёлок Ушаки', 'посёлок Форт Красная Горка',
           'посёлок Цвелодубово', 'посёлок Цвылёво', 'посёлок Шугозеро',
           'посёлок Шушары', 'посёлок Щеглово',
           'посёлок городского типа Большая Ижора',
           'посёлок городского типа Важины',
           'посёлок городского типа Вознесенье',
           'посёлок городского типа Вырица',
           'посёлок городского типа Дружная Горка',
           'посёлок городского типа Дубровка',
           'посёлок городского типа Ефимовский',
           'посёлок городского типа Кондратьево',
           'посёлок городского типа Красный Бор',
           'посёлок городского типа Кузнечное',
           'посёлок городского типа Кузьмоловский',
           'посёлок городского типа Лебяжье',
           'посёлок городского типа Лесогорский',
           'посёлок городского типа Мга', 'посёлок городского типа Назия',
           'посёлок городского типа Никольский',
           'посёлок городского типа Павлово',
           'посёлок городского типа Приладожский',
           'посёлок городского типа Рахья', 'посёлок городского типа Рощино',
           'посёлок городского типа Рябово',
           'посёлок городского типа Сиверский',
           'посёлок городского типа Синявино',
           'посёлок городского типа Советский',
           'посёлок городского типа Тайцы', 'посёлок городского типа Токсово',
           'посёлок городского типа Ульяновка',
           'посёлок городского типа Форносово',
           'посёлок городского типа имени Морозова',
           'посёлок городского типа имени Свердлова',
           'посёлок при железнодорожной станции Вещево',
           'посёлок при железнодорожной станции Приветнинское',
           'посёлок станции Вещево', 'посёлок станции Громово',
           'посёлок станции Корнево', 'посёлок станции Лужайка',
           'посёлок станции Приветнинское', 'посёлок станции Свирь',
           'садоводческое некоммерческое товарищество Лесная Поляна',
           'садовое товарищество Новая Ропша',
           'садовое товарищество Приладожский', 'садовое товарищество Рахья',
           'садовое товарищество Садко', 'село Копорье', 'село Никольское',
           'село Павлово', 'село Паша', 'село Путилово', 'село Рождествено',
           'село Русско-Высоцкое', 'село Старая Ладога', 'село Шум', nan],
          dtype=object)



Также есть повторы в названиях населенных пунктов


```python
# через replace приведем к одному значению посёлок

data = data.replace({'locality_name':{'Никольское': 'село Никольское', 'городской посёлок Советский': 
                                      'посёлок городского типа Советский', 'городской посёлок Большая Ижора':
                                      'посёлок городского типа Большая Ижора', 'городской посёлок Лесогорский':
                                      'посёлок городского типа Лесогорский', 'посёлок Рябово':
                                      'посёлок городского типа Рябово', 'городской посёлок Мга':
                                      'посёлок городского типа Мга', 'городской посёлок Павлово': 
                                      'посёлок городского типа Павлово', 'городской посёлок Назия': 
                                      'посёлок городского типа Назия', 'коттеджный посёлок Лесное': 
                                      'посёлок Лесное', 'Мурино': 'посёлок Мурино', 'Любань': 
                                      'посёлок Любань', 'городской посёлок Рощино': 
                                      'посёлок городского типа Рощино', 'деревня Кудрово': 'Кудрово'}}
                   )
data['locality_name'].sort_values().unique()
```




    array(['Бокситогорск', 'Волосово', 'Волхов', 'Всеволожск', 'Выборг',
           'Высоцк', 'Гатчина', 'Зеленогорск', 'Ивангород', 'Каменногорск',
           'Кингисепп', 'Кириши', 'Кировск', 'Колпино', 'Коммунар',
           'Красное Село', 'Кронштадт', 'Кудрово', 'Лодейное Поле',
           'Ломоносов', 'Луга', 'Новая Ладога', 'Отрадное', 'Павловск',
           'Петергоф', 'Пикалёво', 'Подпорожье', 'Приморск', 'Приозерск',
           'Пушкин', 'Санкт-Петербург', 'Светогорск', 'Сертолово',
           'Сестрорецк', 'Сланцы', 'Сосновый Бор', 'Сясьстрой', 'Тихвин',
           'Тосно', 'Шлиссельбург', 'городской посёлок Будогощь',
           'городской посёлок Виллози', 'городской посёлок Новоселье',
           'городской посёлок Свирьстрой', 'городской посёлок Фёдоровское',
           'городской посёлок Янино-1', 'деревня Агалатово', 'деревня Аро',
           'деревня Батово', 'деревня Бегуницы', 'деревня Белогорка',
           'деревня Большая Вруда', 'деревня Большая Пустомержа',
           'деревня Большие Колпаны', 'деревня Большое Рейзино',
           'деревня Большой Сабск', 'деревня Бор', 'деревня Борисова Грива',
           'деревня Ваганово', 'деревня Вартемяги', 'деревня Вахнова Кара',
           'деревня Выскатка', 'деревня Гарболово', 'деревня Глинка',
           'деревня Горбунки', 'деревня Гостилицы', 'деревня Заклинье',
           'деревня Заневка', 'деревня Зимитицы', 'деревня Извара',
           'деревня Иссад', 'деревня Калитино', 'деревня Кальтино',
           'деревня Камышовка', 'деревня Каськово', 'деревня Келози',
           'деревня Кипень', 'деревня Кисельня', 'деревня Колтуши',
           'деревня Коркино', 'деревня Котлы', 'деревня Кривко',
           'деревня Кузьмолово', 'деревня Курковицы', 'деревня Куровицы',
           'деревня Куттузи', 'деревня Лаврики', 'деревня Лаголово',
           'деревня Лампово', 'деревня Лесколово', 'деревня Лопухинка',
           'деревня Лупполово', 'деревня Малая Романовка',
           'деревня Малое Верево', 'деревня Малое Карлино',
           'деревня Малые Колпаны', 'деревня Мануйлово', 'деревня Меньково',
           'деревня Мины', 'деревня Мистолово', 'деревня Ненимяки',
           'деревня Нижние Осельки', 'деревня Нижняя', 'деревня Низино',
           'деревня Новое Девяткино', 'деревня Новолисино', 'деревня Нурма',
           'деревня Оржицы', 'деревня Парицы', 'деревня Пельгора',
           'деревня Пеники', 'деревня Пижма', 'деревня Пикколово',
           'деревня Пудомяги', 'деревня Пустынка', 'деревня Пчева',
           'деревня Рабитицы', 'деревня Разбегаево', 'деревня Раздолье',
           'деревня Разметелево', 'деревня Рапполово', 'деревня Реброво',
           'деревня Русско', 'деревня Сижно', 'деревня Снегирёвка',
           'деревня Старая', 'деревня Старая Пустошь',
           'деревня Старое Хинколово', 'деревня Старополье',
           'деревня Старосиверская', 'деревня Старые Бегуницы',
           'деревня Суоранда', 'деревня Сяськелево', 'деревня Тарасово',
           'деревня Терпилицы', 'деревня Тихковицы', 'деревня Тойворово',
           'деревня Торосово', 'деревня Торошковичи', 'деревня Трубников Бор',
           'деревня Фалилеево', 'деревня Фёдоровское', 'деревня Хапо-Ое',
           'деревня Хязельки', 'деревня Чудской Бор', 'деревня Шпаньково',
           'деревня Щеглово', 'деревня Юкки', 'деревня Ялгино',
           'деревня Яльгелево', 'деревня Ям-Тесово',
           'коттеджный посёлок Кивеннапа Север', 'коттеджный посёлок Счастье',
           'посёлок Александровская', 'посёлок Алексеевка', 'посёлок Аннино',
           'посёлок Барышево', 'посёлок Белоостров', 'посёлок Бугры',
           'посёлок Возрождение', 'посёлок Войсковицы', 'посёлок Войскорово',
           'посёлок Володарское', 'посёлок Высокоключевой',
           'посёлок Гаврилово', 'посёлок Гарболово', 'посёлок Гладкое',
           'посёлок Глажево', 'посёлок Глебычево', 'посёлок Гончарово',
           'посёлок Громово', 'посёлок Дзержинского', 'посёлок Дружноселье',
           'посёлок Елизаветино', 'посёлок Жилгородок', 'посёлок Жилпосёлок',
           'посёлок Житково', 'посёлок Заводской', 'посёлок Запорожское',
           'посёлок Зимитицы', 'посёлок Ильичёво', 'посёлок Калитино',
           'посёлок Каложицы', 'посёлок Кикерино', 'посёлок Кингисеппский',
           'посёлок Кирпичное', 'посёлок Кобралово', 'посёлок Кобринское',
           'посёлок Коммунары', 'посёлок Коробицыно', 'посёлок Котельский',
           'посёлок Красная Долина', 'посёлок Красносельское',
           'посёлок Левашово', 'посёлок Ленинское', 'посёлок Лесное',
           'посёлок Лисий Нос', 'посёлок Лукаши', 'посёлок Любань',
           'посёлок Мельниково', 'посёлок Металлострой',
           'посёлок Мичуринское', 'посёлок Молодцово', 'посёлок Молодёжное',
           'посёлок Мурино', 'посёлок Мыза-Ивановка', 'посёлок Новогорелово',
           'посёлок Новый Свет', 'посёлок Новый Учхоз', 'посёлок Оредеж',
           'посёлок Пансионат Зелёный Бор', 'посёлок Парголово',
           'посёлок Первомайское', 'посёлок Перово', 'посёлок Песочный',
           'посёлок Петро-Славянка', 'посёлок Петровское',
           'посёлок Платформа 69-й километр', 'посёлок Плодовое',
           'посёлок Плоское', 'посёлок Победа', 'посёлок Поляны',
           'посёлок Понтонный', 'посёлок Почап', 'посёлок Починок',
           'посёлок Пригородный', 'посёлок Пудость', 'посёлок Пушное',
           'посёлок Пчевжа', 'посёлок Рабитицы', 'посёлок Репино',
           'посёлок Романовка', 'посёлок Ромашки', 'посёлок Ропша',
           'посёлок Сапёрное', 'посёлок Сапёрный', 'посёлок Севастьяново',
           'посёлок Селезнёво', 'посёлок Сельцо', 'посёлок Семиозерье',
           'посёлок Семрино', 'посёлок Серебрянский', 'посёлок Совхозный',
           'посёлок Сосново', 'посёлок Старая Малукса', 'посёлок Стеклянный',
           'посёлок Стрельна', 'посёлок Суйда', 'посёлок Сумино',
           'посёлок Суходолье', 'посёлок Тельмана', 'посёлок Терволово',
           'посёлок Торковичи', 'посёлок Торфяное', 'посёлок Тёсово-4',
           'посёлок Углово', 'посёлок Усть-Ижора', 'посёлок Усть-Луга',
           'посёлок Ушаки', 'посёлок Форт Красная Горка',
           'посёлок Цвелодубово', 'посёлок Цвылёво', 'посёлок Шугозеро',
           'посёлок Шушары', 'посёлок Щеглово',
           'посёлок городского типа Большая Ижора',
           'посёлок городского типа Важины',
           'посёлок городского типа Вознесенье',
           'посёлок городского типа Вырица',
           'посёлок городского типа Дружная Горка',
           'посёлок городского типа Дубровка',
           'посёлок городского типа Ефимовский',
           'посёлок городского типа Кондратьево',
           'посёлок городского типа Красный Бор',
           'посёлок городского типа Кузнечное',
           'посёлок городского типа Кузьмоловский',
           'посёлок городского типа Лебяжье',
           'посёлок городского типа Лесогорский',
           'посёлок городского типа Мга', 'посёлок городского типа Назия',
           'посёлок городского типа Никольский',
           'посёлок городского типа Павлово',
           'посёлок городского типа Приладожский',
           'посёлок городского типа Рахья', 'посёлок городского типа Рощино',
           'посёлок городского типа Рябово',
           'посёлок городского типа Сиверский',
           'посёлок городского типа Синявино',
           'посёлок городского типа Советский',
           'посёлок городского типа Тайцы', 'посёлок городского типа Токсово',
           'посёлок городского типа Ульяновка',
           'посёлок городского типа Форносово',
           'посёлок городского типа имени Морозова',
           'посёлок городского типа имени Свердлова',
           'посёлок при железнодорожной станции Вещево',
           'посёлок при железнодорожной станции Приветнинское',
           'посёлок станции Вещево', 'посёлок станции Громово',
           'посёлок станции Корнево', 'посёлок станции Лужайка',
           'посёлок станции Приветнинское', 'посёлок станции Свирь',
           'садоводческое некоммерческое товарищество Лесная Поляна',
           'садовое товарищество Новая Ропша',
           'садовое товарищество Приладожский', 'садовое товарищество Рахья',
           'садовое товарищество Садко', 'село Копорье', 'село Никольское',
           'село Павлово', 'село Паша', 'село Путилово', 'село Рождествено',
           'село Русско-Высоцкое', 'село Старая Ладога', 'село Шум', nan],
          dtype=object)




```python
# удалим строки без города, они будут мешать в анализе и даже пользователям не понятно где вообще эти квартиры находятся.

data = data.dropna(subset=['locality_name'])
```


```python
# проверим, что пропуски удалены.

print('\033[1m' + 'Количество пропусков в столбце "locality_name" :' + '\033[0m', data['locality_name'].isna().sum())
```

    [1mКоличество пропусков в столбце "locality_name" :[0m 49
    

#### Далее посморим на столбец с высотой потолков ceiling_height: минимальная высота потолков 1 метр, максимальная - 100 метров. 

Можно заметить, что встречаются также потолки высотой 20-30 метров. Что тоже аномалия. Логично предположить, что на самом деле это вещественные значения: 2-3 метра. Следовательно нужно поделить такие значения на 10.


```python
data.loc[data['ceiling_height'] >= 5, 'ceiling_height'].count()
```




    37




```python
len(data['ceiling_height'])

```




    23699




```python
# для значений больше 20 применим деление на 10

data.loc[data['ceiling_height'] >= 20, 'ceiling_height'] = data['ceiling_height'] / 10
```


```python
# проверим результат

data['ceiling_height'].describe().T
```




    count    23699.000000
    mean         2.698721
    std          0.253207
    min          1.000000
    25%          2.600000
    50%          2.650000
    75%          2.700000
    max         14.000000
    Name: ceiling_height, dtype: float64




```python
# посмотрим график для наглядности

data['ceiling_height'].sort_values().plot(y = 'ceiling_height', kind = 'hist', bins = 10, range=(2,5))
plt.show()
```


    
![png](output_61_0.png)
    



```python
# построим диаграмму размаха высоты потолков

data.boxplot(column='ceiling_height', figsize=(8, 6))
plt.title('Размах высоты потолков')
plt.ylim(1, 6)
plt.ylabel('высота, м')
plt.show()
```


    
![png](output_62_0.png)
    


*Из графика видно, значения менее 2,5м и более 2,8 метров - выбросы.*


```python
# оставим строки с высотой потолков от 2,5 до 5 метров

data = data.query('2.5 <= ceiling_height <= 5', engine='python')
```

**Посмотрим на столбец floors_total. Удалим строки с кол-вом этажей больше 30**


```python
# оставим строки с этажами < 30

data = data.query('floors_total < 30 or floors_total.isna()', engine='python')
```


```python
data['floors_total'].max()
```




    29.0



**Вывод:**

Сделал предобработку данных, а именно:

- изменил типы данных,
- привел имена столбцов к единому стилю,
- обработал явные и неявные дубликаты,
- также обработал пропуски.

##  Расчёты и добавление результатов в таблицу

### Произведем расчет данных и добавим их в таблицу для дальнейшего исследования:

1. **price_one_square_meter:** - цена одного квадратного метра;
2. **exposition_weekday:** - день недели публикации объявления (0 — понедельник, 1 — вторник и так далее);
3. **exposition_month:** - месяц публикации объявления;
4. **exposition_year:** - год публикации объявления;
5. **floor_category:** - тип этажа квартиры (значения — «первый», «последний», «другой»);
6. **city_centers_nearest_km:** - расстояние до центра города в километрах (переведем из м в км и округлим до целых 
      значений).

#### Добавим столбец price_one_square_meter


```python
# добавим столбец с ценой за 1м²

data['price_one_square_meter'] = data['last_price'] / data['total_area']

# округлим полученную цену до копеек

data['price_one_square_meter'] = data['price_one_square_meter'].round(2)
data.sample(7)
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>city_centers_nearest</th>
      <th>parks_around_3000</th>
      <th>parks_nearest</th>
      <th>ponds_around_3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
      <th>price_one_square_meter</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1212</th>
      <td>2</td>
      <td>8</td>
      <td>104.000000</td>
      <td>2016-11-07</td>
      <td>5</td>
      <td>3.40</td>
      <td>4.0</td>
      <td>67.000000</td>
      <td>2</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>10.0</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>25300.0</td>
      <td>5718.0</td>
      <td>2.0</td>
      <td>381.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>466.0</td>
      <td>0.08</td>
    </tr>
    <tr>
      <th>1445</th>
      <td>3</td>
      <td>4</td>
      <td>61.400002</td>
      <td>2019-02-07</td>
      <td>3</td>
      <td>2.58</td>
      <td>5.0</td>
      <td>43.599998</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>7.4</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>17492.0</td>
      <td>17697.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.07</td>
    </tr>
    <tr>
      <th>9399</th>
      <td>11</td>
      <td>7</td>
      <td>57.000000</td>
      <td>2019-03-08</td>
      <td>2</td>
      <td>2.56</td>
      <td>10.0</td>
      <td>30.000000</td>
      <td>7</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>9.0</td>
      <td>3</td>
      <td>Санкт-Петербург</td>
      <td>12896.0</td>
      <td>12430.0</td>
      <td>1.0</td>
      <td>719.0</td>
      <td>1.0</td>
      <td>26.0</td>
      <td>NaN</td>
      <td>0.12</td>
    </tr>
    <tr>
      <th>8264</th>
      <td>18</td>
      <td>15</td>
      <td>89.300003</td>
      <td>2018-10-19</td>
      <td>4</td>
      <td>2.95</td>
      <td>7.0</td>
      <td>63.099998</td>
      <td>2</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>10.0</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>25474.0</td>
      <td>4322.0</td>
      <td>1.0</td>
      <td>379.0</td>
      <td>3.0</td>
      <td>616.0</td>
      <td>NaN</td>
      <td>0.17</td>
    </tr>
    <tr>
      <th>23478</th>
      <td>4</td>
      <td>6</td>
      <td>39.299999</td>
      <td>2018-05-25</td>
      <td>1</td>
      <td>2.65</td>
      <td>14.0</td>
      <td>14.400000</td>
      <td>4</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>10.9</td>
      <td>2</td>
      <td>Санкт-Петербург</td>
      <td>19553.0</td>
      <td>4762.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>533.0</td>
      <td>147.0</td>
      <td>0.15</td>
    </tr>
    <tr>
      <th>14102</th>
      <td>2</td>
      <td>3</td>
      <td>33.500000</td>
      <td>2017-08-01</td>
      <td>1</td>
      <td>2.65</td>
      <td>25.0</td>
      <td>15.000000</td>
      <td>15</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>9.0</td>
      <td>0</td>
      <td>Кудрово</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>504.0</td>
      <td>0.09</td>
    </tr>
    <tr>
      <th>16154</th>
      <td>11</td>
      <td>10</td>
      <td>90.000000</td>
      <td>2018-02-01</td>
      <td>2</td>
      <td>2.90</td>
      <td>7.0</td>
      <td>60.900002</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>9.3</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>10360.0</td>
      <td>10297.0</td>
      <td>2.0</td>
      <td>320.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>112.0</td>
      <td>0.11</td>
    </tr>
  </tbody>
</table>
</div>



#### Добавим столбец exposition_weekday, exposition_month, exposition_year


```python
# добавим столбец с днем недели публикации объявления
data['exposition_weekday'] = data['first_day_exposition'].dt.weekday

# добавим столбец с месяцем публикации объявления
data['exposition_month'] = data['first_day_exposition'].dt.month

# добавим столбец с годом публикации объявления
data['exposition_year'] = data['first_day_exposition'].dt.year
data.tail()
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>city_centers_nearest</th>
      <th>parks_around_3000</th>
      <th>parks_nearest</th>
      <th>ponds_around_3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
      <th>price_one_square_meter</th>
      <th>exposition_weekday</th>
      <th>exposition_month</th>
      <th>exposition_year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>23694</th>
      <td>9</td>
      <td>9</td>
      <td>133.809998</td>
      <td>2017-03-21</td>
      <td>3</td>
      <td>3.70</td>
      <td>5.0</td>
      <td>73.300003</td>
      <td>3</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>13.830000</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>24665.0</td>
      <td>4232.0</td>
      <td>1.0</td>
      <td>796.0</td>
      <td>3.0</td>
      <td>381.0</td>
      <td>NaN</td>
      <td>0.07</td>
      <td>1</td>
      <td>3</td>
      <td>2017</td>
    </tr>
    <tr>
      <th>23695</th>
      <td>14</td>
      <td>3</td>
      <td>59.000000</td>
      <td>2018-01-15</td>
      <td>3</td>
      <td>2.65</td>
      <td>5.0</td>
      <td>38.000000</td>
      <td>4</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>8.500000</td>
      <td>0</td>
      <td>Тосно</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>45.0</td>
      <td>0.05</td>
      <td>0</td>
      <td>1</td>
      <td>2018</td>
    </tr>
    <tr>
      <th>23696</th>
      <td>18</td>
      <td>2</td>
      <td>56.700001</td>
      <td>2018-02-11</td>
      <td>2</td>
      <td>2.65</td>
      <td>3.0</td>
      <td>29.700001</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>0</td>
      <td>село Рождествено</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.04</td>
      <td>6</td>
      <td>2</td>
      <td>2018</td>
    </tr>
    <tr>
      <th>23697</th>
      <td>13</td>
      <td>11</td>
      <td>76.750000</td>
      <td>2017-03-28</td>
      <td>2</td>
      <td>3.00</td>
      <td>17.0</td>
      <td>NaN</td>
      <td>12</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>23.299999</td>
      <td>2</td>
      <td>Санкт-Петербург</td>
      <td>39140.0</td>
      <td>10364.0</td>
      <td>2.0</td>
      <td>173.0</td>
      <td>3.0</td>
      <td>196.0</td>
      <td>602.0</td>
      <td>0.14</td>
      <td>1</td>
      <td>3</td>
      <td>2017</td>
    </tr>
    <tr>
      <th>23698</th>
      <td>4</td>
      <td>1</td>
      <td>32.299999</td>
      <td>2017-07-21</td>
      <td>1</td>
      <td>2.50</td>
      <td>5.0</td>
      <td>12.300000</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>9.000000</td>
      <td>0</td>
      <td>посёлок Новый Учхоз</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.03</td>
      <td>4</td>
      <td>7</td>
      <td>2017</td>
    </tr>
  </tbody>
</table>
</div>



#### Добавим столбец с категоризацией по этажам floor_category


```python
# функция для категоризации этажности в доме

def get_floor_category(row):
    floor = row['floor']
    floors_total = row['floors_total']
    if floor == 1:
        return 'первый'
    elif floor == floors_total:
        return 'последний'
    else:
        return 'другой'
```


```python
# добавляем столбец с категорией этажа квартиры

data['floor_category'] = data.apply(get_floor_category, axis=1)
data.sample(3)
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>city_centers_nearest</th>
      <th>parks_around_3000</th>
      <th>parks_nearest</th>
      <th>ponds_around_3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
      <th>price_one_square_meter</th>
      <th>exposition_weekday</th>
      <th>exposition_month</th>
      <th>exposition_year</th>
      <th>floor_category</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9877</th>
      <td>19</td>
      <td>3</td>
      <td>41.700001</td>
      <td>2018-02-14</td>
      <td>1</td>
      <td>2.65</td>
      <td>23.0</td>
      <td>14.4</td>
      <td>16</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>9.10</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>22425.0</td>
      <td>24137.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>2.0</td>
      <td>398.0</td>
      <td>54.0</td>
      <td>0.07</td>
      <td>2</td>
      <td>2</td>
      <td>2018</td>
      <td>другой</td>
    </tr>
    <tr>
      <th>12271</th>
      <td>3</td>
      <td>6</td>
      <td>69.000000</td>
      <td>2018-08-08</td>
      <td>2</td>
      <td>2.65</td>
      <td>20.0</td>
      <td>55.0</td>
      <td>14</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>13.73</td>
      <td>0</td>
      <td>посёлок Мурино</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>133.0</td>
      <td>0.09</td>
      <td>2</td>
      <td>8</td>
      <td>2018</td>
      <td>другой</td>
    </tr>
    <tr>
      <th>5153</th>
      <td>9</td>
      <td>3</td>
      <td>47.799999</td>
      <td>2019-04-03</td>
      <td>2</td>
      <td>3.00</td>
      <td>5.0</td>
      <td>NaN</td>
      <td>2</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>13553.0</td>
      <td>9058.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>23.0</td>
      <td>0.06</td>
      <td>2</td>
      <td>4</td>
      <td>2019</td>
      <td>другой</td>
    </tr>
  </tbody>
</table>
</div>



#### Добавим столбец city_centers_nearest_km


```python
data['city_centers_nearest_km'] = round(data['city_centers_nearest'] / 1000)
data.head(4)
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>city_centers_nearest</th>
      <th>parks_around_3000</th>
      <th>parks_nearest</th>
      <th>ponds_around_3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
      <th>price_one_square_meter</th>
      <th>exposition_weekday</th>
      <th>exposition_month</th>
      <th>exposition_year</th>
      <th>floor_category</th>
      <th>city_centers_nearest_km</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20</td>
      <td>13</td>
      <td>108.000000</td>
      <td>2019-03-07</td>
      <td>3</td>
      <td>2.70</td>
      <td>16.0</td>
      <td>51.000000</td>
      <td>8</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>25.0</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>18863.0</td>
      <td>16028.0</td>
      <td>1.0</td>
      <td>482.0</td>
      <td>2.0</td>
      <td>755.0</td>
      <td>NaN</td>
      <td>0.12</td>
      <td>3</td>
      <td>3</td>
      <td>2019</td>
      <td>другой</td>
      <td>16.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>3</td>
      <td>40.400002</td>
      <td>2018-12-04</td>
      <td>1</td>
      <td>2.65</td>
      <td>11.0</td>
      <td>18.600000</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>11.0</td>
      <td>2</td>
      <td>посёлок Шушары</td>
      <td>12817.0</td>
      <td>18603.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>81.0</td>
      <td>0.07</td>
      <td>1</td>
      <td>12</td>
      <td>2018</td>
      <td>первый</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>10</td>
      <td>5</td>
      <td>56.000000</td>
      <td>2015-08-20</td>
      <td>2</td>
      <td>2.65</td>
      <td>5.0</td>
      <td>34.299999</td>
      <td>4</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>8.3</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>21741.0</td>
      <td>13933.0</td>
      <td>1.0</td>
      <td>90.0</td>
      <td>2.0</td>
      <td>574.0</td>
      <td>558.0</td>
      <td>0.09</td>
      <td>3</td>
      <td>8</td>
      <td>2015</td>
      <td>другой</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>64</td>
      <td>159.000000</td>
      <td>2015-07-24</td>
      <td>3</td>
      <td>2.65</td>
      <td>14.0</td>
      <td>NaN</td>
      <td>9</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>28098.0</td>
      <td>6800.0</td>
      <td>2.0</td>
      <td>84.0</td>
      <td>3.0</td>
      <td>234.0</td>
      <td>424.0</td>
      <td>0.40</td>
      <td>4</td>
      <td>7</td>
      <td>2015</td>
      <td>другой</td>
      <td>7.0</td>
    </tr>
  </tbody>
</table>
</div>



**Вывод:**

Добавил необходимые столбцы и произвел расчеты по ним. Отмечу, что из-за пропусков в исходных данных, в расчетных значениях также есть пропуски. В столбце floor_category для 85 строк категория этажа могла определиться неверно 
(вместо последний -> другой), т.к. значения количества этажей для этих объектов отсутствуют. Учитывая то, что доля возможных ошибок крайне мала, на результаты исследования они не повлияют.

## Проведение исследовательского анализа данных:

**Изучение параметров объектов недвижимости**

### Общая площадь


```python
# посмторим описательную часть для столбца 'total_area'

data['total_area'].describe().T
```




    count    23578.000000
    mean        60.346542
    std         35.572060
    min         12.000000
    25%         40.000000
    50%         52.000000
    75%         70.000000
    max        900.000000
    Name: total_area, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR чтобы построить график без выбросов
# первый квартиль Q1
q1 = data['total_area'].quantile(.25) 

# третий квартиль Q3
q3 = data['total_area'].quantile(.75)

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму площади
data['total_area'].hist(bins=30, range=((q1 - 1.5 * iqr), (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Общая площадь объектов недвижимости')
plt.xlabel('м²')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_86_0.png)
    


### Жилая площадь


```python
# посмторим описательную часть для столбца 'living_area' 

data['living_area'].describe()
```




    count    21684.000000
    mean        34.458401
    std         22.011629
    min          2.000000
    25%         18.600000
    50%         30.000000
    75%         42.299999
    max        409.700012
    Name: living_area, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR чтобы построить график без выбросов
# первый квартиль Q1
q1 = data['living_area'].quantile(.25)

 # третий квартиль Q3
q3 = data['living_area'].quantile(.75)

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму площади
data['living_area'].hist(bins=30, range=((q1 - 1.5 * iqr), (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Жилая площадь объектов недвижимости')
plt.xlabel('м²')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_89_0.png)
    


**Вывод:** 

Рассматриваемый диапазон, до примерно 78 м², исключая выбросы. Большая часть объектов недвижимости имеют жилую 
площадь от 15 до 35 м². Самый распространенный вариант - около 15 м². Жилая площадь объектов более 60 м² встречается редко. 
С площадью меньше 15 м² также редкость. Среднее значение - 34 м², медиана 30 м². У графика также наблюдается 
"хвост" из-за редких, но больших значений.

### Площадь кухни


```python
# посмторим описательную часть для столбца 'kitchen_area'

data['kitchen_area'].describe().T
```




    count    21315.000000
    mean        10.568190
    std          5.896854
    min          1.300000
    25%          7.000000
    50%          9.100000
    75%         12.000000
    max        112.000000
    Name: kitchen_area, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR чтобы построить график без выбросов
# первый квартиль Q1
q1 = data['kitchen_area'].quantile(.25) 

# третий квартиль Q3
q3 = data['kitchen_area'].quantile(.75) 

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму площади
data['kitchen_area'].hist(bins=30, range=((q1 - 1.5 * iqr), (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Площадь кухни объектов недвижимости')
plt.xlabel('м²')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_93_0.png)
    


**Вывод:** 

Рассматриваемый диапазон, до примерно 19 м², исключая выбросы. Большая часть объектов недвижимости имеют площадь кухни 
от 5,5 до 12 м². Самый распространенный вариант - около 5,5 м². Площадь кухни более 13 м² встречается редко. 
Площадь кухни менее 5 м² также редкость. Среднее значение - 10,5 м², медиана 9,1 м². У графика также наблюдается 
небольшой "хвост" из-за редких, но больших значений.

### Цена объекта


```python
# посмторим описательную часть для столбца 'last_price'

data['last_price'].describe().T
```




    count    23578.000000
    mean         6.044660
    std         10.857727
    min          0.000000
    25%          3.000000
    50%          4.000000
    75%          6.000000
    max        763.000000
    Name: last_price, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR чтобы построить график без выбросов
# первый квартиль Q1
q1 = data['last_price'].quantile(.25)

# третий квартиль Q3
q3 = data['last_price'].quantile(.75)

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму цены
data['last_price'].hist(bins=30, range=(0, (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Цена объекта недвижимости')
plt.xlabel('10 млн руб.')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_97_0.png)
    


**Вывод**

Рассматриваем диапазон, до примерно 12 млн руб., исключая выбросы. Большинство объектов недвижимости имеют цену в пределах от 3 до 5 млн. руб.. Самый распространенный вариант - около 3.5 млн.руб.. Вариантов с ценой более 10 млн немного. Среднее значение - 6,5 млн, медиана 4,6 млн. У графика также наблюдается небольшой "хвост" из-за редких, но больших значений.

### Количество комнат


```python
# посмторим описательную часть для столбца 'rooms'
data['rooms'].describe().T
```




    count    23578.000000
    mean         2.070956
    std          1.078783
    min          0.000000
    25%          1.000000
    50%          2.000000
    75%          3.000000
    max         19.000000
    Name: rooms, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR чтобы построить график без выбросов
# первый квартиль Q1
q1 = data['rooms'].quantile(.25) 

# третий квартиль Q3
q3 = data['rooms'].quantile(.75) 

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму кол-ва комнат
data['rooms'].hist(bins=5, range=(1, (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Количество комнат объекта недвижимости')
plt.xlabel('комнаты')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_101_0.png)
    


**Вывод:** 

Рассматриваемый диапазо, от 1 до 5 комнат, исключая некорректные значения (0 комнат) и выбросы. Большая часть объектов 
недвижимости имеют 1 или 2 комнаты, чуть меньше - 3 комнаты. Объектов, с кол-вом комнат 4-5 относительно немного.
Среднее и медиана 2 комнаты точны. Крайне редкие значения (от 6 до 19 комнат) не оказывают существенного влияния 
на среднее значение.

### Высота потолков


```python
# посмторим описательную часть для столбца 'ceiling_height'

data['ceiling_height'].describe().T
```




    count    23578.000000
    mean         2.697155
    std          0.215109
    min          2.500000
    25%          2.600000
    50%          2.650000
    75%          2.700000
    max          5.000000
    Name: ceiling_height, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR для построения графика без выбросов
# первый квартиль Q1
q1 = data['ceiling_height'].quantile(.25) 

# третий квартиль Q3
q3 = data['ceiling_height'].quantile(.75)

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму высоты потолков
data['ceiling_height'].hist(bins=10, range=((q1 - 1.5 * iqr), (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Высота потолков объектов недвижимости')
plt.xlabel('метры (м)')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_105_0.png)
    


**Вывод**

Рассматриваем диапазон от 2,5 до 2,85 м, исключая некорректные значения и выбросы. Большинство объектов недвижимости 
имеют высоту потолков 2,5 м и 2,65 м (большинство). Реже представлены варианты от 2,7м до 2,85 м. Среднее 2,7 м и медиана 
2,65 точны.

### Этаж квартиры


```python
# посмторим описательную часть для столбца 'floor'

data['floor'].describe().T
```




    count    23578.000000
    mean         5.881245
    std          4.861659
    min          1.000000
    25%          2.000000
    50%          4.000000
    75%          8.000000
    max         27.000000
    Name: floor, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR для построения графика без выбросов
# первый квартиль Q1
q1 = data['floor'].quantile(.25) 

# третий квартиль Q3
q3 = data['floor'].quantile(.75)

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму этажа квартиры
data['floor'].hist(bins=10, range=(1, (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Этаж объектов недвижимости')
plt.xlabel('этаж')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_109_0.png)
    


**Вывод**

Рассматриваемый диапазон с 1 по 17 этаж, исключая некорректные значения и выбросы. Большинство объектов недвижимости 
расположены с 1 по 4 этаж. Реже представлены варианты с 4 по 7. Среднее 5 этаж и медиана 4 этаж.

### Тип этажа квартиры («первый», «последний», «другой»)


```python
# напомним как мы обозначили столбец с категоризацией по типу квартиры

data.head()
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>city_centers_nearest</th>
      <th>parks_around_3000</th>
      <th>parks_nearest</th>
      <th>ponds_around_3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
      <th>price_one_square_meter</th>
      <th>exposition_weekday</th>
      <th>exposition_month</th>
      <th>exposition_year</th>
      <th>floor_category</th>
      <th>city_centers_nearest_km</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20</td>
      <td>13</td>
      <td>108.000000</td>
      <td>2019-03-07</td>
      <td>3</td>
      <td>2.70</td>
      <td>16.0</td>
      <td>51.000000</td>
      <td>8</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>25.0</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>18863.0</td>
      <td>16028.0</td>
      <td>1.0</td>
      <td>482.0</td>
      <td>2.0</td>
      <td>755.0</td>
      <td>NaN</td>
      <td>0.12</td>
      <td>3</td>
      <td>3</td>
      <td>2019</td>
      <td>другой</td>
      <td>16.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>3</td>
      <td>40.400002</td>
      <td>2018-12-04</td>
      <td>1</td>
      <td>2.65</td>
      <td>11.0</td>
      <td>18.600000</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>11.0</td>
      <td>2</td>
      <td>посёлок Шушары</td>
      <td>12817.0</td>
      <td>18603.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>81.0</td>
      <td>0.07</td>
      <td>1</td>
      <td>12</td>
      <td>2018</td>
      <td>первый</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>10</td>
      <td>5</td>
      <td>56.000000</td>
      <td>2015-08-20</td>
      <td>2</td>
      <td>2.65</td>
      <td>5.0</td>
      <td>34.299999</td>
      <td>4</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>8.3</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>21741.0</td>
      <td>13933.0</td>
      <td>1.0</td>
      <td>90.0</td>
      <td>2.0</td>
      <td>574.0</td>
      <td>558.0</td>
      <td>0.09</td>
      <td>3</td>
      <td>8</td>
      <td>2015</td>
      <td>другой</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>64</td>
      <td>159.000000</td>
      <td>2015-07-24</td>
      <td>3</td>
      <td>2.65</td>
      <td>14.0</td>
      <td>NaN</td>
      <td>9</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>28098.0</td>
      <td>6800.0</td>
      <td>2.0</td>
      <td>84.0</td>
      <td>3.0</td>
      <td>234.0</td>
      <td>424.0</td>
      <td>0.40</td>
      <td>4</td>
      <td>7</td>
      <td>2015</td>
      <td>другой</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>10</td>
      <td>100.000000</td>
      <td>2018-06-19</td>
      <td>2</td>
      <td>3.03</td>
      <td>14.0</td>
      <td>32.000000</td>
      <td>13</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>41.0</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>31856.0</td>
      <td>8098.0</td>
      <td>2.0</td>
      <td>112.0</td>
      <td>1.0</td>
      <td>48.0</td>
      <td>121.0</td>
      <td>0.10</td>
      <td>1</td>
      <td>6</td>
      <td>2018</td>
      <td>другой</td>
      <td>8.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# вызовем describe

data['floor_category'].describe().T
```




    count      23578
    unique         3
    top       другой
    freq       17363
    Name: floor_category, dtype: object




```python
# посмотрим на кол-во в каждой категории

data['floor_category'].value_counts()
```




    floor_category
    другой       17363
    последний     3313
    первый        2902
    Name: count, dtype: int64




```python
# отобразим это на графике

data['floor_category'].value_counts().plot.bar(figsize=(5, 3), ec='black', legend=True)
plt.show()
```


    
![png](output_115_0.png)
    


**Вывод** 

Видно, что объекты недвижимости, расположенные на первом и последним этажах имеют примерно одинаковые значения 
и их доля не столь велика. В основном объекты расположены на этажах между первым и последним.*

### Общее количество этажей в доме


```python
# выведем описательную статистику столбца 'floors_total'

data['floors_total'].describe()
```




    count    23492.000000
    mean        10.650945
    std          6.535243
    min          1.000000
    25%          5.000000
    50%          9.000000
    75%         16.000000
    max         29.000000
    Name: floors_total, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR для построения графика без выбросов
# первый квартиль Q1
q1 = data['floor'].quantile(.25) 

# третий квартиль Q3
q3 = data['floor'].quantile(.75) 

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму общего кол-ва этажей в доме
data['floors_total'].hist(bins=10, range=(1, (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Общее количество этажей в доме')
plt.xlabel('этаж')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_119_0.png)
    


**Вывод:**

Рассматриваемый диапазон с 1 по 17 этаж, исключая некорректные значения и выбросы. Большинство объектов недвижимости - это 
5-ти , 9-ти этажки. Остальные варианты представлены реже. Среднее 10 этаж и медиана 9 этаж.

### Расстояние до центра города в метрах


```python
# выведем описательную статистику столбца 'city_centers_nearest'

data['city_centers_nearest'].describe()
```




    count    18091.000000
    mean     14179.978516
    std       8608.557617
    min        181.000000
    25%       9234.000000
    50%      13090.000000
    75%      16280.000000
    max      65968.000000
    Name: city_centers_nearest, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR для построения графика без выбросов
# первый квартиль Q1
q1 = data['city_centers_nearest'].quantile(.25) 

# третий квартиль Q3
q3 = data['city_centers_nearest'].quantile(.75) 

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму этажа квартиры
data['city_centers_nearest'].hist(bins=20, range=((q1 - 1.5 * iqr), (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Расстояние до центра города в метрах')
plt.xlabel('м')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_123_0.png)
    


**Вывод**

Рассматриваемый диапазон с 3000 до 22000 м, исключая некорректные значения и выбросы. Большинство объектов недвижимости расположены на удалении 13-14 км от центра. Остальные варианты представлены реже. Среднее 13,9 км и медиана 13 км.

### Расстояние до ближайшего аэропорта


```python
# уберем значения равные 0 

data = data.query('airports_nearest != 0')
```


```python
# выведем описательную статистику для столбца 'airports_nearest'

data['airports_nearest'].describe()
```




    count    18067.000000
    mean     28816.652344
    std      12633.223633
    min       6450.000000
    25%      18575.500000
    50%      26765.000000
    75%      37310.000000
    max      84869.000000
    Name: airports_nearest, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR для построения графика без выбросов
# первый квартиль Q1
q1 = data['airports_nearest'].quantile(.25) 

# третий квартиль Q3
q3 = data['airports_nearest'].quantile(.75) 

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму этажа квартиры
data['airports_nearest'].hist(bins=15, range=(0, (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Расстояние до ближайшего аэропорта в метрах')
plt.xlabel('м')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_128_0.png)
    


**Вывод**

Рассматриваемый диапазон с 0 до 65000 м. Большинство объектов недвижимости расположены на удалении от аэропорта на расстоянии 15-25 км. Ближайший к аэропорту объект на расстоянии 6,5 км. Среднее 28,8 км и медиана 26,7 км.

### Расстояние до ближайшего парка в метрах


```python
data.head(3)
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>city_centers_nearest</th>
      <th>parks_around_3000</th>
      <th>parks_nearest</th>
      <th>ponds_around_3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
      <th>price_one_square_meter</th>
      <th>exposition_weekday</th>
      <th>exposition_month</th>
      <th>exposition_year</th>
      <th>floor_category</th>
      <th>city_centers_nearest_km</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20</td>
      <td>13</td>
      <td>108.000000</td>
      <td>2019-03-07</td>
      <td>3</td>
      <td>2.70</td>
      <td>16.0</td>
      <td>51.000000</td>
      <td>8</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>25.0</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>18863.0</td>
      <td>16028.0</td>
      <td>1.0</td>
      <td>482.0</td>
      <td>2.0</td>
      <td>755.0</td>
      <td>NaN</td>
      <td>0.12</td>
      <td>3</td>
      <td>3</td>
      <td>2019</td>
      <td>другой</td>
      <td>16.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7</td>
      <td>3</td>
      <td>40.400002</td>
      <td>2018-12-04</td>
      <td>1</td>
      <td>2.65</td>
      <td>11.0</td>
      <td>18.600000</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>11.0</td>
      <td>2</td>
      <td>посёлок Шушары</td>
      <td>12817.0</td>
      <td>18603.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>81.0</td>
      <td>0.07</td>
      <td>1</td>
      <td>12</td>
      <td>2018</td>
      <td>первый</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>10</td>
      <td>5</td>
      <td>56.000000</td>
      <td>2015-08-20</td>
      <td>2</td>
      <td>2.65</td>
      <td>5.0</td>
      <td>34.299999</td>
      <td>4</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>8.3</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>21741.0</td>
      <td>13933.0</td>
      <td>1.0</td>
      <td>90.0</td>
      <td>2.0</td>
      <td>574.0</td>
      <td>558.0</td>
      <td>0.09</td>
      <td>3</td>
      <td>8</td>
      <td>2015</td>
      <td>другой</td>
      <td>14.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# посмотрим описательную статистику столбуа 'parks_nearest'

data['parks_nearest'].describe().T
```




    count    8038.000000
    mean      490.860168
    std       342.944458
    min         1.000000
    25%       287.250000
    50%       454.000000
    75%       612.000000
    max      3190.000000
    Name: parks_nearest, dtype: float64




```python
# рассчитаем Q1, Q3 и IQR для построения графика без выбросов
# первый квартиль Q1
q1 = data['parks_nearest'].quantile(.25) 

# третий квартиль Q3
q3 = data['parks_nearest'].quantile(.75) 

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму этажа квартиры
data['parks_nearest'].hist(bins=15, range=(1, (q3 + 1.5 * iqr)), figsize=(10, 8), ec='black', legend=True)
plt.title('Расстояние до ближайшего парка в метрах')
plt.xlabel('м')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_133_0.png)
    


**Вывод**

Рассматриваемый диапазон с 0 до 1100 м. Большинство объектов недвижимости расположены на удалении от ближайшего парка на расстоянии 400-600м. Ближайшие к парку объект на расстоянии 500м. Среднее 490м и медиана 454м.

### День и месяц публикации объявления

День публикации объявления


```python
# посмотрим описательную статистику столбца 'exposition_weekday'

data['exposition_weekday'].describe().T
```




    count    23577.000000
    mean         2.569072
    std          1.788719
    min          0.000000
    25%          1.000000
    50%          3.000000
    75%          4.000000
    max          6.000000
    Name: exposition_weekday, dtype: float64




```python
# посмотрим кол-во объявлений по каждому дню недели

data['exposition_weekday'].value_counts().sort_values()
```




    exposition_weekday
    6    1685
    5    1933
    0    3591
    2    3956
    4    3978
    1    4165
    3    4269
    Name: count, dtype: int64




```python
# отобразим это на графике

data['exposition_weekday'].value_counts().plot.bar(figsize=(7, 5), ec='black', legend=True)
plt.show()
```


    
![png](output_139_0.png)
    


**Вывод**

По графику видно, что чаще всего объявления публиковали в будние дни в середине недели. Реже в выходные дни.

### Месяц публикации объявления


```python
# посмотрим описательную статистику столбца 'exposition_month'

data['exposition_month'].describe().T
```




    count    23577.000000
    mean         6.399203
    std          3.491742
    min          1.000000
    25%          3.000000
    50%          6.000000
    75%         10.000000
    max         12.000000
    Name: exposition_month, dtype: float64




```python
# посмотрим кол-во объявлений по каждому дню недели

data['exposition_month'].value_counts().sort_values()
```




    exposition_month
    5     1267
    1     1493
    12    1635
    7     1689
    8     1733
    6     1751
    9     1970
    10    2114
    11    2356
    4     2367
    3     2575
    2     2627
    Name: count, dtype: int64




```python
# отобразим это на графике

data['exposition_month'].value_counts().plot.bar(figsize=(7, 5), ec='black', legend=True)
plt.show()
```


    
![png](output_144_0.png)
    


**Промежуточный вывод**

По графику видно, что чаще всего объявления публиковали после январских праздников, в феврале. Наименьшие показатели в январе и мае. Можно предположить, что это из-за большого кол-ва выходных и праздничных дней.

**Вывод:**

Я получил представление о типичном объекте недвижимости из исходных данных: 

- квартира с 1 или 2 комнатами, 5-ти или 9-ти этажка (с квартирой с 1 по 4 этаж); 
- общей площадью около 45 м²; 
- площадью кухни около 5,5 м²; 
- с высотой потолков 2,6 м; 
- стоимостью около 3.5 млн. руб; 
- расположенной на удалении от центра на расстоянии 11000-16000 метров; 
- от аэропорта на расстоянии 15000-25000 м, до ближайшего парка около 500 метров.

### Изучим, как быстро продавались квартиры (столбец days_exposition)

Этот параметр показывает, сколько дней было размещено каждое объявление:
    
- Построим гистограмму.
- Посчитаем среднее и медиану.
- В ячейке типа markdown опишем, сколько времени обычно занимает продажа. Какие продажи можно считать быстрыми, 
  а какие — необычно долгими?

**Проанализируем время продажи квартиры**


```python
# рассчитаем Q1, Q3 и IQR для построения графика без выбросов

# первый квартиль Q1
q1 = data['days_exposition'].quantile(.25) 

# третий квартиль Q3
q3 = data['days_exposition'].quantile(.75) 

# межквартильный размах IQR
iqr = q3 - q1 

# построим гистограмму времени продажи квартиры
data['days_exposition'].hist(bins=100, range=(0, (q3 + 1.5 * iqr)), figsize=(7, 5), ec='black', legend=True)
plt.title('Время продажи квартиры')
plt.xlabel('дни')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_150_0.png)
    


**Вывод**

На графике видны пики около 50-60 дней, но при таком длинном "хвосте" из данных делать выводы не уместно. Изменим масштаб - изменим период до 100 дней.


```python
# ограничим гистограмму периодом до 100 дней

data['days_exposition'].hist(bins=100, range=(0, 100), figsize=(7, 5), ec='black', legend=True)
plt.title('Время продажи объекта квартиры')
plt.xlabel('дни')
plt.ylabel('объекты недвижимости')
plt.show()
```


    
![png](output_152_0.png)
    


**Вывод**

Судя по графику, чаще всего квартиры продают за 45 и 60 дней. Но тут важно учесть, что возможно квартира не продана, а просто закрылось объявление в связи с истекшим сроком публикации. Также объявление может остаться на сайте, даже если объект недвижимости уже фактически продан, просто забыли снять объявление. В этом случае если пользователь не потдвердит актуальность объявления, оно может быть автоматически удалено.

**Теперь посмотрим на среднее и медиану**


```python
# получим описательную статистику столбца days_exposition

data['days_exposition'].describe().T
```




    count    20416.000000
    mean       180.976242
    std        219.956726
    min          1.000000
    25%         45.000000
    50%         95.000000
    75%        232.000000
    max       1580.000000
    Name: days_exposition, dtype: float64



**Вывод**

Среднее время продажи объекта недвижимости 181 день, медианное - 95 дней. Максимальное значение - 1580 дней.* *Смотря на график, можно увидеть длиный "хвост". Больших значений достаточно много. Среднее значение в 2 раза больше медианного. Стандартное отклонение превышает среднее значение - это говорит о большом кол-ве выбросов. Чтобы посмотреть на всю эту красоту нужно построить диаграмму размаха.


```python
# потроим диаграмму размаха времени продажи объекта недвижимости

data.boxplot(column='days_exposition', figsize=(8, 6))
plt.title('Размах времени продажи объекта недвижимости')
plt.ylim(-100, 600)
plt.ylabel('дни')
plt.show()
```


    
![png](output_157_0.png)
    



```python
# все, что выше этого значения - это выбросы

print('\033[1m' + 'Значение отсекающее выбросы:' + '\033[0m', q3 + 1.5 * iqr)
```

    [1mЗначение отсекающее выбросы:[0m 512.5
    


```python
len(data)
```




    23577



**Обновим датафрейм без выбросов**


```python
# убираем выбросы

data_update = data.query('days_exposition < 510')

# проверим длину датафрейма

print('\033[1m' + 'Количество строк после удаления:' + '\033[0m', len(data_update))
```

    [1mКоличество строк после удаления:[0m 18737
    


```python
print('\033[1m' + 'Количество удаленных строк:' + '\033[0m', 23528-18694)
```

    [1mКоличество удаленных строк:[0m 4834
    

**Вывод**

Убрал из датафрейма 4834 строк, которые содержали выбросы по времени продажи объекта. 

Оценка времени продажи: 

- быстрая продажа - до 45 дней, 
- нормальная продажа - от 45 до 231 дней, 
- долгая продажа - от 231 до 510 дней. 

*Продажи после 510 дней - выбросы.*

### Проанализируем факторы влияющие на общую стоимость объекта

**Изучим зависимость цены от:**

- общей площади;
- жилой площади;
- площади кухни;
- количества комнат;
- этажа, на котором расположена квартира (первый, последний, другой);
- даты размещения (день недели, месяц, год).


```python
# визуализируем зависимость цены от общей площади

data.plot(x='total_area', y='last_price',\
                  style='.', title='Зависимость цены от общей площади',\
                  alpha=0.05, grid=True, sharex=False)
plt.show()
```


    
![png](output_166_0.png)
    



```python
# визуализируем зависимость цены от жилой площади

data.sort_values('total_area').plot(x='total_area', y='last_price',\
    style='-', title='Зависимость цены от общей площади')
plt.show()
```


    
![png](output_167_0.png)
    



```python
# визуализируем зависимость средней цены от жилой площади

data.pivot_table(index='total_area', values='last_price')\
.plot(style='-',title='Зависимость средней цены от общей площади', figsize=(10,4))
plt.show()
```


    
![png](output_168_0.png)
    


**Вывод**

Расчет корреляции показывает незначительную зависимость цены от жилой площади. На графике видна более четкая зависимость для площади от 10 до 70 кв.м. Остальные значения площади более подвержены разбросу по цене.*


```python
# визуализируем зависимость средней цены от площади кухни

data.pivot_table(index='kitchen_area', values='last_price')\
.plot(style='-',title='Зависимость средней цены от площади кухни', figsize=(10,4))
plt.show
print('Коэффициент корреляции цены от площади кухни', round(data['kitchen_area'].corr(data['last_price']), 2))
```

    Коэффициент корреляции цены от площади кухни 0.52
    


    
![png](output_170_1.png)
    



```python
# визуализируем зависимость цены от этажа

data.pivot_table(index='floor', values='last_price')\
.plot(style='-',title='Зависимость средней цены от этажа', figsize=(10,4))
plt.show
print('Коэффициент корреляции цены от этажа', round(data['floor'].corr(data['last_price']), 2))
```

    Коэффициент корреляции цены от этажа 0.03
    


    
![png](output_171_1.png)
    



```python
# визуализируем зависимость цены от количества комнат

data.pivot_table(index='rooms', values='last_price')\
.plot(style='-',title='Зависимость средней цены от количества комнат', figsize=(10,4))
plt.show
print('Коэффициент корреляции цены от количества комнат', round(data['rooms'].corr(data['last_price']), 2))
```

    Коэффициент корреляции цены от количества комнат 0.36
    


    
![png](output_172_1.png)
    


**Вывод**

Расчёт коэффициента коррекляции Пирсона показывает очень слабую зависимости цены от количества комнат. Хотя на графике ситуация выглядит по другому. Но мы принимает значения расчёта.


```python
data.pivot_table(index='floor_category', values='last_price', aggfunc='median')
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
      <th>last_price</th>
    </tr>
    <tr>
      <th>floor_category</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>другой</th>
      <td>4</td>
    </tr>
    <tr>
      <th>первый</th>
      <td>3</td>
    </tr>
    <tr>
      <th>последний</th>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
# для наглядности используем логарифмическую шкалу

data.pivot_table(index='floor_category', values='last_price', aggfunc=('median'))\
.plot(style='-',title='Зависимость средней цены от типа этажа', figsize=(10,4), kind='bar', logy=True)
plt.show()
```


    
![png](output_175_0.png)
    


**Вывод**

Анализ медианных значений показвает наиболее низкую стоимость первых этажей, а также снижение стоимости последних этажей по сравнению с остальными


```python
data.pivot_table(index='exposition_weekday', values='last_price')\
.plot(style='-',title='Зависимость средней цены от дня недели размещения объявления', figsize=(10,4))
plt.show
print('Коэффициент корреляции цены от дня недели размещения объявления', round(data['exposition_weekday'].corr(data['last_price']), 2))
```

    Коэффициент корреляции цены от дня недели размещения объявления 0.0
    


    
![png](output_177_1.png)
    


**Вывод**

Очевидно, что анализ показал полное отсутствие зависимости цены от дня недели*


```python
data.pivot_table(index='exposition_month', values='last_price')\
.plot(style='-',title='Зависимость средней цены от месяца размещения объявления', figsize=(10,4))
plt.show
print('Коэффициент корреляции цены от месяца размещения объявления', round(data['exposition_month'].corr(data['last_price']), 2))
```

    Коэффициент корреляции цены от месяца размещения объявления 0.0
    


    
![png](output_179_1.png)
    


**Вывод**

Коэффициент корреляции показывает отсутствие зависимости цены от месяца подачи объявления. Вместе с тем на графике 
зависимости прослеживается сезонность. Видны пики повышения стоимости в апреле, сентябре. В мае и октябре заметен спад цен.*


```python
data.pivot_table(index='exposition_year', values='last_price')\
.plot(style='-',title='Зависимость средней цены от года размещения объявления', figsize=(10,4))
plt.show
print('Коэффициент корреляции цены от года размещения объявления', round(data['exposition_year'].corr(data['last_price']), 2))
```

    Коэффициент корреляции цены от года размещения объявления -0.04
    


    
![png](output_181_1.png)
    



```python
data.pivot_table(index='exposition_year', values='price_one_square_meter')\
.plot(style='-',title='Зависимость средней цены кв.м от года размещения объявления', figsize=(10,4))
plt.show
print('Коэффициент корреляции цены  кв.м от года размещения объявления', round(data['exposition_year'].corr(data['price_one_square_meter']), 2))
```

    Коэффициент корреляции цены  кв.м от года размещения объявления 0.0
    


    
![png](output_182_1.png)
    



```python
data.pivot_table(index='exposition_year', values='total_area')\
.plot(style='-',title='Зависимость площади от года размещения объявления', figsize=(10,4))
plt.show
print('Коэффициент корреляции площади от года размещения объявления', round(data['exposition_year'].corr(data['total_area']), 2))
```

    Коэффициент корреляции площади от года размещения объявления -0.08
    


    
![png](output_183_1.png)
    


**Вывод**

Коэффициент корреляции показывает отсутствие зависимости цены от года подачи объявления. Отрицатеьлная динамика цен по годам скорее говорит о постепенной популяризации сервиса в сегменте низкой ценовой категории и в более мелких поселениях до 2017 года. После чего на графике отражается естественный рост цен.

### Расчитать среднюю цену одного квадратного метра в 10 населённых пунктах с наибольшим числом объявлений. 

Выделить населённые пункты с самой высокой и низкой стоимостью квадратного метра. 


```python
# ТОП 10 населенных пунктов с наибольшим числом объявлений

top_10_localities = data_update['locality_name'].value_counts().head(10)
top_10_localities
```




    locality_name
    Санкт-Петербург      12408
    посёлок Мурино         518
    Кудрово                406
    посёлок Шушары         388
    Всеволожск             308
    Колпино                293
    посёлок Парголово      287
    Пушкин                 276
    Гатчина                244
    Выборг                 191
    Name: count, dtype: int64




```python
# выведем среднюю цену за кв м по топ 10 населенным пунктам

top_10_localities_pivot = data_update.query('locality_name in @top_10_localities.index').pivot_table(index='locality_name', values='price_one_square_meter')
top_10_localities_pivot.sort_values(by='price_one_square_meter', ascending=False)
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
      <th>price_one_square_meter</th>
    </tr>
    <tr>
      <th>locality_name</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Санкт-Петербург</th>
      <td>0.102135</td>
    </tr>
    <tr>
      <th>Пушкин</th>
      <td>0.092391</td>
    </tr>
    <tr>
      <th>Кудрово</th>
      <td>0.082562</td>
    </tr>
    <tr>
      <th>посёлок Парголово</th>
      <td>0.078362</td>
    </tr>
    <tr>
      <th>посёлок Мурино</th>
      <td>0.073282</td>
    </tr>
    <tr>
      <th>посёлок Шушары</th>
      <td>0.068119</td>
    </tr>
    <tr>
      <th>Колпино</th>
      <td>0.064437</td>
    </tr>
    <tr>
      <th>Всеволожск</th>
      <td>0.058506</td>
    </tr>
    <tr>
      <th>Гатчина</th>
      <td>0.057172</td>
    </tr>
    <tr>
      <th>Выборг</th>
      <td>0.047068</td>
    </tr>
  </tbody>
</table>
</div>




```python
# отобразим на графике среднюю цену квадратного метра в топ 10 населенных пунктах

top_10_localities_pivot.sort_values(by='price_one_square_meter').plot(kind='barh', legend=True, grid=True, ec='black', figsize=(8, 6))
plt.title('Средняя цена за м²')
plt.xlabel('руб/м²')
plt.ylabel('')
plt.show()
```


    
![png](output_189_0.png)
    


**Вывод:**

Из графика видно, что наибольшая средняя цена за 1 квадратный метр в Санкт-Петербурге (111722 руб.), что логично. Следом по стоимости идет Пушкин (101894 руб.), что тоже логично - много исторических мест, парков и расположен к городу ближе, чем, например, Гатчина и Выборг. Наименьшая цена за квадратный метр в Выборге (57011 руб.).

Ранее я посчитал расстояние до центра в километрах. Теперь выделим квартиры в Санкт-Петербурге с помощью столбца locality_name и вычислим среднюю цену каждого километра. Опишим, как стоимость объектов зависит от расстояния до центра города.


```python
# выберем только Санкт-Петербург

df_spb = data_update.query('locality_name == "Санкт-Петербург"')
df_spb.head()
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
      <th>total_images</th>
      <th>last_price</th>
      <th>total_area</th>
      <th>first_day_exposition</th>
      <th>rooms</th>
      <th>ceiling_height</th>
      <th>floors_total</th>
      <th>living_area</th>
      <th>floor</th>
      <th>is_apartment</th>
      <th>studio</th>
      <th>open_plan</th>
      <th>kitchen_area</th>
      <th>balcony</th>
      <th>locality_name</th>
      <th>airports_nearest</th>
      <th>city_centers_nearest</th>
      <th>parks_around_3000</th>
      <th>parks_nearest</th>
      <th>ponds_around_3000</th>
      <th>ponds_nearest</th>
      <th>days_exposition</th>
      <th>price_one_square_meter</th>
      <th>exposition_weekday</th>
      <th>exposition_month</th>
      <th>exposition_year</th>
      <th>floor_category</th>
      <th>city_centers_nearest_km</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>0</td>
      <td>64</td>
      <td>159.000000</td>
      <td>2015-07-24</td>
      <td>3</td>
      <td>2.65</td>
      <td>14.0</td>
      <td>NaN</td>
      <td>9</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>NaN</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>28098.0</td>
      <td>6800.0</td>
      <td>2.0</td>
      <td>84.0</td>
      <td>3.0</td>
      <td>234.0</td>
      <td>424.0</td>
      <td>0.40</td>
      <td>4</td>
      <td>7</td>
      <td>2015</td>
      <td>другой</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>10</td>
      <td>100.000000</td>
      <td>2018-06-19</td>
      <td>2</td>
      <td>3.03</td>
      <td>14.0</td>
      <td>32.000000</td>
      <td>13</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>41.0</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>31856.0</td>
      <td>8098.0</td>
      <td>2.0</td>
      <td>112.0</td>
      <td>1.0</td>
      <td>48.0</td>
      <td>121.0</td>
      <td>0.10</td>
      <td>1</td>
      <td>6</td>
      <td>2018</td>
      <td>другой</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>18</td>
      <td>5</td>
      <td>61.000000</td>
      <td>2017-02-26</td>
      <td>3</td>
      <td>2.50</td>
      <td>9.0</td>
      <td>43.599998</td>
      <td>7</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>6.5</td>
      <td>2</td>
      <td>Санкт-Петербург</td>
      <td>50898.0</td>
      <td>15008.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>289.0</td>
      <td>0.08</td>
      <td>6</td>
      <td>2</td>
      <td>2017</td>
      <td>другой</td>
      <td>15.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>5</td>
      <td>5</td>
      <td>39.599998</td>
      <td>2017-11-16</td>
      <td>1</td>
      <td>2.67</td>
      <td>12.0</td>
      <td>20.299999</td>
      <td>3</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>8.5</td>
      <td>0</td>
      <td>Санкт-Петербург</td>
      <td>38357.0</td>
      <td>13878.0</td>
      <td>1.0</td>
      <td>310.0</td>
      <td>2.0</td>
      <td>553.0</td>
      <td>137.0</td>
      <td>0.13</td>
      <td>3</td>
      <td>11</td>
      <td>2017</td>
      <td>другой</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16</td>
      <td>4</td>
      <td>39.000000</td>
      <td>2017-11-18</td>
      <td>1</td>
      <td>2.65</td>
      <td>14.0</td>
      <td>20.500000</td>
      <td>5</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>7.6</td>
      <td>1</td>
      <td>Санкт-Петербург</td>
      <td>12900.0</td>
      <td>14259.0</td>
      <td>1.0</td>
      <td>590.0</td>
      <td>1.0</td>
      <td>296.0</td>
      <td>19.0</td>
      <td>0.10</td>
      <td>5</td>
      <td>11</td>
      <td>2017</td>
      <td>другой</td>
      <td>14.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# посмотрим длину получившегося df

len(df_spb)
```




    12408



**Вывод**

12466 объявлений из Санкт-Петербурга. Определим центр с помощью стоимости квадратного метра. Построим график. Та точка, после которой пойдет явный спад в стоимости и будем считать за границы центра города.


```python
# рассчитаем среднюю цену квадратного метра до центра

(
df_spb
    .pivot_table(index='city_centers_nearest_km', values='price_one_square_meter')
    .plot(marker='o', grid=True, figsize=(8, 6), legend=False)
)
plt.title('Средняя цена квадратного метра\nс шагом в 1 км до центра')
plt.xlabel('км')
plt.ylabel('руб./м²')
plt.show()
```


    
![png](output_194_0.png)
    


**Вывод**

Из графика можно заметить, что после 8-го километра форма графика становится линейной и стоимость начинается уменьшаться. Максимальная стоимость в зоне у самого центра (до 1 км). Пик в районе 27 км - возможен из-за класса жилья - элитное.

## Общий вывод

В ходе работы была проведена предобработка данных - устранены некоторые пропуски, некорректные значения. Оптимизированы 
названия населенных пунктов. Скорее всего, часть некорректных и пропущенных значений является ошибками ввода, 
часть - следствием невозможности обработать неполный адрес объекта.

В дальнейшем при сборе данных стоит попытаться контролировать получаемые значения - ограничить высоту потолка правдоподобными 6-ю метрами, не пропускать общую этажность дома, площадь кухни, жилую площадь.

Из полученного датасета можно сделать вывод, что в центре Петербурга квартиры дороже, чем на окраине или в городах-спутниках. Студии и однушки по цене квадратного метра являются лидерами, но при этом продаются быстрее всего. К тому же и количество их предложений самое большое.

**Наибольшее влияние на стоимость квартиры оказывает её площадь.** Чем больше площадь квартиры, тем выше её стоимость. Также на стоимость квартиры влияет и количество комнат. Чем больше комнат, тем выше стоимость. На стоимость квартиры также влияет расстояние до центра города. Чем ближе квартира располагается к центру, тем выше ее стоимость. По результатам исследования принял, что зона центра города распространяется на 8 км.

**Мы получили представление о типичном объекте недвижимости:** квартира с 1 или 2 комнатами, 5-ти или 9-ти этажка (с квартирой с 1 по 4 этаж), общей площадью около 45 м², площадью кухни около 5,5 м², с высотой потолков 2,6 м, стоимостью около 3.5 млн.руб, расположенной на удалении от центра на расстоянии 11-16 км, от аэропорта на расстоянии 15-25 км, до ближайшего парка около 500 метров.

**Также установлено:**

1. **Ожидаемое время продажи объекта недвижимости** - от 45 до 231 дня.
2. **Самая высокая средняя стоимость квадратного метра в Санкт-Петербурге** - 111 722 руб./м² (топ-10 населенных пунктов по количеству объявлений).
3. **Самая низкая средняя стоимость квадратного метра в Выборге** - 57 011 руб./м² (топ-10 населенных пунктов по количеству объявлений).

Сделаны графики соотношений цены к другим показателям квартир

- **Коэффициент корреляции цены от общей площади  = 0.68**
 *Чем больше площадь помещения, тем выше цена*
- **Коэффициент корреляции цены от жилой площади = 0.55**
 *Незначительная зависимость цены от жилой площади.*
- **Коэффициент корреляции цены от площади кухни = 0.54**
 *График и расчёт коррекляции показывают слабую зависимость цены от площади кухни*
- **Коэффициент корреляции цены от этажа = 0.09**
 *Расположение квартиры слаюо влияет на цену*
- **Коэффициент корреляции цены от количества комнат = 0.38**
 *Очень слабая зависимость цены от количества комнат*
- **Коэффициент корреляции цены от дня недели размещения объявления = -0.02**
 *Очевидно, что анализ показал полное отсутствие зависимости цены от дня недели.*
- **Коэффициент корреляции цены от месяца размещения объявления = 0.0**
 *Коэффициент корреляции показывает отсутствие зависимости цены от месяца подачи объявления. Вместе с тем на графике зависимости прослеживается сезонность. Видны пики повышения стоимости в апреле, сентябре. В мае и октябре заметен спад цен..*
- **Коэффициент корреляции цены от года размещения объявления = -0.01**
 *В 2016, 2017 и 2018 году цены на квартиры были гораздо ниже, чем в 2015 или в 2019 году. Корреляция не обнаружена между показателями "цена" и "год". Нет линейной зависимости.*
