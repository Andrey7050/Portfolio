<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#Обзор-данных" data-toc-modified-id="Обзор-данных-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>Обзор данных</a></span></li><li><span><a href="#Предобработка-данных" data-toc-modified-id="Предобработка-данных-2"><span class="toc-item-num">2&nbsp;&nbsp;</span>Предобработка данных</a></span><ul class="toc-item"><li><span><a href="#Стиль-заголовков" data-toc-modified-id="Стиль-заголовков-2.1"><span class="toc-item-num">2.1&nbsp;&nbsp;</span>Стиль заголовков</a></span></li><li><span><a href="#Пропуски-значений" data-toc-modified-id="Пропуски-значений-2.2"><span class="toc-item-num">2.2&nbsp;&nbsp;</span>Пропуски значений</a></span></li><li><span><a href="#Дубликаты-данных" data-toc-modified-id="Дубликаты-данных-2.3"><span class="toc-item-num">2.3&nbsp;&nbsp;</span>Дубликаты данных</a></span></li></ul></li><li><span><a href="#Проверка-гипотез" data-toc-modified-id="Проверка-гипотез-3"><span class="toc-item-num">3&nbsp;&nbsp;</span>Проверка гипотез</a></span><ul class="toc-item"><li><span><a href="#Сравнение-поведения-пользователей-двух-столиц" data-toc-modified-id="Сравнение-поведения-пользователей-двух-столиц-3.1"><span class="toc-item-num">3.1&nbsp;&nbsp;</span>Сравнение поведения пользователей двух столиц</a></span></li><li><span><a href="#Музыка-в-начале-и-в-конце-недели" data-toc-modified-id="Музыка-в-начале-и-в-конце-недели-3.2"><span class="toc-item-num">3.2&nbsp;&nbsp;</span>Музыка в начале и в конце недели</a></span></li><li><span><a href="#Жанровые-предпочтения-в-Москве-и-Петербурге" data-toc-modified-id="Жанровые-предпочтения-в-Москве-и-Петербурге-3.3"><span class="toc-item-num">3.3&nbsp;&nbsp;</span>Жанровые предпочтения в Москве и Петербурге</a></span></li></ul></li><li><span><a href="#Итоги-исследования" data-toc-modified-id="Итоги-исследования-4"><span class="toc-item-num">4&nbsp;&nbsp;</span>Итоги исследования</a></span></li></ul></div>

# Исследование данных сервиса “Яндекс.Музыка” — сравнение пользователей двух городов

Сравнение музыкальных предпочтений жителей городов Москвы и Петербурга. На исходных данных Яндекс Музыки необходимо сравнить поведение пользователей двух столиц.

**Цель исследования** — проверьть на практике три предварительные гипотезы:
1. Может ли активность пользователей сервиса зависить от дня недели. Как это проявляется в Москве и Петербурге.
2. В понедельник утром в Москве предподчитают одни жанры, а в Петербурге — другие. Как и вечером пятницы предпочитают разные жанры — в зависимости от города.
3. Москва и Петербург предпочитают разные жанры музыки. Действительно ли в Москве чаще слушают поп-музыку, в Петербурге — русский рэп.

**Ход исследования**

1. Загрузить исходные данные о поведении пользователей из файла `yandex_music_project.csv`. 
2. Изучить исходные данные перед проверкой гипотез.
3. Проверить исходные данные на ошибки и оценить их влияние на исследование. Исправить самые критичные ошибки исходных данных.
4. Проверить первоначальные гипотезы.

##  Обзор данных


```python
# импортируем необходимые библиотеки
import pandas as pd
```


```python
# загрузим и причитаем мсходный файл
df = pd.read_csv('F:/Work projects/yandex_music_project.csv')
```


