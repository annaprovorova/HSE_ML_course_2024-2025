# HSE_ML_course 2024-2025

Материалы практических занятий курса "Машинное обучение", 3 курс, НИУ ВШЭ

*Лектор Мыльников Л.А., семинары группы РИС-22-2*

*Семинарист Проворова А.А.*

---

В приложенных документах содержатся материалы с семинаров.


### Задания к семинарам:

### Модуль 1
---

**Семинар 1:**

##### Загрузка и визуализация данных

1) Скачать файлы данных или подобрать свои (https://disk.yandex.ru/d/ZKrrXqH5nrp2Gw )
   - DataSet1_1 – Данные о развитии ИТ технологий в регионах РФ (может быть решена задача кластеризации– разделения регионов)
   - DataSet1_2 – Данные о кражах в магазинах самообслуживания (задача классификации)
   - DataSet1_3 – Стоимость и объем продаж акций компании Google (работа с временными рядами, может быть решена задача прогнозирования)
   - DataSet1_4 – статистика заболеваемости COVID-19 по странам (работа с временными рядами)
   - Другие данные(временные ряды, для задачи классификации и для задачи кластеризации) с Kaggle или других источников в свободном доступе.

2) Создать файл программы на языке Python
3) Загрузить данные
4) Построить графики, провести визуальный анализ данных

*Дополнительные баллы:* 
1) Свой файл данных;
2) Качественный анализ данных (описание);
3) Использование дополнительных способов визуализации.

---

**Семинар 2**
##### Преобразование данных 

Материалы для работы на семинаре https://colab.research.google.com/drive/1VrvgDwUjJb4dxovWYmPJJiUlyREKNIde?usp=sharing

1) Подобрать данные с Kaggle или других источников в свободном доступе (Список источников [см. здесь](https://github.com/annaprovorova/HSE_ML_course_2024-2025/blob/main/%D0%98%D1%81%D1%82%D0%BE%D1%87%D0%BD%D0%B8%D0%BA%D0%B8%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85.md))
2) Вычислить новые показатели
3) Оценить Accuracy

*Дополнительные баллы:*
   1) Очистка данных
   2) Другие методы решения задачи или методы оценки эффективности
  
---

**Семинар 3**

##### Интерполяция данных

Материалы для работы на семинаре  https://colab.research.google.com/drive/1urQF4j1l9OK-uaqNhFfNqK_zoOh8bZJr?usp=sharing

1) Скачать файлы данных или подобрать свои (https://disk.yandex.ru/d/ADpRgSJX_uJ4qQ )
   - DataSet3_1 – Данные о частоте и потребляемой мощности электрической энергии офисным зданием (регулярный временной ряд)
      - Timestamp - дата в формате мм/дд/гггг чч:мм
      - OAT (F) - Outside Air Temperature — температура наружного воздуха, в градусах Фаренгейта.
      - Power (kW) - Мощность в киловаттах
   - DataSet3_2 – данные о курсе доллара и стоимости барреля нефти (нерегулярный временной ряд)
      - Data - дата в формате дд.мм.гггг
      - Dollar - стоимость 1 доллара в этот день
      - Oil Brent - стоимость одного барреля нефти Oil Brent  

Взять не менее 10 значений и построить по ним интерполяционные кривые 
   - по формуле Лагранжа
   - по формуле Ньютона
   - с использованием сплайнов (интерполяция кубическим сплайном)

*Дополнительные баллы:* 
1) Свой файл данных
2) Продолжить интерполяционные кривые за пределы рассматриваемого интервала
3) Реализовать построение кривых без использования встроенных функций/библиотек

---

**Семинар 4**

##### Однопараметрическая экстраполяция

Материалы для работы на семинаре https://colab.research.google.com/drive/1KmQA3_Qi3vmowZHjr963HjGWHjXr7-mS?usp=sharing

1) Взять файлы данных с временными рядами прошлых работ или подобрать свои (DataSet3_1, DataSet3_2, DataSet1_4).
2) Взять не менее 100 значений и разбить их на 2 выборки (80 и 20) и исследовать возможность прогнозирования с использованием одного параметра.
3) Использовать первые 80 значений для обучения моделей
   - методом МНК для функций $y=c_{0}+c_{1}*x+c_{2}*x^{2}$
   - методом kNN
   - ARIMA модели
