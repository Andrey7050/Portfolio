<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Загрузка-данных-и-изучение-общей-информации" data-toc-modified-id="Загрузка-данных-и-изучение-общей-информации-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Загрузка данных и изучение общей информации</a></span></li><li><span><a href="#Предобработка-данных" data-toc-modified-id="Предобработка-данных-2"><span class="toc-item-num">2&nbsp;&nbsp;</span>Предобработка данных</a></span><ul class="toc-item"><li><span><a href="#Удаление-пропусков" data-toc-modified-id="Удаление-пропусков-2.1"><span class="toc-item-num">2.1&nbsp;&nbsp;</span>Удаление пропусков</a></span></li><li><span><a href="#Обработка-аномальных-значений" data-toc-modified-id="Обработка-аномальных-значений-2.2"><span class="toc-item-num">2.2&nbsp;&nbsp;</span>Обработка аномальных значений</a></span></li><li><span><a href="#Заменим-вещественный-тип-данных-в-столбце-total_income-на-целочисленный-с-помощью-метода-astype()." data-toc-modified-id="Заменим-вещественный-тип-данных-в-столбце-total_income-на-целочисленный-с-помощью-метода-astype().-2.3"><span class="toc-item-num">2.3&nbsp;&nbsp;</span>Заменим вещественный тип данных в столбце total_income на целочисленный с помощью метода astype().</a></span></li><li><span><a href="#Обработка-дубликатов" data-toc-modified-id="Обработка-дубликатов-2.4"><span class="toc-item-num">2.4&nbsp;&nbsp;</span>Обработка дубликатов</a></span></li><li><span><a href="#Категоризация-данных" data-toc-modified-id="Категоризация-данных-2.5"><span class="toc-item-num">2.5&nbsp;&nbsp;</span>Категоризация данных</a></span></li></ul></li><li><span><a href="#Исследование-данных" data-toc-modified-id="Исследование-данных-3"><span class="toc-item-num">3&nbsp;&nbsp;</span>Исследование данных</a></span><ul class="toc-item"><li><span><a href="#Есть-ли-зависимость-между-количеством-детей-и-возвратом-кредита-в-срок?" data-toc-modified-id="Есть-ли-зависимость-между-количеством-детей-и-возвратом-кредита-в-срок?-3.1"><span class="toc-item-num">3.1&nbsp;&nbsp;</span>Есть ли зависимость между количеством детей и возвратом кредита в срок?</a></span></li><li><span><a href="#Есть-ли-зависимость-между-семейным-положением-и-возвратом-кредита-в-срок?" data-toc-modified-id="Есть-ли-зависимость-между-семейным-положением-и-возвратом-кредита-в-срок?-3.2"><span class="toc-item-num">3.2&nbsp;&nbsp;</span>Есть ли зависимость между семейным положением и возвратом кредита в срок?</a></span></li><li><span><a href="#Есть-ли-зависимость-между-уровнем-дохода-и-возвратом-кредита-в-срок?" data-toc-modified-id="Есть-ли-зависимость-между-уровнем-дохода-и-возвратом-кредита-в-срок?-3.3"><span class="toc-item-num">3.3&nbsp;&nbsp;</span>Есть ли зависимость между уровнем дохода и возвратом кредита в срок?</a></span></li><li><span><a href="#Как-разные-цели-кредита-влияют-на-его-возврат-в-срок?" data-toc-modified-id="Как-разные-цели-кредита-влияют-на-его-возврат-в-срок?-3.4"><span class="toc-item-num">3.4&nbsp;&nbsp;</span>Как разные цели кредита влияют на его возврат в срок?</a></span></li></ul></li><li><span><a href="#Приведите-возможные-причины-появления-пропусков-в-исходных-данных" data-toc-modified-id="Приведите-возможные-причины-появления-пропусков-в-исходных-данных-4"><span class="toc-item-num">4&nbsp;&nbsp;</span>Приведите возможные причины появления пропусков в исходных данных</a></span><ul class="toc-item"><li><span><a href="#Объясните,-почему-заполнить-пропуски-медианным-значением-—-лучшее-решение-для-количественных-переменных" data-toc-modified-id="Объясните,-почему-заполнить-пропуски-медианным-значением-—-лучшее-решение-для-количественных-переменных-4.1"><span class="toc-item-num">4.1&nbsp;&nbsp;</span>Объясните, почему заполнить пропуски медианным значением — лучшее решение для количественных переменных</a></span></li></ul></li><li><span><a href="#Общий-вывод" data-toc-modified-id="Общий-вывод-5"><span class="toc-item-num">5&nbsp;&nbsp;</span>Общий вывод</a></span></li></ul></div>

**Исследование надежности заемщиков**

**Описание проекта**

