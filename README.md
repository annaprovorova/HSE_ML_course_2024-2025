# HSE_ML_course 2024-2025

Материалы практических занятий курса "Машинное обучение", 3 курс, НИУ ВШЭ

*Лектор Мыльников Л.А., семинары групп 3, 4 (Направление "Бизнес-информатика")*

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

1) Взять файлы данных с временными рядами прошлых работ или подобрать свои (DataSet3_1, DataSet3_2, DataSet1_4).
2) Взять не менее 100 значений и разбить их на 2 выборки (80 и 20) и исследовать возможность прогнозирования с использованием одного параметра.
3) Использовать первые 80 значений для обучения моделей - методом МНК для функций $y=c_{0}+c_{1}*x+c_{2}*x^{2}$ - методом kNN - ARIMA модели
4) Построить графики получаемых с использованием построенных моделей функций и нанести значения из тренировочной и тестовой выборок
  
*Дополнительные баллы:* 
1) Свой файл данных;
2) Усложнить функцию для метода МНК;
3) Реализовать методы МНК и/или kNN и/или авторегрессии без использования библиотек;
4) Проверить выбранные для описания значения (ряд) на стационарность (тест Дики-Фуллера + другие способы проверки).

---

# Важная информация!

Как расчитывается оценка?

**Оценка за 1 и 2 модуль** = округление до целого $(0.1 * Score_{1} + 0.5 * Score_{2} + 0.2 * Score_{3} + 0.2 * Score_{add})$

$Score_{1}$ - оценка за результаты текущего тестирования (проводится после лекционного занятия). Результаты каждого тестирования принимают бинарное значение от 0 до 10. Итоговый результат Score_1 определяется как среднее арифметическое результатов тестирования. Оценка 10 за каждый тест ставится при условии правильного ответа на все вопросы (если отдельно не оговорено, что 10 может быть поставлено при неполном ответе).

$Score_{2}$ – оценка за выполнение заданий на практиках. Принимает значение от 0 до 10. Результат Score_2 определяется как среднее арифметическое оценок за выполнение практик. Оценка за задание на практику ставится исходя из качества выполнения работы (0 - работа не выполнена, 8 - полное выполнение **и объяснение** задания по примеру, 9-10 полное выполнение задания и дополнительных требований к нему.

$Score_{3}$ – оценка за экзамен(финальное тестирование). Принимает значение от 0 до 10. Экзамен проводится в форме тестирования, содержащего вопросы по теории и вычислительные задания. Оценка зависит от процента правильных ответов. 

$Score_{add}$ – дополнительные баллы. Может принимать от 0 до 10 баллов. ставится за использование материалов курса в исследовательской и прикладной работе (подготовка публикаций, выступлений, участие в конкурсах) по тематике курса. Конкретный балл выставляется в зависимости от достигнутого результата и уровня журнала/конференции/конкурса.
