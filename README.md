# PPO

## 1. Название
Система управление заказами для металлопрокатного завода

## 2. Краткое описание
Приложение для управления заказами на металлопрокатном заводе. Необходимо создать возможность создания и отслеживания прогресса заказа. Кроме того, необходимо предоставить пользователю возможность просмотра доступности материалов на складе (в том числе необходимых для производства конкретного заказа).

## 3. Краткое описание предметной области
Система менеджмента заказов для предприятия

## 4. Краткий анализ аналогичных решений по 3 критериям (1 таблица)
| Название |Тип Приложения|Цена|Возможность кастомизации| 
|---------|------------|------|-----------------------|
| 1С Предприятие | Desktop | 621 руб./рабочее место | + |
| РосБизнесСофт WMS| Web | 815 руб./рабочее место/месяц | - |
| KardexRemstar WMS | Комплексная модульная система | от 400 000 руб.  | + |

## 5. Краткое обоснование целесообразности и актуальности проекта (1 абзац)
В своё время мне приходилось работать на металлопрокатном заводе и львиную долю времени отнимал поиск материалов на складе, отслеживание прогресса заказа, а также поиск всех позиций готового заказа. Данная программа должна помочь оптимизировать производственный процесс

## 6. Use-Case - диаграмма; 
![alt text for screen readers](/img/use_case.png).


## 7. ER-диаграмма сущностей (не путать с диаграммой БД – диаграмма сущность-связь не приземлена на конкретную СУБД и показывает сущности системы); 
![alt text for screen readers](/img/er.png).

## 8. Пользовательские сценарии (в текстовом виде);
Для добавления заказа менеджер заходит в окно добавления заказа и заполняет форму. При корректном значении всех полей заказ будет добавлен в базу и получит статус "Ожидает"

Работник производства, указывает что начата работа над заказом (статус меняется на "В производстве") и по мере выполнения указывает количество выполненных позиций, а также их положение на складе. 

В любой момент пользователь может проверить имеющиеся на складе материалы (в главном окне) либо же доступность материалов для выполнения заказа (в окне заказов).

После того, как все позиции заказа были отмечены работником как произведённые, его статус меняется на "Передан в доставку".

## 9. Формализация бизнес-правил (в виде BPMN).
![alt text for screen readers](/img/bpmn.png).

## 10. Описание типа приложения и выбранного технологического стека 
Front-end: Qt

Back-end: C++

DB: PostgreSQL

## 11. Верхнеуровневое разбиение на компоненты (в следующих лабах сможете уточнить)
![alt text for screen readers](/img/components.svg).

## 12. UML диаграммы классов для двух отдельных компонентов - компонента доступа к данным и компонента с бизнес-логикой
### UML-диаграмма компонента доступа к данным 
![alt text for screen readers](/img/data_uml.svg).
