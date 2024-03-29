Инструменты:
pandas, numpy, matplotlib, sklearn.[train_test_split, DecisionTreeClassifier, RandomForestClassifier, KNeighborsClassifier, LogisticRegression, roc_auc_score, f1_score, StandardScaler,RobustScaler, MinMaxScaler, PolynomialFeatures, Pipeline]

Самостоятельный проект. Обучение с учителем: качество модели

Задачи исследования
Построение модели, которая предскажет вероятность снижения покупательской активности клиента в следующие три месяца.
В исследование нужно включить дополнительные данные финансового департамента о прибыльности клиента: какой доход каждый покупатель приносил компании за последние три месяца.
Используя данные модели и данные о прибыльности клиентов, нужно выделить сегменты покупателей и разработать для них персонализированные предложения.

Этапы исследования
Шаг 1. Загрузка данных
Шаг 2. Предобработка данных
Шаг 3. Исследовательский анализ данных
Шаг 4. Объединение таблиц
Шаг 5. Корреляционный анализ
Шаг 6. Использование пайплайнов
Шаг 7. Анализ важности признаков
Шаг 8. Сегментация покупателей
Шаг 9. Общий вывод


Вывод по предобработке:

Проверил размерность
Проверил типы данных
Ввел доп. показатели
Подготовил данные для анализа данных Данные не обладали резкими выбросами или значительными искажениями.

Вывод по исследовательсткому анализу:

Целевой признак распределен неравномерно, большая часть пользователей сохранила свой уровень активности
Количество клиентов со стандартной подпиской почти в 2.5 раза больше чем премьер.
Большая часть клиентов оставляет оповещения от приложения, возможно это связано с их малой частотой либо сложностями в отключении.
Основная масса пользователей приносит выгоду в размере от 3 до 6 процентов, однако присутствует некоторое количество тех, кто покупает более выгодные для маркетплейсов товары.
Наибольшее количество клиентов приносит 4%.
Почти половина клиентов имеет среднее значение взаимодействий с марктеплейсом (4), а количество тех кто обращается меньше и больше раз равно.
Можно заметить что количество привлекаемых пользователей плавно падает по мере существования магазина, возможно это связано с уменьшением количества не пользующихся им людей.

Клиенты делятся на 2 группы
Первая покупает только во время акций, из за чего показатель стремится к 1
Вторая производит покупки постоянно, не подстраивая график под акции
Наибольшую популрность имею товары детей
Меньше всего покупают Кухонную посуду
В среднем клиент просматривает от 2 до 5 категорий за визит.
Большая часть клиентов имеет малое количество неоплаченных покупок.
В среднем клиент получает от 2 до 6 ошибок в месяц

Средняий показатель проведенного времени у пользоватей 20-35 минут. Скорее всего этого времени хватает на просмотр свежих предложений либо поиск нужного товара и его сравнения с аналогами.

В среднем общая выручка от клиента за 3 месяца находится в промежутке от 12500 до 17500. Присутвуют значения как сильно меньше, так и больше, но они скорее всего связаны с заинтересованностью отдельных клиентов в маркетплейсе.

Средний показатель выручки у пользоватей 3-5.5 процентов. Видимо этот показатель наиболее характерен для представленных товаров, с учетом периодических акций, сокращающих этот процесс в случае отдельной покупки

Объединение таблиц:
Получен основной датасет, в него включены данные о выручке, прибыли и проведенном времени.
Полученный набор данных подготовленк дальнейшему анализу

Корреляционный анализ: Наибольшее влияние на покупательскую активность оказывают такие показатели как:

Время проведенное на сайте (как бщее так и в отдельные месяцы) Страниц_за_визит Маркет_актив6мес (активность за послдние месяцы) Средний_просмотр_категорий_за_визит Выручка_пред2_мес (выручка за препредыдущий месяц) (возможно это связано с тем что при выгодной деятельности работа на сайте продолжается, а при ошибке пользователь уходит, либо с каким либо мероприятием, проходившим за месяц до момента сбора данных)

С учетом этих данных в дальнейшем будет строиться формирвоание и обучение моделей в пайплайнах, а также дальнешйая сегментация по резльтатам.

Пайплайны:

Проведено формирвоание и обучение пайплайнов.
отобрана наиболее подходящая нам метрика для оценки и финальная модель на основе сравнения результатов исследований.
DecisionTreeClassifier(max_depth=8, max_features=9, random_state=42)

Проведены проверки качества модели

Анализ признаков:
На основе лучшей модели проводим анализ и визуализацию показателей. Отобран второй список наиболее важных для целевого признака показателей: Общее время
Страниц за визит Тип сервиса Кол-во неоплаченных продуктов Наличие ошибок Акционные покупки Категории покупки

Полученный данные используем в дальнейшем для дальнейшей сегментации

Сегментация покупателей:

Мы выделяем целевую группу пользователей Наиболее крупная группа пользователей имеет среднюю прибыль (от 3 до 5 процентов примерно) Ее покупательскую активность стоит повысить, сравнив ее показателями с группой пользователей, обладающих большей прибылью.

Производим ее разделение по целевому признаку, сравниваем показатели влияющих на него показателей и делаем выводы о том на что нужно обратить внимание для улучшения эффективности работы.

Финал

Согласно результатам исследования для улучшения удержания клиентов следует обратить внимание на следующие вещи:

Увеличение количества их прибыли( А следовательно либо изменение ценовой политики, либо увелечения количества акций)
Улучшение качества работы сервиса (Ошибки сильно влияют на удржание аудитории)
Увеличением количества премиум-пользователй
Возможно стоит обратить внимание подачу информации о товаре или интерфейс, ведь постоянные пользователи проводят на сайте значительно меньше времени чем те кто уходят с площадки.