На основе данных кредитного отдела банка исследовал влияние семейного положения и количества детей на факт погашения кредита в срок. Была получена информация о данных. Определены и обработаны пропуски. Заменены типы данных на соответствующие хранящимся данным. Удалены дубликаты. Выделены леммы в значениях столбца и категоризированны данные.

**Задача проекта**

На основе статистики о платёжеспособности клиентов исследовать влияние семейное положение и количества детей клиента на факт возврата кредита в указанный срок.

**Описание данных**

- **children** — количество детей в семье
- **days_employed** — общий трудовой стаж в днях
- **dob_years** — возраст клиента в годах
- **education** — уровень образования клиента
- **education_id** — идентификатор уровня образования
- **family_status** — семейное положение
- **family_status_id** — идентификатор семейного положения
- **gender** — пол клиента
- **income_type** — тип занятости
- **debt** — имел ли задолженность по возврату кредитов
- **total_income** — ежемесячный доход
- **purpose** — цель получения кредита

**План выполнения проекта**

**Шаг 1.** Загрузить исходные данные и изучить общую информацию

**Шаг 2.** Выполнить предобработку данных
- изучить и обработать пропуски данных;
- выявить и изучить аномалии в первоночальных данных;
- изучить и при необходимости изменить типы данных;
- обнаружить и обработать явные и неявные дубликаты. 

**Шаг 3.** Свормировать дополнительные столбцы для удобства анализа данных

**Шаг 4.** Ответить на поставленные вопросы исследования 

**Шаг 5.** Подготовить вывод и рекомендации на основании полученных данных

## Загрузка данных и изучение общей информации


```python
# импортируем библиотеку pandas

import pandas as pd
```


```python
# причитаем данные из csv-файла в датафрейм и сохраним в переменную data

data = pd.read_csv('F:/Work projects/bank_data_project.csv') 
```


```python
# просмотрим первые 20 строчек датафрейма data на экране

data.head(20)
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
      <th>children</th>
      <th>days_employed</th>
      <th>dob_years</th>
      <th>education</th>
      <th>education_id</th>
      <th>family_status</th>
      <th>family_status_id</th>
      <th>gender</th>
      <th>income_type</th>
      <th>debt</th>
      <th>total_income</th>
      <th>purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>-8437.673028</td>
      <td>42</td>
      <td>высшее</td>
      <td>0</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>253875.639453</td>
      <td>покупка жилья</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>-4024.803754</td>
      <td>36</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>112080.014102</td>
      <td>приобретение автомобиля</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0</td>
      <td>-5623.422610</td>
      <td>33</td>
      <td>Среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>M</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>145885.952297</td>
      <td>покупка жилья</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>-4124.747207</td>
      <td>32</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>M</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>267628.550329</td>
      <td>дополнительное образование</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0</td>
      <td>340266.072047</td>
      <td>53</td>
      <td>среднее</td>
      <td>1</td>
      <td>гражданский брак</td>
      <td>1</td>
      <td>F</td>
      <td>пенсионер</td>
      <td>0</td>
      <td>158616.077870</td>
      <td>сыграть свадьбу</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>-926.185831</td>
      <td>27</td>
      <td>высшее</td>
      <td>0</td>
      <td>гражданский брак</td>
      <td>1</td>
      <td>M</td>
      <td>компаньон</td>
      <td>0</td>
      <td>255763.565419</td>
      <td>покупка жилья</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0</td>
      <td>-2879.202052</td>
      <td>43</td>
      <td>высшее</td>
      <td>0</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>компаньон</td>
      <td>0</td>
      <td>240525.971920</td>
      <td>операции с жильем</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0</td>
      <td>-152.779569</td>
      <td>50</td>
      <td>СРЕДНЕЕ</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>M</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>135823.934197</td>
      <td>образование</td>
    </tr>
    <tr>
      <th>8</th>
      <td>2</td>
      <td>-6929.865299</td>
      <td>35</td>
      <td>ВЫСШЕЕ</td>
      <td>0</td>
      <td>гражданский брак</td>
      <td>1</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>95856.832424</td>
      <td>на проведение свадьбы</td>
    </tr>
    <tr>
      <th>9</th>
      <td>0</td>
      <td>-2188.756445</td>
      <td>41</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>M</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>144425.938277</td>
      <td>покупка жилья для семьи</td>
    </tr>
    <tr>
      <th>10</th>
      <td>2</td>
      <td>-4171.483647</td>
      <td>36</td>
      <td>высшее</td>
      <td>0</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>M</td>
      <td>компаньон</td>
      <td>0</td>
      <td>113943.491460</td>
      <td>покупка недвижимости</td>
    </tr>
    <tr>
      <th>11</th>
      <td>0</td>
      <td>-792.701887</td>
      <td>40</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>77069.234271</td>
      <td>покупка коммерческой недвижимости</td>
    </tr>
    <tr>
      <th>12</th>
      <td>0</td>
      <td>NaN</td>
      <td>65</td>
      <td>среднее</td>
      <td>1</td>
      <td>гражданский брак</td>
      <td>1</td>
      <td>M</td>
      <td>пенсионер</td>
      <td>0</td>
      <td>NaN</td>
      <td>сыграть свадьбу</td>
    </tr>
    <tr>
      <th>13</th>
      <td>0</td>
      <td>-1846.641941</td>
      <td>54</td>
      <td>неоконченное высшее</td>
      <td>2</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>130458.228857</td>
      <td>приобретение автомобиля</td>
    </tr>
    <tr>
      <th>14</th>
      <td>0</td>
      <td>-1844.956182</td>
      <td>56</td>
      <td>высшее</td>
      <td>0</td>
      <td>гражданский брак</td>
      <td>1</td>
      <td>F</td>
      <td>компаньон</td>
      <td>1</td>
      <td>165127.911772</td>
      <td>покупка жилой недвижимости</td>
    </tr>
    <tr>
      <th>15</th>
      <td>1</td>
      <td>-972.364419</td>
      <td>26</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>116820.904450</td>
      <td>строительство собственной недвижимости</td>
    </tr>
    <tr>
      <th>16</th>
      <td>0</td>
      <td>-1719.934226</td>
      <td>35</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>289202.704229</td>
      <td>недвижимость</td>
    </tr>
    <tr>
      <th>17</th>
      <td>0</td>
      <td>-2369.999720</td>
      <td>33</td>
      <td>высшее</td>
      <td>0</td>
      <td>гражданский брак</td>
      <td>1</td>
      <td>M</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>90410.586745</td>
      <td>строительство недвижимости</td>
    </tr>
    <tr>
      <th>18</th>
      <td>0</td>
      <td>400281.136913</td>
      <td>53</td>
      <td>среднее</td>
      <td>1</td>
      <td>вдовец / вдова</td>
      <td>2</td>
      <td>F</td>
      <td>пенсионер</td>
      <td>0</td>
      <td>56823.777243</td>
      <td>на покупку подержанного автомобиля</td>
    </tr>
    <tr>
      <th>19</th>
      <td>0</td>
      <td>-10038.818549</td>
      <td>48</td>
      <td>СРЕДНЕЕ</td>
      <td>1</td>
      <td>в разводе</td>
      <td>3</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>242831.107982</td>
      <td>на покупку своего автомобиля</td>
    </tr>
  </tbody>
</table>
</div>




```python
#  просмотрим основную информацию о датафрейме