5) Построить графики получаемых с использованием построенных моделей функций и нанести значения из тренировочной и тестовой выборок
  
*Дополнительные баллы:* 
1) Свой файл данных;
2) Усложнить функцию для метода МНК;
3) Реализовать методы МНК и/или kNN и/или авторегрессии без использования библиотек;
4) Проверить выбранные для описания значения (ряд) на стационарность (тест Дики-Фуллера + другие способы проверки).

---

**Семинар 5**

##### Многопараметрическая экстраполяция

Материалы для работы на семинаре https://colab.research.google.com/drive/1azVRrUDPn66QDAe_BHsZrg2udAT7_Lq5?usp=sharing

1) Взять файлы данных с временными рядами прошлых работ или подобрать свои
    - DataSet1_4 (ссылка прикреплена к заданию к семинару 1);
    - DataSet5_1 – «Динамика цен на основные социально значимые продовольственные товары в розничной сети Свердловской области» (данные сортированы по следующим столбцам:
         1) Дата мониторинга;
         2) кура охлажденная и мороженая. руб./кг;
         3) молоко цельное питьевое 2.5-3.2% жирности. руб./л.;
         4) мука пшеничная в/с. руб./кг;
         5) хлеб и булочные изделия из пшеничной муки 1 и 2 с.. руб./кг;
         6) яйцо куриное. руб./дес.;
         7) картофель. Руб./кг.;
    - DataSet5_2 – данные об аренде велосипедов (задание со школы Сириус 2022 года))
   (ссылка - https://disk.yandex.ru/d/lXRX2k0yiLwR5Q).
2) Выбрать параметры используемые для прогнозирования, взять не менее 100 значений и разбить их на 2 выборки (80 и 20)
3) Использовать первые 80 значений для обучения моделей
   -методом МНК (квадратичная гипотеза), методом kNN, методом SVM, методом Lasso, методом PLS
   3.1 Использовать не менее 2-х параметров для прогнозирования целевого параметра
   3.2. Добавить к параметрам из варианта 3.1 значения целевого параметра со сдвигом на один шаг в прошлое (отставание от прогнозируемого значения на один шаг)
4) Построить графики получаемых с использованием построенных моделей функций и нанести значения из тренировочной и тестовой выборок

*Дополнительные баллы:*

Реализовать прогнозирование на заданное (N) количество шагов в будущее  используя для прогнозирования каждого следующего шага (кроме первого) прогнозные значения параметров. Для прогнозирования первого значения используются реальные снятые значения. Обучение модели осуществляется как в основном задании.

---


**Семинар 6**

##### Сравнение временных рядов

Материалы для работы на семинаре https://colab.research.google.com/drive/1JORNtIQPIZ7VflyGv-g7LkoEbl_YaznF?usp=sharing

1) Взять файлы данных из предложенных наборов (3-4 нормативных и 3-4 ненормативных сигнала, https://disk.yandex.ru/d/l9hS2owRKUMdoQ )

Файлы содержание в названии h… - нормативная работа подшипника (сигналы с четырех датчиков вибрации) 
Файлы содержание в названии b… - не нормативная работа подшипника (сигналы с четырех датчиков вибрации)). 

2) Взять не менее 100 значений

3) Посчитать для всех сочетаний значения коэффициентов корреляции (Пирсона, Спирмена, Кендала) и сделать соответствующие выводы

4) Посчитать значение DTW для всех сочетаний, сравнить со значениями коэффициентов корреляции, сделать выводы
  
5) Посчитать спектральную плотность сигнала

6) Разложить временные ряды на составляющие

*Дополнительные баллы:*

1. Провести оценки коэффициентов корреляции и DTW для спектральной плотности сигнала 
2. Спрогнозировать составляющие полученные при разложении методом STL с использованием методов с предыдущего семинара, восстановить прогнозные значения, построить графики исходного и прогнозного временных рядов

