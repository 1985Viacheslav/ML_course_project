# ML_course_project

Выполнил Брежнев Вячеслав Александрович группа М8О-109М-23

Описание проекта и план выполнения:
Датасет - информация из клиентской базы телекоммуникационной компании.

Аналитическая задача — построить регрессионную/классифицирующую модель.

Описание данных:
Каждый клиент описывается следующим набором признаков:

Возраст, Среднемесячный расход, Средняя продолжительность разговоров, Звонков днем за месяц, Звонков вечером за месяц, Звонков ночью за месяц, Звонки в другие города, Звонки в другие страны, Доля звонков на стационарные телефоны, Количество SMS за месяц, Дата подключения тарифа.
План выполнения:
Загружаем данные и библиотеки
Проводим первичный краткий EDA
Выбираем ML-модель и ставим задачу ререссии/классификации
Создаем класс с функциями загрузки данных, EDA первичных данных, фильтрации и очистки данных, EDA очищенных данных, предикта, GSCV
Оцениваем r2_score

Выбор ML-модели
Для выбранного датасета мы выберем модель регрессии и будем предсказывать колонку "Среднемесячный расход" на основе остальных колонок.
В качестве регрессионной модели возьмем Catboost.

Вывод
Предложенный алгоритм Catboost показывает себя на достаточно высоком уровне "прямо из коробки", что доказывается метриками.

r2_score (к-т детерминации) = 0,93 что говорит о крайне высоком качестве полученной модели, которая способна предсказывать траты каждого пользователя в зависимости от прееданных фичей. Данную модель можно с успехом использовать в реальных продуктовых задачах с целью выявления клиентов, которые готовы много тратить на услуги связи с целью удержания таких клиентов и повышения продуктовых/бизнесовых метрик, таких как LTV, AOV, ARPU и другие.

Дополнительно модель была подвергнута минимлаьной оптимизации с помощью алгоритма кросс-валидации, что также дает прирост качества целевых технических метрик.

Внутри реализованного класса есть множество методов, позволяющих провести тщательный и информативный анализ данных, на основе которого также можно сделать полезные для бизнеса выводы.

Ссылка на презентацию:
https://drive.google.com/file/d/10GtAlr18zi2wQm0ej0p0StYLWqEBMq8c/view?usp=sharing