```python
# выведем на экран десять строк таблицы
df.head(10)
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
      <th>userID</th>
      <th>Track</th>
      <th>artist</th>
      <th>genre</th>
      <th>City</th>
      <th>time</th>
      <th>Day</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>FFB692EC</td>
      <td>Kamigata To Boots</td>
      <td>The Mass Missile</td>
      <td>rock</td>
      <td>Saint-Petersburg</td>
      <td>20:28:33</td>
      <td>Wednesday</td>
    </tr>
    <tr>
      <th>1</th>
      <td>55204538</td>
      <td>Delayed Because of Accident</td>
      <td>Andreas Rönnberg</td>
      <td>rock</td>
      <td>Moscow</td>
      <td>14:07:09</td>
      <td>Friday</td>
    </tr>
    <tr>
      <th>2</th>
      <td>20EC38</td>
      <td>Funiculì funiculà</td>
      <td>Mario Lanza</td>
      <td>pop</td>
      <td>Saint-Petersburg</td>
      <td>20:58:07</td>
      <td>Wednesday</td>
    </tr>
    <tr>
      <th>3</th>
      <td>A3DD03C9</td>
      <td>Dragons in the Sunset</td>
      <td>Fire + Ice</td>
      <td>folk</td>
      <td>Saint-Petersburg</td>
      <td>08:37:09</td>
      <td>Monday</td>
    </tr>
    <tr>
      <th>4</th>
      <td>E2DC1FAE</td>
      <td>Soul People</td>
      <td>Space Echo</td>
      <td>dance</td>
      <td>Moscow</td>
      <td>08:34:34</td>
      <td>Monday</td>
    </tr>
    <tr>
      <th>5</th>
      <td>842029A1</td>
      <td>Преданная</td>
      <td>IMPERVTOR</td>
      <td>rusrap</td>
      <td>Saint-Petersburg</td>
      <td>13:09:41</td>
      <td>Friday</td>
    </tr>
    <tr>
      <th>6</th>
      <td>4CB90AA5</td>
      <td>True</td>
      <td>Roman Messer</td>
      <td>dance</td>
      <td>Moscow</td>
      <td>13:00:07</td>
      <td>Wednesday</td>
    </tr>
    <tr>
      <th>7</th>
      <td>F03E1C1F</td>
      <td>Feeling This Way</td>
      <td>Polina Griffith</td>
      <td>dance</td>
      <td>Moscow</td>
      <td>20:47:49</td>
      <td>Wednesday</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8FA1D3BE</td>
      <td>И вновь продолжается бой</td>
      <td>NaN</td>
      <td>ruspop</td>
      <td>Moscow</td>
      <td>09:17:40</td>
      <td>Friday</td>
    </tr>
    <tr>
      <th>9</th>
      <td>E772D5C0</td>
      <td>Pessimist</td>
      <td>NaN</td>
      <td>dance</td>
      <td>Saint-Petersburg</td>
      <td>21:20:49</td>
      <td>Wednesday</td>
    </tr>
  </tbody>
</table>
</div>




```python
# выведем общую информацию о таблице 
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 65079 entries, 0 to 65078
    Data columns (total 7 columns):
     #   Column    Non-Null Count  Dtype 
    ---  ------    --------------  ----- 
     0     userID  65079 non-null  object
     1   Track     63848 non-null  object
     2   artist    57876 non-null  object
     3   genre     63881 non-null  object
     4     City    65079 non-null  object
     5   time      65079 non-null  object
     6   Day       65079 non-null  object
    dtypes: object(7)
    memory usage: 3.5+ MB
    

Исходная таблица состоит из семи столбцов. Тип данных во всех столбцах — `object`.

Согласно данных в техническом задании столбцы содержат:
* `userID` — идентификатор пользователя;
* `Track` — название трека;  
* `artist` — имя исполнителя;
* `genre` — название жанра;
* `City` — город пользователя;
* `time` — время начала прослушивания;
* `Day` — день недели.

Количество значений в столбцах различается, что говорит о наличии в данных пропущенных значений.

Кроме этого названия столбцов содержат следующие нарушения стиля:
1. Строчные буквы сочетаются с прописными.
2. Встречаются пробелы.
3. В названии нет нижнего подчеркивания.

**Вывод**