**ВАЖНО!!! Обязательно посмотрите материалы Л.А. Мыльникова к семинару в SmartLMS**

---

**Семинар 7**

#### Проверка адекватности моделей

Материалы для работы на семинаре https://colab.research.google.com/drive/1ByOhFj4WNizDadDMpuZQwQ5pEQG9anLg?usp=sharing

1) Проверить адекватность полученных ранее (на практике 5) моделей
   - построить графики исходных и полученных данных
   - построить скрипичные и боксплот диаграммы исходных и полученных данных
   - получить значения $R^2$, RMSE, MAE, MAPE
   - проверить адекватность полученных моделей с помощью критериев Фишера и Стьюдента 

3) Произвести выбор модели на основе полученных результатов и критерия χ2
  
*Дополнительные баллы:* 

1. Построить функции распределения исходных данных 

2. Использовать дополнительные критерии/тесты проверки адекватности моделей

---

**Семинар 8**

#### Переход от задачи регрессии к задаче классификации

Материалы для работы на семинаре https://colab.research.google.com/drive/13of5sqxnxGgFFu6Md2WZQc7Y5pIeqPr5?usp=sharing

1) Построить регрессионную модель:
   - Либо спрогнозировать число сданных в аренду велосипедов (см. файл DataSet5_2.csv) с использованием множественной регресии, 
   - Либо взять свой файл данных.
2) Свести задачу регрессии к задаче классификации для этого ввести граничное значение (экономически выгодное значение числа сданных в аренду) для велосипедов и ввести дополнительную колонку (колонку класса) означающую эффективность или нет (1 или 0). 
3) Построить модель классификации для предсказания дней эффективной работы. Сравнить качество моделей предсказания дней эффективной работы (модели регрессии и классификации).
4) Сравнить качество моделей по критериям (Confusion Matrix, ROC кривая, Accuracy, Precision, Recall, F-мера, Log Loss)
  
*Дополнительные баллы:* 

1) Использовать свой файл данных 
2) Рассмотреть не менее 3-х дополнительных моделей классификации и обосновать выбор одной из них (Например, SVM, дерево и другие).

---

**Семинар 9**

##### Ассоциативные правила 

Материалы для работы на семинаре https://colab.research.google.com/drive/1EsIl1nRcqaKA5HQZop01PeKPgBt3SuRM?usp=sharing

1) Исследовать данные на наличие ассоциативных правил на файле отличном от использованного в примере (пример выполнен на файле расположенном по [ссылке](https://disk.yandex.ru/d/Qvwpjgm5lwU2yQ)) 
2) Попробовать создать различные ассоциативные правила в зависимости от выбранных метрик и их пороговых значений.
3) Интерпретировать полученные результаты 

*Дополнительные баллы*: 

1) Исследовать файл с использованием алгоритма SlopeOne 
2) Исследовать файл с использованием алгоритма PageRank алгоритма

---

**Семинар 10**

##### Повышение эффективности моделей

Материалы для работы на семинаре https://colab.research.google.com/drive/1oHAgqjFKxqCpvLi5U5lskynnCiXkU0f3?usp=sharing

1) Решить задачу классификации методами k-NN, SVM, Naive Bayes, Decision Tree и провести оценку качества.
   Предлагаемые файлы для работы:

   *DataSet11_2* - Необходимо выявить на основании параметров клиентов, выплатит ли он кредит вовремя, т.е. определить, выдавать ли ему кредит (скоринг-модель)

   *DataSet11_3* - Данные о режимах работы технического устройства. Предсказание температуры на выходе (будет температура выше или ниже заданного порога? Т.е произойдет или нет срабатывание защиты). BK_T25  должно быть <400 что бы не происходило срабатывания защиты!

   Файлы можно найти по [ссылке](https://disk.yandex.ru/d/FJs9p6fbMKLddA)

3) Выполнить кроссвалидацию и сравнить качество получаемых результатов с результатами полученными на предыдущем этапе 
4) Построить композицию моделей и сравнить качество модели с предыдущими результатами 

*Дополнительные баллы*: 

