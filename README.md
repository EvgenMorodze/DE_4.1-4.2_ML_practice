# DE_4.1_4.2_ML_practice  
Репозиторий с практическими работами по теме "Машинное обучение на больших данных". Работы по соотвю. темам разложены по файлам:  
- **ML_4-1_morozov.ipynb**  
- **ML_4-2_morozov.ipynb**  

## 4.1. Машинное обучение на больших данных.

***


### 1. Постановка задачи.

Машинное обучение является одним из самых перспективных направлений в IT. В данной практической работе рассматривались основы машинного обучения: классы задач машинного обучения, линейные модели, методы борьбы с переобучением моделей и некоторые способы улучшения качества моделей. В рамках самостоятельной раборы требоуется обучить несколько моделей машинного обучения в Python и выполнить ряд задач по отбору признаков, разделению выборки, подбору гиперпараметров и расчёту метрик.  

Источник данных (kaggle titanic dataset): https://www.kaggle.com/competitions/titanic/data?select=train.csv


### 2. Ход работы.

1. Загрузка данных.
2. Исключение признаков, которые могут привести к переобучению (например, id).
3. Разделение выборки на train и test.
4. Преобразование категориальных и некатегориальных признаков
5. Подбор гиперпараметров для обоих моделей с помощью RandomizedSearchCV, обоснование выбора.
6. Обучение моделей логистической регрессии и KNN, получение метрик классификации, выводы.

### 3. Описание данных.

Датасет на странице соревнования представлен в разделённом на тренировочную и тестовую выборки виде, использовалась лишь тренировочная выборка. Данные представлены в табличном виде, описание содержащихся признаков ниже:  

Variable | Definition | Key | Notes
:------ | :------: | :------ | :------
***survival*** | Survival | 0 = No, 1 = Yes|
***pclass*** | Ticket class | 1 = 1st, 2 = 2nd, 3 = 3rd | 1st = Upper, 2nd = Middle, 3rd = Lower 
***sex*** | Sex | 
***Age*** |	Age in years | | Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5 
***sibsp***	| # of siblings / spouses aboard the Titanic | | The dataset defines family relations in this way:  ***Sibling*** *= brother, sister, stepbrother, stepsister.*  ***Spouse*** *= husband, wife (mistresses and fiancés were ignored)*  
***parch***	| # of parents / children aboard the Titanic | | The dataset defines family relations in this way:  ***Parent*** *= mother, father.*  ***Child*** *= daughter, son, stepdaughter, stepson. Some children travelled only with a nanny, therefore parch=0 for them.*
***ticket*** |	Ticket number	| 
***fare***	| Passenger fare	| 
***cabin***	| Cabin number	| 
***embarked***	| Port of Embarkation |	C = Cherbourg, Q = Queenstown, S = Southampton