data.info() 
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 21525 entries, 0 to 21524
    Data columns (total 12 columns):
     #   Column            Non-Null Count  Dtype  
    ---  ------            --------------  -----  
     0   children          21525 non-null  int64  
     1   days_employed     19351 non-null  float64
     2   dob_years         21525 non-null  int64  
     3   education         21525 non-null  object 
     4   education_id      21525 non-null  int64  
     5   family_status     21525 non-null  object 
     6   family_status_id  21525 non-null  int64  
     7   gender            21525 non-null  object 
     8   income_type       21525 non-null  object 
     9   debt              21525 non-null  int64  
     10  total_income      19351 non-null  float64
     11  purpose           21525 non-null  object 
    dtypes: float64(2), int64(5), object(5)
    memory usage: 2.0+ MB
    

**Вывод**

Прочитанные данные соответствуют описанию в техническом задании. 

## Предобработка данных

### Удаление пропусков


```python
# выведем количество пропущенных значений для каждого столбца.

data.isna().sum()
```




    children               0
    days_employed       2174
    dob_years              0
    education              0
    education_id           0
    family_status          0
    family_status_id       0
    gender                 0
    income_type            0
    debt                   0
    total_income        2174
    purpose                0
    dtype: int64



В двух столбцах есть пропущенные значения. Один из них — `days_employed`. Другой столбец с пропущенными значениями — `total_income` — хранит данные о доходах. На сумму дохода сильнее всего влияет тип занятости, поэтому заполнить пропуски в этом столбце возможно медианным значением по каждому типу из столбца `total_income`. Кроме этого, у клиента с типом занятости `сотрудник` пропуск в столбце `total_income` необходимо заполнить медианным доходом среди всех записей с тем же типом.