1) Использовать свой файл данных (НЕ СБАЛАНСИРОВАННЫЕ ДАННЫЕ!!!) 
2) Использовать другие виды кроссвалидации 
3) Использовать другие методы построения композиций моделей

---

**Семинар 11**

##### Работа с текстовыми данными

Материалы для работы на семинаре [https://colab.research.google.com/drive/1oHAgqjFKxqCpvLi5U5lskynnCiXkU0f3?usp=sharing](https://colab.research.google.com/drive/1KpxWgIhxPkxbjn_4IukpKx_cwrQpazfJ?usp=sharing)

(файлы данных см. по [ссылке](https://disk.yandex.ru/d/HHKOvuZqKmcmbw))

Обучите модель для определения принадлежности текста к одному из заданных классов. При разборе текста
используйте Bag-of-words. Используйте свой файл данных. 

*Дополнительные баллы*:

1. Используйте TF-IDF
2. Используйте множественную классификацию


---

**Семинар 13**

##### Работа с текстовыми данными (часть 2)

Материалы для работы на семинаре https://colab.research.google.com/drive/1xye197dijco2Rsh2iyqcZIbdXBnPzJZk?usp=sharing
(файлы данных см. по [ссылке](https://disk.yandex.ru/d/y3y3dCl-2-dN5g)).

1) Обучите модель для определения принадлежности текста к одному из заданных классов. При разборе текста
используйте разбор текста по частям речи и построение векторов. Использовать свой файл данных **на другом языке**.
2) Проведите апробацию модели на всех приведенных файлах.
3) Сравнить результаты и сделать выводы.

Для определения класса используйте таблицу следующего вида:

![image](https://github.com/annaprovorova/HSE_ML_course/assets/42402997/5808a837-b6ce-4665-b566-c01b2b99bfa8)

*Дополнительные баллы*:

1. Изменить набор выделяемых частей речи (ввести дополнительные)

---

**Семинар 14:**

##### Работа с текстовыми данными (часть 3 – прототип чат бота)

1) Изучите предложенный пример. 
2) Модифицируйте предложенный пример под свои пары вопрос-ответ и сформулируйте не менее 5 своих вопросов.
3) Исследуйте работу системы и сделайте выводы о применимости к своему набору данных способов оценки схожести и структурирования информации и текстовых данных.
  
*Дополнительные баллы*: 
1. Доработайте код таким образом чтобы у него был интерфейс через который можно было формулировать вопрос и получать ответ.

**или**

2. Сделайте бонусное задание, подключив API любого сайта (по Вашему выбору).
   
---


# Важная информация!

Как расчитывается оценка?

**Оценка за 1 и 2 модуль** = округление до целого $(0.1 * Score_{1} + 0.5 * Score_{2} + 0.2 * Score_{3} + 0.2 * Score_{add})$

$Score_{1}$ - оценка за результаты текущего тестирования (проводится после лекционного занятия). Результаты каждого тестирования принимают бинарное значение от 0 до 10. Итоговый результат Score_1 определяется как среднее арифметическое результатов тестирования. Оценка 10 за каждый тест ставится при условии правильного ответа на все вопросы (если отдельно не оговорено, что 10 может быть поставлено при неполном ответе).

$Score_{2}$ – оценка за выполнение заданий на практиках. Принимает значение от 0 до 10. Результат Score_2 определяется как среднее арифметическое оценок за выполнение практик. Оценка за задание на практику ставится исходя из качества выполнения работы (0 - работа не выполнена, 8 - полное выполнение **и объяснение** задания по примеру, 9-10 полное выполнение задания и дополнительных требований к нему.

$Score_{3}$ – оценка за экзамен(финальное тестирование). Принимает значение от 0 до 10. Экзамен проводится в форме тестирования, содержащего вопросы по теории и вычислительные задания. Оценка зависит от процента правильных ответов. 

$Score_{add}$ – дополнительные баллы. Может принимать от 0 до 10 баллов. ставится за использование материалов курса в исследовательской и прикладной работе (подготовка публикаций, выступлений, участие в конкурсах) по тематике курса. Конкретный балл выставляется в зависимости от достигнутого результата и уровня журнала/конференции/конкурса.
