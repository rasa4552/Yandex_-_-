Инструменты:
pandas, numpy, matplotlib, seaborn, sklearn.[LinearRegression, RandomForestRegressor, DecisionTreeRegressor, OrdinalEncoder, StandardScaler, GridSearchCV, TimeSeriesSplit], LGBMRegressor, CatBoostRegressor

Временные ряды. Имеются исторические данные о заказах такси в аэропортах. Нужно построить модель для предсказания количество заказов такси на следующий час.

В ходе проекта были обработаны данные о заказах такси.

Для прогноза количества заказов такси были построены 3 модели предскания.

Самой эффективной моделью, которая показала минимальную метрику RSME(41.815 ) является модель градиентного бустинга библиотеки LightGBM.

Требование о значении метрики RMSE выполнено.