```python
 # функция заменяет NaN в total_income на медианное значение этого столбца у соответствующего income_type
    
def fillbygroup(data):
    unique_inc_type = data['income_type'].unique()
    for type in unique_inc_type:
        data.loc[data['income_type'] == type, 'total_income'] = data.loc[data['income_type'] == type, 'total_income'].fillna(data[data['income_type'] == type]['total_income'].median())
    return data
 
data = fillbygroup(data)
data.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 21525 entries, 0 to 21524
    Data columns (total 12 columns):
     #   Column            Non-Null Count  Dtype  
    ---  ------            --------------  -----  
     0   children          21525 non-null  int64  
     1   days_employed     19351 non-null  float64
     2   dob_years         21525 non-null  int64  
     3   education         21525 non-null  object 
     4   education_id      21525 non-null  int64  
     5   family_status     21525 non-null  object 
     6   family_status_id  21525 non-null  int64  
     7   gender            21525 non-null  object 
     8   income_type       21525 non-null  object 
     9   debt              21525 non-null  int64  
     10  total_income      21525 non-null  float64
     11  purpose           21525 non-null  object 
    dtypes: float64(2), int64(5), object(5)
    memory usage: 2.0+ MB
    


```python
# заполним пропуски в столбце days_employed медианными значениями по каждому типу занятости income_type.

for t in data['income_type'].unique():
    data.loc[(data['income_type'] == t) & (data['days_employed'].isna()), 'days_employed'] = \
    data.loc[(data['income_type'] == t), 'days_employed'].median()
data.isna().sum()    
```




    children            0
    days_employed       0
    dob_years           0
    education           0
    education_id        0
    family_status       0
    family_status_id    0
    gender              0
    income_type         0
    debt                0
    total_income        0
    purpose             0
    dtype: int64



### Обработка аномальных значений

Обработаем пропуски в столбце days_employed. Отрицательное количество дней трудового стажа - это аномалия. 


```python
# заменим все отрицательные значения положительными с помощью метода abs()

data['days_employed'] = data['days_employed'].abs()
```


```python
# для каждого типа занятости выведем медианное значение трудового стажа days_employed в днях.

data.groupby('income_type')['days_employed'].median()
```




    income_type
    безработный        366413.652744
    в декрете            3296.759962
    госслужащий          2689.368353
    компаньон            1547.382223
    пенсионер          365213.306266
    предприниматель       520.848083
    сотрудник            1574.202821
    студент               578.751554
    Name: days_employed, dtype: float64



У двух типов (безработные и пенсионеры) получатся аномально большие значения. Исправить такие значения сложно, поэтому оставьте их как есть.


```python
# выведем перечень уникальных значений столбца children, чтобы убедиться, что артефакты удалены.

data['children'].sort_values().unique()
```




    array([-1,  0,  1,  2,  3,  4,  5, 20], dtype=int64)




```python
# удалим строки столбца `children` в которых встречаются аномальные значения из датафрейма data

data = data.loc[data['children'] !=-1]
data = data.loc[data['children'] !=20]
```


```python
# выведем перечень уникальных значений столбца children, чтобы убедиться, что артефакты удалены.

data['children'].sort_values().unique()
```




    array([0, 1, 2, 3, 4, 5], dtype=int64)



### Заменим вещественный тип данных в столбце total_income на целочисленный с помощью метода astype().


```python
data['total_income'] = data['total_income'].astype('int')
```

### Обработка дубликатов


```python
# выведем уникальные занчения столбца `education`

data['education'].sort_values().unique()
```




    array(['ВЫСШЕЕ', 'Высшее', 'НАЧАЛЬНОЕ', 'НЕОКОНЧЕННОЕ ВЫСШЕЕ',
           'Начальное', 'Неоконченное высшее', 'СРЕДНЕЕ', 'Среднее',
           'УЧЕНАЯ СТЕПЕНЬ', 'Ученая степень', 'высшее', 'начальное',
           'неоконченное высшее', 'среднее', 'ученая степень'], dtype=object)




```python
# привем их к нижнему регистру и проверим результат

data['education'] = data['education'].str.lower()
data['education'].sort_values().unique()
```




    array(['высшее', 'начальное', 'неоконченное высшее', 'среднее',
           'ученая степень'], dtype=object)




```python
data.duplicated().sum()
data = data.drop_duplicates(keep='first')
```

### Категоризация данных

На основании диапазонов, указанных ниже, создадим в датафрейме data столбец **total_income_category** с категориями:

- 0–30000 — 'E';
- 30001–50000 — 'D';
- 50001–200000 — 'C';
- 200001–1000000 — 'B';
- 1000001 и выше — 'A'.


```python
# bспользуйем собственную функцию с именем categorize_income() и метод apply()

def categorize_income(income):
    if income < 30001:
        return 'E'
    elif 30001 <= income < 50001:
        return 'D'
    elif 50001 <= income <200001:
        return 'C'
    elif 200001 <= income <1000001:
        return 'B'
    else:
        return 'A'
