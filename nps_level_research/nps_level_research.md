# Исследование опроса клиентов телекомунникацонной компании

**Описание проекта**

Заказчик данного исследования — большая телекоммуникационная компания, которая оказывает услуги на территории всего СНГ. Перед компанией стоит задача определить текущий уровень потребительской лояльности, или NPS (от англ. Net Promoter Score), среди клиентов из России.

Компания провела опрос и попросила вас подготовить дашборд с его итогами. Большую базу данных для такой задачи разворачивать не стали и выгрузили данные в SQLite.

Чтобы оценить результаты опроса, оценки обычно делят на три группы:

- **9-10 баллов** — «cторонники» (англ. promoters);
- **7-8 баллов** — «нейтралы» (англ. passives);
- **0-6 баллов** — «критики» (англ. detractors).

Итоговое значение NPS рассчитывается по формуле: % «сторонников» - % «критиков».

**Цель проекта**

Изучить предоставленные данные и ответить на следующие вопросы. Как распределены участники опроса по возрасту, полу и возрасту? Каких пользователей больше: новых или старых? Пользователи из каких городов активнее участвовали в опросе?

- Какие группы пользователей наиболее лояльны к сервису? Какие менее?

- Какой общий NPS среди всех опрошенных?

- Как можно описать клиентов, которые относятся к группе cторонников (англ. promoters)?

### Загрузка данных


```python
import os
import pandas as pd
from sqlalchemy import create_engine

# путь к БД на вашем компьютере (например, в той же папке, что и тетрадь)
path_to_db_local ='F:/Обучение/Обучение програмированию/telecomm_csi.db'
# путь к БД на платформе
path_to_db_platform = '/datasets/telecomm_csi.db'
# итоговый путь к БД
path_to_db = None

# если путь на вашем компьютере ведёт к БД, то он становится итоговым
if os.path.exists(path_to_db_local):
    path_to_db = path_to_db_local
# иначе: если путь на платформе ведёт к БД, то он становится итоговым
elif os.path.exists(path_to_db_platform):
    path_to_db = path_to_db_platform
# иначе выводится сообщение о том, что файл не найден
else:
    raise Exception('Файл с базой данных SQLite не найден!')

# если итоговый путь не пустой
if path_to_db:
    # то создаём подключение к базе
    engine = create_engine(f'sqlite:///{path_to_db}', echo=False)
    
    # пример запроса
    query = """
SELECT u.user_id,
       u.lt_day,
       CASE 
           WHEN u.lt_day <= 365 THEN 'Новый'
           ELSE 'Старый'
           END AS is_new,
       u.age,
       CASE 
           WHEN u.gender_segment == 1 THEN 'Женщина'
           WHEN u.gender_segment == 0 THEN 'Мужчина'
           ELSE 'z'
           END AS gender_segment,
       u.os_name,
       u.cpe_type_name,
       location.country,
       location.city,
       SUBSTR(age_segment.title, 4) AS age_segment,
       SUBSTR(traffic_segment.title, 4) AS traffic_segment,
       SUBSTR(lifetime_segment.title, 4) AS lifetime_segment,
       u.nps_score,
       CASE 
           WHEN u.nps_score >= 9 THEN 'Cторонник'
           WHEN u.nps_score >= 7 THEN 'Нейтрал'
           ELSE 'Критик'
           END AS nps_group
FROM user AS u
JOIN location ON u.location_id = location.location_id
JOIN age_segment ON u.age_gr_id = age_segment.age_gr_id
JOIN traffic_segment ON u.tr_gr_id = traffic_segment.tr_gr_id
JOIN lifetime_segment ON u.lt_gr_id = lifetime_segment.lt_gr_id;
"""
    
    # создаём датафрейм по данным запроса
    df = pd.read_sql(query, engine) 
```


