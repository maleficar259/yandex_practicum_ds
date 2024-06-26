# Проект "Определение стоимости автомобилей"

Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение для привлечения новых клиентов. В нём можно быстро узнать рыночную стоимость своего автомобиля. В нашем распоряжении исторические данные: технические характеристики, комплектации и цены автомобилей. Нам нужно построить модель для определения стоимости. 


***Цель исследования:*** 
Построить модель, которая с достаточной точностью предсказывала бы для клиентов стоимость автомобиля по предложенным параметрам

Предоставлена выгрузка объявлений из сервиса по продвжи автомобиля, где содержатся данные о технических характеристиках, комплектации и ценах других автомобилей.

***Ограничения исследования:***
1. Заказчику важны:
    - качество предсказания
    - скорость предсказания
    - время обучения
2. Следует использовать несколько различных моделей одна из которых — LightGBM, как минимум одна — не бустинг
3. Значение метрики RMSE должно быть меньше 2500

***Ход исследования:***  
Наше исследование будет проходить в шесть этапов:  
1. Загрузка, обзор и предобработка данных
2. Подготовка выборок под различные модели
3. Обучение моделей и подбор гиперпараметров
4. Выбор модели исходя из значения RMSE и скорости обучения и предсказания
5. Тестирование выбранной модели и проверка ее на адексатность
6. Подготовка общего вывода


***Описание данных***  
* **Признаки**  
    - **DateCrawled** — дата скачивания анкеты из базы  
    - **VehicleType** — тип автомобильного кузова  
    - **RegistrationYear** — год регистрации автомобиля  
    - **Gearbox** — тип коробки передач  
    - **Power** — мощность (л.с.)  
    - **Model** — модель автомобиля  
    - **Kilometer** — пробег (км)  
    - **RegistrationMonth** — месяц регистрации автомобиля  
    - **FuelType** — тип топлива  
    - **Brand** — марка автомобиля  
    - **Repaired** — была машина в ремонте или нет  
    - **DateCreated** — дата создания анкеты  
    - **NumberOfPictures** — количество фотографий автомобиля  
    - **PostalCode** — почтовый индекс владельца анкеты (пользователя)  
    - **LastSeen** — дата последней активности пользователя  
* **Целевой признак**  
    - **Price** — цена (евро)  