```


```python
data['total_income_category'] = data['total_income'].apply(categorize_income)
```


```python
data['purpose'].sort_values().unique()
```




    array(['автомобили', 'автомобиль', 'высшее образование',
           'дополнительное образование', 'жилье',
           'заняться высшим образованием', 'заняться образованием',
           'на покупку автомобиля', 'на покупку подержанного автомобиля',
           'на покупку своего автомобиля', 'на проведение свадьбы',
           'недвижимость', 'образование', 'операции с жильем',
           'операции с коммерческой недвижимостью',
           'операции с недвижимостью', 'операции со своей недвижимостью',
           'покупка жилой недвижимости', 'покупка жилья',
           'покупка жилья для сдачи', 'покупка жилья для семьи',
           'покупка коммерческой недвижимости', 'покупка недвижимости',
           'покупка своего жилья', 'получение высшего образования',
           'получение дополнительного образования', 'получение образования',
           'приобретение автомобиля', 'профильное образование',
           'ремонт жилью', 'свадьба', 'свой автомобиль',
           'сделка с автомобилем', 'сделка с подержанным автомобилем',
           'строительство жилой недвижимости', 'строительство недвижимости',
           'строительство собственной недвижимости', 'сыграть свадьбу'],
          dtype=object)



Создадим функцию, которая на основании данных из столбца purpose сформирует новый столбец purpose_category, в который войдут следующие категории:

- `операции с автомобилем`,
- `операции с недвижимостью`,
- `проведение свадьбы`,
- `получение образования`.


```python
def categorize_purpose(row):
    try:
        if 'автом' in row:
            return 'операции с автомобилем'
        elif 'жил' in row or 'недвиж' in row:
            return 'операции с недвижимостью'
        elif 'свад' in row:
            return 'проведение свадьбы'
        elif 'образов' in row:
            return 'получение образования'
    except:
        return 'нет категории'
```


```python
data['purpose_category'] = data['purpose'].apply(categorize_purpose)
```

## Исследование данных 

### Есть ли зависимость между количеством детей и возвратом кредита в срок?


```python
# функция категоризации по кооличеству детей

def children_category(children):
    if 1 <= children <= 2:
        return 'есть дети'
    if children >= 3:
        return 'многодетный'
    return 'нет детей'
```


```python
# создаем столбец children_rank

data['children_rank'] = data['children'].apply(children_category)
```


```python
# Проверяем результат. Выведем последние 5 значений

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
      <th>children</th>
      <th>days_employed</th>
      <th>dob_years</th>
      <th>education</th>
      <th>education_id</th>
      <th>family_status</th>
      <th>family_status_id</th>
      <th>gender</th>
      <th>income_type</th>
      <th>debt</th>
      <th>total_income</th>
      <th>purpose</th>
      <th>total_income_category</th>
      <th>purpose_category</th>
      <th>children_rank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>21520</th>
      <td>1</td>
      <td>4529.316663</td>
      <td>43</td>
      <td>среднее</td>
      <td>1</td>
      <td>гражданский брак</td>
      <td>1</td>
      <td>F</td>
      <td>компаньон</td>
      <td>0</td>
      <td>224791</td>
      <td>операции с жильем</td>
      <td>B</td>
      <td>операции с недвижимостью</td>
      <td>есть дети</td>
    </tr>
    <tr>
      <th>21521</th>
      <td>0</td>
      <td>343937.404131</td>
      <td>67</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>пенсионер</td>
      <td>0</td>
      <td>155999</td>
      <td>сделка с автомобилем</td>
      <td>C</td>
      <td>операции с автомобилем</td>
      <td>нет детей</td>
    </tr>
    <tr>
      <th>21522</th>
      <td>1</td>
      <td>2113.346888</td>
      <td>38</td>
      <td>среднее</td>
      <td>1</td>
      <td>гражданский брак</td>
      <td>1</td>
      <td>M</td>
      <td>сотрудник</td>
      <td>1</td>
      <td>89672</td>
      <td>недвижимость</td>
      <td>C</td>
      <td>операции с недвижимостью</td>
      <td>есть дети</td>
    </tr>
    <tr>
      <th>21523</th>
      <td>3</td>
      <td>3112.481705</td>
      <td>38</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>M</td>
      <td>сотрудник</td>
      <td>1</td>
      <td>244093</td>
      <td>на покупку своего автомобиля</td>
      <td>B</td>
      <td>операции с автомобилем</td>
      <td>многодетный</td>
    </tr>
    <tr>
      <th>21524</th>
      <td>2</td>
      <td>1984.507589</td>
      <td>40</td>
      <td>среднее</td>
      <td>1</td>
      <td>женат / замужем</td>
      <td>0</td>
      <td>F</td>
      <td>сотрудник</td>
      <td>0</td>
      <td>82047</td>
      <td>на покупку автомобиля</td>
      <td>C</td>
      <td>операции с автомобилем</td>
      <td>есть дети</td>
    </tr>
  </tbody>