```python
df.sample(10)
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
      <th>user_id</th>
      <th>lt_day</th>
      <th>is_new</th>
      <th>age</th>
      <th>gender_segment</th>
      <th>os_name</th>
      <th>cpe_type_name</th>
      <th>country</th>
      <th>city</th>
      <th>age_segment</th>
      <th>traffic_segment</th>
      <th>lifetime_segment</th>
      <th>nps_score</th>
      <th>nps_group</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>377010</th>
      <td>TI6O84</td>
      <td>886</td>
      <td>Старый</td>
      <td>43.0</td>
      <td>Женщина</td>
      <td>IOS</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Екатеринбург</td>
      <td>35-44</td>
      <td>1-5</td>
      <td>25-36</td>
      <td>10</td>
      <td>Cторонник</td>
    </tr>
    <tr>
      <th>191345</th>
      <td>JVYPF5</td>
      <td>1078</td>
      <td>Старый</td>
      <td>24.0</td>
      <td>Мужчина</td>
      <td>PROPRIETARY</td>
      <td>PHONE</td>
      <td>Россия</td>
      <td>Рязань</td>
      <td>16-24</td>
      <td>10-15</td>
      <td>25-36</td>
      <td>9</td>
      <td>Cторонник</td>
    </tr>
    <tr>
      <th>388233</th>
      <td>U397G0</td>
      <td>674</td>
      <td>Старый</td>
      <td>40.0</td>
      <td>Женщина</td>
      <td>ANDROID</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Ижевск</td>
      <td>35-44</td>
      <td>10-15</td>
      <td>13-24</td>
      <td>10</td>
      <td>Cторонник</td>
    </tr>
    <tr>
      <th>234679</th>
      <td>M4TS6D</td>
      <td>3575</td>
      <td>Старый</td>
      <td>59.0</td>
      <td>Женщина</td>
      <td>ANDROID</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Новосибирск</td>
      <td>55-64</td>
      <td>5-10</td>
      <td>36+</td>
      <td>10</td>
      <td>Cторонник</td>
    </tr>
    <tr>
      <th>357292</th>
      <td>SHDQFT</td>
      <td>446</td>
      <td>Старый</td>
      <td>34.0</td>
      <td>Женщина</td>
      <td>ANDROID</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Курск</td>
      <td>25-34</td>
      <td>20-25</td>
      <td>13-24</td>
      <td>5</td>
      <td>Критик</td>
    </tr>
    <tr>
      <th>106704</th>
      <td>FHSSUB</td>
      <td>191</td>
      <td>Новый</td>
      <td>38.0</td>
      <td>Женщина</td>
      <td>ANDROID</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Тула</td>
      <td>35-44</td>
      <td>10-15</td>
      <td>7-12</td>
      <td>10</td>
      <td>Cторонник</td>
    </tr>
    <tr>
      <th>486950</th>
      <td>Z6SR7M</td>
      <td>2866</td>
      <td>Старый</td>
      <td>42.0</td>
      <td>Женщина</td>
      <td>ANDROID</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Иркутск</td>
      <td>35-44</td>
      <td>0.1-1</td>
      <td>36+</td>
      <td>8</td>
      <td>Нейтрал</td>
    </tr>
    <tr>
      <th>287967</th>
      <td>OW9OHH</td>
      <td>795</td>
      <td>Старый</td>
      <td>35.0</td>
      <td>Мужчина</td>
      <td>ANDROID</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Москва</td>
      <td>35-44</td>
      <td>5-10</td>
      <td>25-36</td>
      <td>5</td>
      <td>Критик</td>
    </tr>
    <tr>
      <th>48776</th>
      <td>CIOX5Z</td>
      <td>178</td>
      <td>Новый</td>
      <td>30.0</td>
      <td>Мужчина</td>
      <td>IOS</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Новосибирск</td>
      <td>25-34</td>
      <td>30-35</td>
      <td>4-6</td>
      <td>5</td>
      <td>Критик</td>
    </tr>
    <tr>
      <th>267444</th>
      <td>NU34D4</td>
      <td>525</td>
      <td>Старый</td>
      <td>63.0</td>
      <td>Мужчина</td>
      <td>ANDROID</td>
      <td>SMARTPHONE</td>
      <td>Россия</td>
      <td>Красноярск</td>
      <td>55-64</td>
      <td>55-60</td>
      <td>13-24</td>
      <td>10</td>
      <td>Cторонник</td>
    </tr>
  </tbody>
</table>
</div>



### Описание данных

- **user_id** — идентификатор клиента 
- **lt_day** — количество дней «жизни» клиента 
- **is_new** — поле хранит информацию о том, является ли клиент новым 
- **age** — возраст gender_segment — пол os_name — тип операционной системы 
- **cpe_type_name** — тип устройства 
- **country** — страна проживания 
- **city** — город проживания 
- **age_segment** — возрастной сегмент 
- **traffic_segment** — сегмент по объёму потребляемого трафика 
- **lifetime_segment** — сегмент по количеству дней «жизни» nps_score — оценка клиента в NPS-опросе 
- **nps_group** — поле хранит информацию о том, к какой группе относится оценка клиента в опросе


```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 502493 entries, 0 to 502492
    Data columns (total 14 columns):
     #   Column            Non-Null Count   Dtype  
    ---  ------            --------------   -----  
     0   user_id           502493 non-null  object 
     1   lt_day            502493 non-null  int64  
     2   is_new            502493 non-null  object 
     3   age               501939 non-null  float64
     4   gender_segment    502493 non-null  object 
     5   os_name           502493 non-null  object 
     6   cpe_type_name     502493 non-null  object 
     7   country           502493 non-null  object 
     8   city              502493 non-null  object 
     9   age_segment       502493 non-null  object 
     10  traffic_segment   502493 non-null  object 
     11  lifetime_segment  502493 non-null  object 
     12  nps_score         502493 non-null  int64  
     13  nps_group         502493 non-null  object 
    dtypes: float64(1), int64(2), object(11)
    memory usage: 53.7+ MB
    

### Сохранение данных 


```python
df.to_csv('telecomm_csi_tableau.csv', index=False)
```

### Дашборд исследования NPS

[Ссылка на исследование уровня потребительской лояльности (уровень NPS) ver. 1.1.](https://public.tableau.com/app/profile/andrey.manannikov/viz/NPSManannikovA_A_/Story1?publish=yes)

### Исседование NPS в PDF формате 

[Ссылка на исселедования уровня потребительской лояльности (уровень NPS) ver. 1.1.](https://disk.yandex.ru/d/sBA5ThMDUa8LQg)