В каждой строке исходной таблицы — данные о прослушанном треке. Часть колонок описывает саму композицию: название, исполнителя и жанр. Остальные исходные данные рассказывают о пользователе сервиса: из какого он города, когда он слушал музыку.

После предварительного изучения можно утверждать, что данных достаточно для проверки гипотез. Но исходные данные содержат  пропуски в данных, а в названиях колонок — нарушение стиля.

Для проложения исследования необходимо устранить проблемы в данных.

## Предобработка данных

### Стиль заголовков


```python
# выведем на экран название столбцов
df.columns
```




    Index(['  userID', 'Track', 'artist', 'genre', '  City  ', 'time', 'Day'], dtype='object')




```python
# приведем наименование столбцов в соответствии с общими правилами
df = df.rename(columns={'  userID': 'user_id',
'Track': 'track',
'  City  ': 'city',
'Day': 'day'})
```


```python
# выведем для проверки результата на экран
df.columns
```




    Index(['user_id', 'track', 'artist', 'genre', 'city', 'time', 'day'], dtype='object')



### Пропуски значений


```python
# посчитаем количество пропущенных значений в таблице
df.isna().sum()
```




    user_id       0
    track      1231
    artist     7203
    genre      1198
    city          0
    time          0
    day           0
    dtype: int64



Пропуски в столбце `genre` могут помешать сравнить музыкальные вкусы в Москве и Санкт-Петербурге. В идеале было бы правильно установить причину пропусков и восстановить данные. На данный момент такой возможности нет. 

Поэтому придётся:
- заполнить и эти пропуски явными обозначениями;
- оценить, насколько они повредят расчётам.

Пропуски в исходных данных в столбцах `track` и `artist` не важны для исследования. Заменим их явными обозначениями.


```python
# заменим пропущенные значения в столбцах track, artist и genre на строку 'unknown'. Создадим список 
# columns_to_replace, который переберет его элементы циклом for и для каждого столбца выполнит замену пропущенных значений:
columns_to_replace = ['track', 'artist', 'genre']
for columns in columns_to_replace:
    df[columns] = df[columns].fillna('unknown') 
df = df.reset_index(drop=True)    
```


```python
# проверим результат замены данных в таблице
df.isna().sum()
```




    user_id    0
    track      0
    artist     0
    genre      0
    city       0
    time       0
    day        0
    dtype: int64



### Дубликаты данных

**Удаление явных дубликатов**