</table>
</div>




```python
# создаем копию датасета, что бы не работать с исходным

temp = data.copy()

# Напишем функцию, так как все задачи аналогичны

def que(category):
    data_temp = temp.pivot_table(index=category, values='debt', aggfunc=['count', 'sum', 'mean'])
    data_temp.columns = ['Всего кредитополучателей', 'Всего должников', 'Доля должников']
    # Оформим таблицу цветным градиентом, но можно ее вывести и просто display(data_temp)
    display(data_temp.style.format("{:.3f}").background_gradient(cmap='Blues', axis=0))
    
que('children')
```


<style type="text/css">
#T_a7086_row0_col0, #T_a7086_row0_col1, #T_a7086_row4_col2 {
  background-color: #08306b;
  color: #f1f1f1;
}
#T_a7086_row0_col2 {
  background-color: #1c6bb0;
  color: #f1f1f1;
}
#T_a7086_row1_col0 {
  background-color: #a9cfe5;
  color: #000000;
}
#T_a7086_row1_col1 {
  background-color: #8dc1dd;
  color: #000000;
}
#T_a7086_row1_col2 {
  background-color: #083d7f;
  color: #f1f1f1;
}
#T_a7086_row2_col0 {
  background-color: #dae8f6;
  color: #000000;
}
#T_a7086_row2_col1 {
  background-color: #d3e4f3;
  color: #000000;
}
#T_a7086_row2_col2 {
  background-color: #083776;
  color: #f1f1f1;
}
#T_a7086_row3_col0 {
  background-color: #f3f8fe;
  color: #000000;
}
#T_a7086_row3_col1 {
  background-color: #f2f8fd;
  color: #000000;
}
#T_a7086_row3_col2 {
  background-color: #0f5aa3;
  color: #f1f1f1;
}
#T_a7086_row4_col0, #T_a7086_row4_col1, #T_a7086_row5_col0, #T_a7086_row5_col1, #T_a7086_row5_col2 {
  background-color: #f7fbff;
  color: #000000;
}
</style>
<table id="T_a7086">
  <thead>
    <tr>
      <th class="blank level0" >&nbsp;</th>
      <th id="T_a7086_level0_col0" class="col_heading level0 col0" >Всего кредитополучателей</th>
      <th id="T_a7086_level0_col1" class="col_heading level0 col1" >Всего должников</th>
      <th id="T_a7086_level0_col2" class="col_heading level0 col2" >Доля должников</th>
    </tr>
    <tr>
      <th class="index_name level0" >children</th>
      <th class="blank col0" >&nbsp;</th>
      <th class="blank col1" >&nbsp;</th>
      <th class="blank col2" >&nbsp;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th id="T_a7086_level0_row0" class="row_heading level0 row0" >0</th>
      <td id="T_a7086_row0_col0" class="data row0 col0" >14091.000</td>
      <td id="T_a7086_row0_col1" class="data row0 col1" >1063.000</td>
      <td id="T_a7086_row0_col2" class="data row0 col2" >0.075</td>
    </tr>
    <tr>
      <th id="T_a7086_level0_row1" class="row_heading level0 row1" >1</th>
      <td id="T_a7086_row1_col0" class="data row1 col0" >4808.000</td>
      <td id="T_a7086_row1_col1" class="data row1 col1" >444.000</td>
      <td id="T_a7086_row1_col2" class="data row1 col2" >0.092</td>
    </tr>
    <tr>
      <th id="T_a7086_level0_row2" class="row_heading level0 row2" >2</th>
      <td id="T_a7086_row2_col0" class="data row2 col0" >2052.000</td>
      <td id="T_a7086_row2_col1" class="data row2 col1" >194.000</td>
      <td id="T_a7086_row2_col2" class="data row2 col2" >0.095</td>
    </tr>
    <tr>
      <th id="T_a7086_level0_row3" class="row_heading level0 row3" >3</th>
      <td id="T_a7086_row3_col0" class="data row3 col0" >330.000</td>
      <td id="T_a7086_row3_col1" class="data row3 col1" >27.000</td>
      <td id="T_a7086_row3_col2" class="data row3 col2" >0.082</td>
    </tr>
    <tr>
      <th id="T_a7086_level0_row4" class="row_heading level0 row4" >4</th>
      <td id="T_a7086_row4_col0" class="data row4 col0" >41.000</td>
      <td id="T_a7086_row4_col1" class="data row4 col1" >4.000</td>
      <td id="T_a7086_row4_col2" class="data row4 col2" >0.098</td>
    </tr>
    <tr>
      <th id="T_a7086_level0_row5" class="row_heading level0 row5" >5</th>
      <td id="T_a7086_row5_col0" class="data row5 col0" >9.000</td>
      <td id="T_a7086_row5_col1" class="data row5 col1" >0.000</td>
      <td id="T_a7086_row5_col2" class="data row5 col2" >0.000</td>
    </tr>
  </tbody>
