# Исследование объявлений о продаже квартир

----

## Описание проекта


В нашем распоряжении данные сервиса Яндекс Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктах за несколько лет. Цель исследования -  определить рыночную стоимость объектов недвижимости. Для этого нужно провести исследовательский анализ данных и установить параметры, влияющие на цену объектов.**
По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта и других объектов — эти данные автоматически получены из геосервисов. Количество парков и водоёмов также заполняется без участия пользователя.**


## Описание данных


Данные хранятся в файле real_estate_data.csv.

- airports_nearest — расстояние до ближайшего аэропорта в метрах (м)
- balcony — число балконов
- ceiling_height — высота потолков (м)
- cityCenters_nearest — расстояние до центра города (м)
- days_exposition — сколько дней было размещено объявление (от публикации до снятия)
- first_day_exposition — дата публикации
- floor — этаж
- floors_total — всего этажей в доме
- is_apartment — апартаменты (булев тип)
- kitchen_area — площадь кухни в квадратных метрах (м²)
- last_price — цена на момент снятия с публикации
- living_area — жилая площадь в квадратных метрах (м²)
- locality_name — название населённого пункта
- open_plan — свободная планировка (булев тип)
- parks_around3000 — число парков в радиусе 3 км
- parks_nearest — расстояние до ближайшего парка (м)
- ponds_around3000 — число водоёмов в радиусе 3 км
- ponds_nearest — расстояние до ближайшего водоёма (м)
- rooms — число комнат
- studio — квартира-студия (булев тип)
- total_area — общая площадь квартиры в квадратных метрах (м²)
- total_images — число фотографий квартиры в объявлении


##Последовательность выполнения проекта##


Шаг 1. Открыть файл с данными и изучить общую информацию.

- Загрузите данные из csv-файла в датафрейм.
- Изучить общую информацию о полученном датафрейме.
- Построить гистограмму для всех числовых столбцов таблицы на одном графике.

Шаг 2. Выполните предобработку данных

- Найти и изучить пропущенные значения в столбцах.
- Определить, в каких столбцах есть пропуски.
- Заполните пропущенные значения там, где это возможно.
- Изучить типы данных в столбцах и изменить их при необходимости.
- Изучите уникальные значения, устраните неявные дубликаты.

Шаг 3. Добавить в таблицу новые столбцы со следующими параметрами:

- цена одного квадратного метра;
- день недели публикации объявления;
- месяц публикации объявления;
- год публикации объявления;
- тип этажа квартиры;
- расстояние до центра города в километрах.

Шаг 4. Провести исследовательский анализ данных.

- Изучить перечисленные ниже параметры объектов и построить отдельные гистограммы для каждого из них:
 - общая площадь;
 - жилая площадь;
 - площадь кухни;
 - цена объекта;
 - количество комнат;
 - высота потолков;
 - тип этажа квартиры;
 - общее количество этажей в доме;
 - расстояние до центра города в метрах;
 - расстояние до ближайшего парка.
- Изучить, как быстро продавались квартиры, построить гистограмму, посчитать среднее и медиану.
- Определите факторы, которые больше всего влияют на стоимость объекта. Изучить, зависит ли цена от:
 - общей площади;
 - жилой площади;
 - площади кухни;
 - количества комнат;
 - этажа, на котором расположена квартира;
 - даты размещения (день недели, месяц, год).
- Построить графики, которые покажут зависимость цены от указанных выше параметров.
- Посчитать среднюю цену одного квадратного метра в 10 населённых пунктах с наибольшим числом объявлений. Построить сводную таблицу с количеством объявлений и средней ценой квадратного метра для этих населенных пунктов. Выделить населённые пункты с самой высокой и низкой стоимостью квадратного метра.
- Вычислить среднюю стоимость квартир в Санкт-Петербурге на разном удалении от центра, учитывая каждый километр расстояния, построить график изменения средней цены.

Шаг 5. Написать общий вывод
