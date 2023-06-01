## Лабораторная работа 4
*Дисциплина:* Тестирование ПО

*Вариант:* системный

*Отчёт:* [report.pdf](https://github.com/ANegrash/TPO_lab4/blob/main/report.pdf)

### Задание
С помощью программного пакета Apache JMeter провести нагрузочное и стресс-тестирование веб-приложения в соответствии с вариантом задания.

В ходе нагрузочного тестирования необходимо протестировать 3 конфигурации аппаратного обеспечения и выбрать среди них наиболее дешёвую, удовлетворяющую требованиям по максимальному времени отклика приложения при заданной нагрузке (в соответствии с вариантом).

В ходе стресс-тестирования необходимо определить, при какой нагрузке выбранная на предыдущем шаге конфигурация перестаёт удовлетворять требованиями по максимальному времени отклика. Для этого необходимо построить график зависимости времени отклика приложения от нагрузки.

#### Webapp properties:
- First hardware configuration ($ 2400) URL - http://stload.se.ifmo.ru:8080?token=468486620&user=2023825522&config=1;
- Second hardware configuration ($ 4500) URL - http://stload.se.ifmo.ru:8080?token=468486620&user=2023825522&config=2;
- Third hardware configuration ($ 6400) URL - http://stload.se.ifmo.ru:8080?token=468486620&user=2023825522&config=3;
- Maximum parallel sessions count - 9;
- Load average (requests per minute; per session) - 40;
- Maximum request processing timeout - 710 ms.

#### Как подключиться?
```
ssh -L 8888:stload.se.ifmo.ru:8080 sXXXXXX@se.ifmo.ru -p 2222
```

После чего необходимые данные будут доступны по адресу:

`http://127.0.0.1:8888?token=<your_token>&user=<user>&config=<config_number>`

[Конфигурация для JMeter](https://github.com/ANegrash/TPO_lab4/blob/main/config.jmx)

Примечание: у меня вышло подключиться только на Linux, т.к. на Windows не работал OpenSSH.