</table>



**Вывод**: 

*Наличие детей повышает вероятность задолженности.*

* Возможно, это связано с дополнительными расходами на детей. Однако, в многодетных семьях уровень должников ниже (8.2%), чем в семьях с одним или двумя детьми (9.3%). Это может быть связано либо с тем, что существуют программы поддержки многодетных семей или количество заемщиков в категории "многодетный" для данного сравнения недостаточно. Для категории граждан без детей самый низкий показатель должников (7.3%).

### Есть ли зависимость между семейным положением и возвратом кредита в срок?


```python
# cформируем таблицу методом pivot_table()
debt_family_status = data.pivot_table(index='family_status', columns='debt', values='gender', aggfunc='count')

# cформируем столбцы
debt_family_status.columns = ['no_debt', 'debt']

# подсчитаем долю должников
debt_family_status['share_of_debtors'] = debt_family_status['debt'] / (debt_family_status['debt'] + debt_family_status['no_debt'])

# переведем значения в столбце доля дожников в проценты
debt_family_status['share_of_debtors'] = debt_family_status['share_of_debtors'].map('{:.1%}'.format)

# oтсортируем столбец доля должников по убыванию
debt_family_status.sort_values(by='share_of_debtors', ascending=False)
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
      <th>no_debt</th>
      <th>debt</th>
      <th>share_of_debtors</th>
    </tr>
    <tr>
      <th>family_status</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Не женат / не замужем</th>
      <td>2523</td>
      <td>273</td>
      <td>9.8%</td>
    </tr>
    <tr>
      <th>гражданский брак</th>
      <td>3749</td>
      <td>385</td>
      <td>9.3%</td>
    </tr>
    <tr>
      <th>женат / замужем</th>
      <td>11334</td>
      <td>927</td>
      <td>7.6%</td>
    </tr>
    <tr>
      <th>в разводе</th>
      <td>1105</td>
      <td>84</td>
      <td>7.1%</td>
    </tr>
    <tr>
      <th>вдовец / вдова</th>
      <td>888</td>
      <td>63</td>
      <td>6.6%</td>
    </tr>
  </tbody>
</table>
</div>



**Вывод:** 

*Холостые и живущие в граждансокм браке пары больше подвержены риску стать должниками.*

* Может быть, это связано с тем, что у них больше свободы действий по распоряжению своими средствами. У них нет совместных накоплений, каждый распоряжается своими средствами по своему. Остальные категории, находящиеся в браке или на текущей момент в браке имеют меньшие проценты должников. Наиболее низкий процент у категории вдовец/вдова (6.6%). Это может быть связано с дополнительными средствами, доставшимися по наследству.

### Есть ли зависимость между уровнем дохода и возвратом кредита в срок?


```python
# сформируем таблицу методом pivot()
debt_total_income = data.pivot_table(index='total_income_category', columns='debt', values='gender', aggfunc='count')

# сформируем столбцы
debt_total_income.columns = ['no_debt', 'debt']

# подсчитаем долю должников
debt_total_income['share_of_debtors'] = debt_total_income['debt'] / (debt_total_income['debt'] + debt_total_income['no_debt'])

# переведем значения в столбце доля дожников в проценты
debt_total_income['share_of_debtors'] = debt_total_income['share_of_debtors'].map('{:.1%}'.format)

# отсортируем по столбцу доля лолжников по убыванию
debt_total_income.sort_values(by='share_of_debtors', ascending=False)
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
      <th>no_debt</th>
      <th>debt</th>
      <th>share_of_debtors</th>
    </tr>
    <tr>
      <th>total_income_category</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>E</th>
      <td>20</td>
      <td>2</td>
      <td>9.1%</td>
    </tr>
    <tr>
      <th>C</th>
      <td>14568</td>
      <td>1353</td>
      <td>8.5%</td>
    </tr>
    <tr>
      <th>A</th>
      <td>23</td>
      <td>2</td>
      <td>8.0%</td>
    </tr>
    <tr>
      <th>B</th>
      <td>4660</td>
      <td>354</td>
      <td>7.1%</td>
    </tr>
    <tr>
      <th>D</th>
      <td>328</td>
      <td>21</td>
      <td>6.0%</td>
    </tr>
  </tbody>
</table>
</div>



**Вывод**

*Категория граждан (С) со средним доходом (50001–200000) больше подвержены риску стать должниками.*