```python
# посчитаем явные дубликаты в исходной таблице
print('\033[1m' + 'Количество дубликатов в таблице:' + '\033[0m', df.duplicated().sum())
```

    [1mКоличество дубликатов в таблице:[0m 3826
    


```python
# удалим явные дубликаты в исходных данных
df = df.drop_duplicates()
```


```python
# проверим результат удаления явных дубликатов 
print('\033[1m' + 'Количество дубликатов в таблице:' + '\033[0m', df.duplicated().sum())
```

    [1mКоличество дубликатов в таблице:[0m 0
    

**Удаление неявных дубликатов**


```python
# выведем на экран список уникальных названий жанров, отсортированный в алфавитном порядке
df['genre'].sort_values().unique()
```




    array(['acid', 'acoustic', 'action', 'adult', 'africa', 'afrikaans',
           'alternative', 'alternativepunk', 'ambient', 'americana',
           'animated', 'anime', 'arabesk', 'arabic', 'arena',
           'argentinetango', 'art', 'audiobook', 'author', 'avantgarde',
           'axé', 'baile', 'balkan', 'beats', 'bigroom', 'black', 'bluegrass',
           'blues', 'bollywood', 'bossa', 'brazilian', 'breakbeat', 'breaks',
           'broadway', 'cantautori', 'cantopop', 'canzone', 'caribbean',
           'caucasian', 'celtic', 'chamber', 'chanson', 'children', 'chill',
           'chinese', 'choral', 'christian', 'christmas', 'classical',
           'classicmetal', 'club', 'colombian', 'comedy', 'conjazz',
           'contemporary', 'country', 'cuban', 'dance', 'dancehall',
           'dancepop', 'dark', 'death', 'deep', 'deutschrock', 'deutschspr',
           'dirty', 'disco', 'dnb', 'documentary', 'downbeat', 'downtempo',
           'drum', 'dub', 'dubstep', 'eastern', 'easy', 'electronic',
           'electropop', 'emo', 'entehno', 'epicmetal', 'estrada', 'ethnic',
           'eurofolk', 'european', 'experimental', 'extrememetal', 'fado',
           'fairytail', 'film', 'fitness', 'flamenco', 'folk', 'folklore',
           'folkmetal', 'folkrock', 'folktronica', 'forró', 'frankreich',
           'französisch', 'french', 'funk', 'future', 'gangsta', 'garage',
           'german', 'ghazal', 'gitarre', 'glitch', 'gospel', 'gothic',
           'grime', 'grunge', 'gypsy', 'handsup', "hard'n'heavy", 'hardcore',
           'hardstyle', 'hardtechno', 'hip', 'hip-hop', 'hiphop',
           'historisch', 'holiday', 'hop', 'horror', 'house', 'hymn', 'idm',
           'independent', 'indian', 'indie', 'indipop', 'industrial',
           'inspirational', 'instrumental', 'international', 'irish', 'jam',
           'japanese', 'jazz', 'jewish', 'jpop', 'jungle', 'k-pop',
           'karadeniz', 'karaoke', 'kayokyoku', 'korean', 'laiko', 'latin',
           'latino', 'leftfield', 'local', 'lounge', 'loungeelectronic',
           'lovers', 'malaysian', 'mandopop', 'marschmusik', 'meditative',
           'mediterranean', 'melodic', 'metal', 'metalcore', 'mexican',
           'middle', 'minimal', 'miscellaneous', 'modern', 'mood', 'mpb',
           'muslim', 'native', 'neoklassik', 'neue', 'new', 'newage',
           'newwave', 'nu', 'nujazz', 'numetal', 'oceania', 'old', 'opera',
           'orchestral', 'other', 'piano', 'podcasts', 'pop', 'popdance',
           'popelectronic', 'popeurodance', 'poprussian', 'post',
           'posthardcore', 'postrock', 'power', 'progmetal', 'progressive',
           'psychedelic', 'punjabi', 'punk', 'quebecois', 'ragga', 'ram',
           'rancheras', 'rap', 'rave', 'reggae', 'reggaeton', 'regional',
           'relax', 'religious', 'retro', 'rhythm', 'rnb', 'rnr', 'rock',
           'rockabilly', 'rockalternative', 'rockindie', 'rockother',
           'romance', 'roots', 'ruspop', 'rusrap', 'rusrock', 'russian',
           'salsa', 'samba', 'scenic', 'schlager', 'self', 'sertanejo',
           'shanson', 'shoegazing', 'showtunes', 'singer', 'ska', 'skarock',
           'slow', 'smooth', 'soft', 'soul', 'soulful', 'sound', 'soundtrack',
           'southern', 'specialty', 'speech', 'spiritual', 'sport',
           'stonerrock', 'surf', 'swing', 'synthpop', 'synthrock',
           'sängerportrait', 'tango', 'tanzorchester', 'taraftar', 'tatar',
           'tech', 'techno', 'teen', 'thrash', 'top', 'traditional',
           'tradjazz', 'trance', 'tribal', 'trip', 'triphop', 'tropical',
           'türk', 'türkçe', 'ukrrock', 'unknown', 'urban', 'uzbek',
           'variété', 'vi', 'videogame', 'vocal', 'western', 'world',
           'worldbeat', 'ïîï', 'электроника'], dtype=object)



Изучение списка названий жанров выявило неявные дубликаты названия `hiphop`, вызванные ошибками или альтернативными названиями жанра.

В списке присутсвуют следующие неявные дубликаты:
* *hip*,
* *hop*,
* *hip-hop*.


```python
# методом `replace()` заменим каждое значение из списка дубликатов (`hip`, `hop` и `hip-hop`) на `hiphop`
duplicates = ['hip' , 'hop' , 'hip-hop']
name = 'hiphop'
df['genre'] = df['genre'].replace(duplicates, name)
```


```python
# провери результат замены неявных дубликатов
df['genre'].sort_values().unique()
```




    array(['acid', 'acoustic', 'action', 'adult', 'africa', 'afrikaans',
           'alternative', 'alternativepunk', 'ambient', 'americana',
           'animated', 'anime', 'arabesk', 'arabic', 'arena',
           'argentinetango', 'art', 'audiobook', 'author', 'avantgarde',
           'axé', 'baile', 'balkan', 'beats', 'bigroom', 'black', 'bluegrass',
           'blues', 'bollywood', 'bossa', 'brazilian', 'breakbeat', 'breaks',
           'broadway', 'cantautori', 'cantopop', 'canzone', 'caribbean',
           'caucasian', 'celtic', 'chamber', 'chanson', 'children', 'chill',
           'chinese', 'choral', 'christian', 'christmas', 'classical',
           'classicmetal', 'club', 'colombian', 'comedy', 'conjazz',
           'contemporary', 'country', 'cuban', 'dance', 'dancehall',
           'dancepop', 'dark', 'death', 'deep', 'deutschrock', 'deutschspr',
           'dirty', 'disco', 'dnb', 'documentary', 'downbeat', 'downtempo',
           'drum', 'dub', 'dubstep', 'eastern', 'easy', 'electronic',
           'electropop', 'emo', 'entehno', 'epicmetal', 'estrada', 'ethnic',
           'eurofolk', 'european', 'experimental', 'extrememetal', 'fado',
           'fairytail', 'film', 'fitness', 'flamenco', 'folk', 'folklore',
           'folkmetal', 'folkrock', 'folktronica', 'forró', 'frankreich',
           'französisch', 'french', 'funk', 'future', 'gangsta', 'garage',
           'german', 'ghazal', 'gitarre', 'glitch', 'gospel', 'gothic',
           'grime', 'grunge', 'gypsy', 'handsup', "hard'n'heavy", 'hardcore',
           'hardstyle', 'hardtechno', 'hiphop', 'historisch', 'holiday',
           'horror', 'house', 'hymn', 'idm', 'independent', 'indian', 'indie',
           'indipop', 'industrial', 'inspirational', 'instrumental',
           'international', 'irish', 'jam', 'japanese', 'jazz', 'jewish',
           'jpop', 'jungle', 'k-pop', 'karadeniz', 'karaoke', 'kayokyoku',
           'korean', 'laiko', 'latin', 'latino', 'leftfield', 'local',
           'lounge', 'loungeelectronic', 'lovers', 'malaysian', 'mandopop',
           'marschmusik', 'meditative', 'mediterranean', 'melodic', 'metal',
           'metalcore', 'mexican', 'middle', 'minimal', 'miscellaneous',
           'modern', 'mood', 'mpb', 'muslim', 'native', 'neoklassik', 'neue',
           'new', 'newage', 'newwave', 'nu', 'nujazz', 'numetal', 'oceania',
           'old', 'opera', 'orchestral', 'other', 'piano', 'podcasts', 'pop',
           'popdance', 'popelectronic', 'popeurodance', 'poprussian', 'post',
           'posthardcore', 'postrock', 'power', 'progmetal', 'progressive',
           'psychedelic', 'punjabi', 'punk', 'quebecois', 'ragga', 'ram',
           'rancheras', 'rap', 'rave', 'reggae', 'reggaeton', 'regional',
           'relax', 'religious', 'retro', 'rhythm', 'rnb', 'rnr', 'rock',
           'rockabilly', 'rockalternative', 'rockindie', 'rockother',
           'romance', 'roots', 'ruspop', 'rusrap', 'rusrock', 'russian',
           'salsa', 'samba', 'scenic', 'schlager', 'self', 'sertanejo',
           'shanson', 'shoegazing', 'showtunes', 'singer', 'ska', 'skarock',
           'slow', 'smooth', 'soft', 'soul', 'soulful', 'sound', 'soundtrack',
           'southern', 'specialty', 'speech', 'spiritual', 'sport',
           'stonerrock', 'surf', 'swing', 'synthpop', 'synthrock',
           'sängerportrait', 'tango', 'tanzorchester', 'taraftar', 'tatar',
           'tech', 'techno', 'teen', 'thrash', 'top', 'traditional',
           'tradjazz', 'trance', 'tribal', 'trip', 'triphop', 'tropical',
           'türk', 'türkçe', 'ukrrock', 'unknown', 'urban', 'uzbek',
           'variété', 'vi', 'videogame', 'vocal', 'western', 'world',
           'worldbeat', 'ïîï', 'электроника'], dtype=object)



**Вывод**

В процессе предобработки исходных данных обнаружило три проблемы в данных:

- нарушения в стиле заголовков,
- пропущенные значения,
- дубликаты — явные и неявные.

Для упрощения работы с таблицей исправили заголовки. Удал дубликаты для повышения точности исследования.

Пропущенные значения заменили на `'unknown'`. 

## Проверка гипотез

### Сравнение поведения пользователей двух столиц

**Первая гипотеза** говорит, что пользователи сервиса по-разному слушают музыку в Москве и Санкт-Петербурге. Проверьм это предположение по данным о трёх днях недели — понедельнике, среде и пятнице. 

Для этого необходимо:
- Разделить пользователей Москвы и Санкт-Петербурга.
- Сравним, сколько треков послушала каждая группа пользователей в понедельник, среду и пятницу.


```python
# оценим активность пользователей в каждом городе. Сгруппируем данные по городу и посчитайем прослушивания в каждой группе.
df.groupby('city') ['time'].count()
```




    city
    Moscow              42741
    Saint-Petersburg    18512
    Name: time, dtype: int64



В Москве прослушиваний больше, чем в Петербурге. Из этого не следует, что московские пользователи чаще слушают музыку. Просто самих пользователей в Москве больше.


```python
# сгруппируем данные по дню недели и посчитайте прослушивания в понедельник, среду и пятницу
df.groupby('day') ['time'].count()
```




    day
    Friday       21840
    Monday       21354
    Wednesday    18059
    Name: time, dtype: int64



В среднем пользователи из двух городов менее активны по средам. Но картина может измениться, если рассмотреть каждый город в отдельности.


```python
# создадим функцию number_tracks(), посчитываюшая прослушивания для заданного дня и города. Передадим ей два параметра:
# день недели, название города.
def number_tracks(day , city):
    track_list = df[df['day'] == day]
    track_list = track_list[track_list['city']== city]
    track_list_count = track_list['user_id'].count()
    return track_list_count
```


```python
# данные для понедельника и Москвы
print('\033[1m' + 'Количество прослушанных треков в понедельник пользователями Москвы:' + '\033[0m',
      number_tracks('Monday', 'Moscow'))
```

    [1mКоличество прослушанных треков в понедельник пользователями Москвы:[0m 15740
    


```python
# данные для понедельника и Санкт-Петербурга
print('\033[1m' + 'Количество прослушанных треков в понедельник пользователями Санкт-Петербурга:' + '\033[0m',
      number_tracks('Monday', 'Saint-Petersburg'))
```

    [1mКоличество прослушанных треков в понедельник пользователями Санкт-Петербурга:[0m 5614
    


```python
# данные для среды и Москвы
print('\033[1m' + 'Количество прослушанных треков в среду пользователями Москвы:' + '\033[0m',
      number_tracks('Wednesday', 'Moscow'))
```

    [1mКоличество прослушанных треков в среду пользователями Москвы:[0m 11056
    


```python
# данные для среды и Санкт-Петербурга
print('\033[1m' + 'Количество прослушанных треков в среду пользователями Санкт-Петербурга:' + '\033[0m',
      number_tracks('Wednesday', 'Saint-Petersburg'))
```

    [1mКоличество прослушанных треков в среду пользователями Санкт-Петербурга:[0m 7003
    


```python
# данные для пятницы и Москвы
print('\033[1m' + 'Количество прослушанных треков в пятницу пользователями Москвы:' + '\033[0m',
      number_tracks('Friday', 'Moscow'))
```

    [1mКоличество прослушанных треков в пятницу пользователями Москвы:[0m 15945
    


```python
# данные для среды и Санкт-Петербурга
print('\033[1m' + 'Количество прослушанных треков в пятницу пользователями Санкт-Петербурга:' + '\033[0m',
      number_tracks('Friday', 'Saint-Petersburg'))
```

    [1mКоличество прослушанных треков в пятницу пользователями Санкт-Петербурга:[0m 5895
    


```python
# создайте таблицу, где:

# - названия колонок — ['city', 'monday', 'wednesday', 'friday'];
# - данные — результаты, которые вы получили с помощью number_tracks.
data=[['Moscow',15740,11056, 15945], ['Saint-Petersburg',5614, 7003,5895 ]]
pd.DataFrame(data = data, columns = ['city', 'monday', 'wednesday', 'friday'])
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
      <th>city</th>
      <th>monday</th>
      <th>wednesday</th>
      <th>friday</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Moscow</td>
      <td>15740</td>
      <td>11056</td>
      <td>15945</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Saint-Petersburg</td>
      <td>5614</td>
      <td>7003</td>
      <td>5895</td>
    </tr>
  </tbody>
</table>
</div>



**Выводы**

Полученные данные показывают разницу поведения пользователей:

- В Москве пик прослушиваний приходится на понедельник и пятницу, а в среду заметен спад.
- В Петербурге, наоборот, больше слушают музыку по средам. Активность в понедельник и пятницу здесь почти в равной мере 
  уступает среде.

Значит, данные говорят в пользу первой гипотезы.

### Музыка в начале и в конце недели

Во **второй гипотезе** описывается утверждение, что утром в понедельник в Москве преобладают одни жанры, а в Петербурге — другие. Так же и вечером пятницы преобладают разные жанры — в зависимости от города.

Сохраните таблицы с данными в две переменные:


```python
# по Москве — в moscow_general
moscow_general = df[df['city']=='Moscow']
```


```python
# по Санкт-Петербургу — в spb_general
spb_general = df[df['city']=='Saint-Petersburg']
```

Создадим функцию `genre_weekday()` с четырьмя параметрами:

* таблица (датафрейм) с данными,
* день недели,
* начальная временная метка в формате 'hh:mm',
* последняя временная метка в формате 'hh:mm'.



```python
def genre_weekday(table, day, time1, time2): 
    genre_df = table[table['day'] == day]
    genre_df = genre_df[genre_df['time'] > time1]
    genre_df = genre_df[genre_df['time'] < time2]
    genre_df_count = genre_df.groupby('genre')['time'].count()
    genre_df_sorted =  genre_df_count.sort_values(ascending=False)
    return genre_df_sorted[:10]
```


```python
#  Cравните результаты функции genre_weekday() для Москвы и Санкт-Петербурга в понедельник утром (с 7:00 до 11:00) 
# и в пятницу вечером (с 17:00 до 23:00)
genre_weekday(moscow_general, 'Monday', '07:00', '11:00')
```




    genre
    pop            781
    dance          549
    electronic     480
    rock           474
    hiphop         286
    ruspop         186
    world          181
    rusrap         175
    alternative    164
    unknown        161
    Name: time, dtype: int64




```python
genre_weekday(spb_general, 'Monday', '07:00', '11:00') 
```




    genre
    pop            218
    dance          182
    rock           162
    electronic     147
    hiphop          80
    ruspop          64
    alternative     58
    rusrap          55
    jazz            44
    classical       40
    Name: time, dtype: int64




```python
genre_weekday(moscow_general, 'Friday', '17:00', '23:00')  
```




    genre
    pop            713
    rock           517
    dance          495
    electronic     482
    hiphop         273
    world          208
    ruspop         170
    alternative    163
    classical      163
    rusrap         142
    Name: time, dtype: int64




```python
genre_weekday(spb_general, 'Friday', '17:00', '23:00') 
```




    genre
    pop            256
    electronic     216
    rock           216
    dance          210
    hiphop          97
    alternative     63
    jazz            61
    classical       60
    rusrap          59
    world           54
    Name: time, dtype: int64



**Вывод**

При сравнении топ-10 жанров в понедельник утром, можно сделать такие выводы:

1. В Москве и Петербурге слушают похожую музыку. Единственное различие — в московский рейтинг вошёл жанр “world”, а в петербургский — джаз и классика.

2. В Москве пропущенных значений оказалось так много, что значение `'unknown'` заняло десятое место среди самых популярных жанров. Значит, пропущенные значения занимают существенную долю в данных и угрожают достоверности исследования.

Вечер пятницы не меняет эту картину. Некоторые жанры поднимаются немного выше, другие спускаются, но в целом топ-10 остаётся тем же самым.

Таким образом, вторая гипотеза подтвердилась лишь частично:
* Пользователи слушают похожую музыку в начале недели и в конце.
* Разница между Москвой и Петербургом не слишком выражена. В Москве чаще слушают русскую популярную музыку, в Петербурге — джаз.

Однако пропуски в данных ставят под сомнение этот результат. В Москве их так много, что рейтинг топ-10 мог бы выглядеть иначе, если бы не утерянные  данные о жанрах.

### Жанровые предпочтения в Москве и Петербурге

**Третья ипотеза**: Петербург — столица рэпа, музыку этого жанра там слушают чаще, чем в Москве. А Москва — город контрастов, в котором, тем не менее, преобладает поп-музыка.


```python
# сгруппируем таблицу moscow_general по жанру и посчитаем прослушивания треков каждого жанра методом count(). 
# затем отсортируем результ в порядке убывания и сохраним его в таблице moscow_genres.
moscow_genres=moscow_general.groupby('genre')['genre'].count().sort_values(ascending = False)
```


```python
# посмотрим десять строк moscow_genres 
moscow_genres.head(10) 
```




    genre
    pop            5892
    dance          4435
    rock           3965
    electronic     3786
    hiphop         2096
    classical      1616
    world          1432
    alternative    1379
    ruspop         1372
    rusrap         1161
    Name: genre, dtype: int64




```python
# сгруппируем таблицу spb_general по жанру. Посчитаеме прослушивания треков каждого жанра. 
# результат отсортируем в порядке убывания и сохраним в таблице spb_genres:
spb_genres = spb_general.groupby('genre')['genre'].count().sort_values(ascending=False)
```


```python
# посмотрим первые 10 строк spb_genres 
spb_genres.head(10)
```




    genre
    pop            2431
    dance          1932
    rock           1879
    electronic     1736
    hiphop          960
    alternative     649
    classical       646
    rusrap          564
    ruspop          538
    world           515
    Name: genre, dtype: int64



**Вывод**

Гипотеза подтвердилась частично:
* **Поп-музыка** — самый популярный жанр в Москве, как и предполагала гипотеза. Более того, в топ-10 жанров встречается близкий жанр — русская популярная музыка.
* Вопреки ожиданиям, рэп одинаково популярен в Москве и Петербурге.


## Итоги исследования

В процессе проведения исследования проверили три гипотезы и установили:

1. День недели влияет по-разному на активность пользователей в Москве и Петербурге.

Первая гипотеза полностью подтвердилась.

2. Музыкальные предпочтения пользователей сервиса не сильно меняются в течение недели — будь то Москва или Петербург. Небольшие различия заметны в начале недели, по понедельникам:
* в Москве слушают музыку жанра “world”,
* в Петербурге — джаз и классику.

Таким образом, вторая гипотеза подтвердилась лишь отчасти. Этот результат мог оказаться иным, если бы не пропуски в данных.

3. Во вкусах пользователей Москвы и Петербурга больше общего, чем различий. Вопреки ожиданиям, предпочтения жанров в Петербурге напоминают московские.

Третья гипотеза не подтвердилась. Если различия в предпочтениях и существуют, на основной массе пользователей они незаметны.
