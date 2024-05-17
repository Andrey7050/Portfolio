#  Создание дашборда по пользовательским событиям для агрегаторановостей

**Описание проекта**

Исседовать историю TED-конференции с помощью инструментов программы Tableau, найти взаимосвязи в данных, проанализировать и представить графицеское представление ключевых моментов и сделать выводы на основании полученных данных.

**Задачи проекта**

1. Построить дашборд «История выступлений»;
2. Построить дашборд «Тематики выступлений»;
3. Создать дашборд «Авторы выступлений»;
4. Создать дашборд на свободную тему:
   - «Другие» тематики;
   - «Просмотры и мероприятия».

**Описание данных**

Файлы *tableau_project_data_1.csv, tableau_project_data_2.csv*, *tableau_project_data_3.csv* хранят данные выступлений. У них одинаковая структура:
- **talk_id** — идентификатор выступления;
- **url** — ссылка на запись выступления;
- **title** — название выступления;
- **escription** — краткое описание;
- **film_date** — дата записи выступления;
- **duration** — длительность в секундах;
- **views** — количество просмотров;
- **main_tag** — основная категория, к которой относится выступление;
- **speaker_id** — уникальный идентификатор автора выступления;
- **laughter_count** — количество раз, когда аудитория смеялась в ходе выступления;
- **applause_count** — количество раз, когда аудитория аплодировала в ходе выступления;
- **language** — язык, на котором велось выступление;
- **event_id** — уникальный идентификатор конференции.

Файл *tableau_project_event_dict.csv* — справочник конференций. Описание таблицы:
- **conf_id** — уникальный идентификатор конференции;
- **event** — название конференции;
- **country** — страна проведения конференции.

Файл *tableau_project_speakers_dict.csv* — справочник авторов выступления. Описание таблицы:
- **author_id** — уникальный идентификатор автора выступления;
- **speaker_name** — имя автора;
- **speaker_occupation** — профессиональная область автора;
- **speaker_description** — описание профессиональной деятельности автора.

**План выполнения проекта**

**Шаг 1.** Загрузить и изучить предоставленные данные. Провести обьединение данных. Определить тип и состав данных. Настроить фильтры для определение пороговых значений.

**Шаг 2.** Постоение визуализаций на основе полученных данных.

**Шаг 3.** Составление дашбордов из построенных визуализаций;
   - дашборд «История выступлений»;
   - дашборд «Тематики выступлений»;
   - «Авторы выступлений»;
   - «Другие» тематики;
   - «Просмотры и мероприятия».
   
**Шаг 4.** Публикация дашбордов и размещение ссылки в проекте.

### Загрузка и изучение данных

Загрузить данные в Tableau.
С помощью Union объединить файлы **tableau_project_data** в единую таблицу. Объединить таблицу с данными выступлений, справочники конференций и авторов с помощью Relationship.

Изучить состав и типы данных. С помощью визуализации изучить, как количество конференций распределено по времени. Определить год, после которого количество выступлений скачкообразно выросло.
Настройть фильтр, который исключит все выступления до найденного порогового года на уровне источника данных.

### История выступлений 

Постройть дашборд **«История выступлений»**.

Изуть представленные данные о проведении TED-конференции в разрезе Выступлений по странам, Выступлений по годам, Процента выступлений по тематикам. Из построенных визуализаций необходимо создать дашборд «История выступлений». Для удобства последующего использования визуализации будут размещены на отдельных листах. После построение визуализаций будут размещены выводы. 

### Тематика выступлений

Создать дашборд **«Тематики выступлений»**.

Изучить предоставленные данные и выянить каким образом выступелния на коференции распределялись по тематикам. Выяснить наиболее популярные тематики. Определить распределение положительных реакций слушателей смеха.

### Авторы выступлений

Создать дашборд **«Авторы выступлений»**.

Изучить информацию об авторах, выступающих на конференциях, наиболее популярные области деятельности авторов. 

### Просмотр и мероприятия

Создать дашборд на свободную тему.

Добавьте в презентацию дашборд на свободную тему с двумя или тремя визуализациями. Варианты вопросов, на которые можно ответить дашбордом:
Как изменился состав тематик категории «Другие» в 2019–2021 годах?
Можно ли разделить конференции на категории? Как менялась популярность этих категорий со временем?
Не забудьте добавить свои выводы и наблюдения на дашборд.

### Создание презентации 

Создать презентацию.

С помощью story создать презентацию из четырёх слайдов:
 - дашборд «История выступлений»;
 - дашборд «Тематики выступлений»;
 - дашборд «Авторы выступлений»;
 - дашборд на свободную тему.
Опубликуйте презентацию на сайте Tableau Public. Не забудьте открыть к ней доступ.

### Ссылка на презентацию

[Ссылка на исследование TED-конференции Версия 1.5.](https://public.tableau.com/app/profile/andrey.manannikov/viz/TEDproject_17066312089540/TED2001-2021?publish=yes)