* Несмотря на то, что в итоговой таблице должников данная категория граждан имеет не самый высокий процент по должникам, для точного исследования нам необходимо рассматривать репрезентативные выборки (категории граждан). Соответственно категории "E" и "A" мы не берем в расчет (из-за маленькой выборки), а выводы делаем опираясь на категории C, B, D. Сравнивая эти категории можно сделать вывод, что наибольший риск стать должниками у категории C, а наименьший у категории D.

### Как разные цели кредита влияют на его возврат в срок?


```python
# сформируем таблицу методом pivot_table()
debt_purpose_category = data.pivot_table(index='purpose_category', columns='debt', values='gender', aggfunc='count')

# сформируем столбцы
debt_purpose_category.columns = ['no_debt', 'debt']

# подсчитаем долю должников
debt_purpose_category['share_of_debtors'] = debt_purpose_category['debt'] / (debt_purpose_category['debt'] + debt_purpose_category['no_debt'])

# переводем значения в столбце доля дожников в проценты
debt_purpose_category['share_of_debtors'] = debt_purpose_category['share_of_debtors'].map('{:.1%}'.format)

# отсортируем по столбцу доля лолжников по убыванию
debt_purpose_category.sort_values(by='share_of_debtors', ascending=False)
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
      <th>no_debt</th>
      <th>debt</th>
      <th>share_of_debtors</th>
    </tr>
    <tr>
      <th>purpose_category</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>операции с автомобилем</th>
      <td>3879</td>
      <td>400</td>
      <td>9.3%</td>
    </tr>
    <tr>
      <th>получение образования</th>
      <td>3619</td>
      <td>369</td>
      <td>9.3%</td>
    </tr>
    <tr>
      <th>проведение свадьбы</th>
      <td>2130</td>
      <td>183</td>
      <td>7.9%</td>
    </tr>
    <tr>
      <th>операции с недвижимостью</th>
      <td>9971</td>
      <td>780</td>
      <td>7.3%</td>
    </tr>
  </tbody>
</table>
</div>



**Вывод:**

*Граждане, берущие кредиты на получение образования и операции с автомобилем больше подвержены риску стать должниками.*

* Эти две категории имеют одинаковый процент должников (9.3%). Граждане, которые берут кредит для проведения операций с недвижимостью более отвественно подходят к его погашению. Заемщики оформляющие кредиты на получение образования и операции с автомобилем больше подвержены риску стать должниками. Денежные средства взятые на дополнительное образование или приобретение автомобиля несут для заемщика дополнительные риски невозврата кредита по причине непредвиденных расходов связанных с эксплуатацией автомобиля (крупные поломки и ДТП), а также проблемы при трудоустройстве на новую работу или непредвиденное увеличение срока поиска новой работы.

## Приведите возможные причины появления пропусков в исходных данных

**Вывод:**

*Появленные пропуски в исходных данных могли появиться по следующим причинам:*

- **Организационного характера** - политика конфиденциальности банка препятсвующая иденификации отдельных физических лиц или
  юридических лиц.
- **Технического характера** - отсутсвующие данные могли появиться в следствии нарущениия процесса сбора и обработки данных, 
  програмных сбоев и проблем с оборудованием.
- **Человеческий фактор** - случайные и осознанные ошибки при вводе данных, а также нежелание отвечать на вопросы.
  

### Объясните, почему заполнить пропуски медианным значением — лучшее решение для количественных переменных

**Вывод**

Возможно, потому, что медиана устойчива к выбросам и аномальным значениям.

## Общий вывод

В ходе исследования надёжности заемщиков были изучены полученные данные, обработаны и заполнены пропуски, 
удалены дубликаты и клиенты были объединены в группы по разным параметрам. 

По итогам проделанной работы можно сделать следующие выводы:

- в целом, бездетные семья реже допускают задержки в платежах по кредиту, % должников держится на уровне 7.54%, но данные
  не однозначные, возможно, нужна большая выборка, чем та, которую мы имеем. 
- у группы клиентов, которые находятся или когда-либо находились в браке процент должников на уровне 7% - это на 2.1% ниже, 
  чем у людей никогда не состоявших в официальном браке. 
- уровень дохода напрямую коррелирует с возвратом кредита в срок - в зоне риска по просрочке платежа люди со средним заработком.
- чаще всего возвращают в срок кредиты на собственное жилье, а больше всего задержек по кредитам на автомобили и образование. 
  У групп клиентов, целью кредита у которых является автомобиль и образование: 9.3% должников (на 1.2% выше среднего).

Резюмируя можно сказать, что разброс значений по просроченным платежам не превышает двух процентов (от 7 до 9%), 
что означает разницу в вероятности просрочки платежа на 20%.


```python

```
