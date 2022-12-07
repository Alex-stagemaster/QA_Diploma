# Дипломный проект
### Дипломный проект представляет собой автоматизацию тестирования комплексного сервиса, взаимодействующего с СУБД и API Банка.
#### Приложение представляет собой веб-сервис, который предоставляет возможность купить тур по определённой цене с помощью двух вариантов:
- оплата по дебетовой карте
- выдача кредита по данным банковской карты

#### При работе над данным проектом были созданы сопутствующие документы:
1. [План автоматизации](https://github.com/Alex-stagemaster/QA_Diploma/blob/master/documentation/plan.md)
2. [Отчет о проведенном тестировании](https://github.com/Alex-stagemaster/QA_Diploma/blob/master/documentation/Report.md)
3. [Отчет о проведённой автоматизации тестирования](https://github.com/Alex-stagemaster/QA_Diploma/blob/master/documentation/Summary.md)

#### Требуемое окружение:
- установленный Docker;
- убедиться, что порты 8080, 9999 и 5432 или 3306 открыты;

#### Инструкция:
1. Скачайть архив;

2. Запустить контейнер, в котором разворачивается БД `docker-compose up -d --force-recreate`

3. Убедиться, что БД готова к работе (просмотр логов `docker-compose logs -f <applicationName>` (mysql или postgres)
4. Запустить SUT во вкладке Terminal Intellij IDEA командой:
   `java -jar artifacts/aqa-shop.jar`
5. Для запуска авто-тестов в Terminal Intellij IDEA открыть новую сессию и ввести команду:
   `./gradlew clean test allureReport -Dheadless=true`
   где:
   `allureReport` - подготовка данных для отчета Allure;
   `-Dheadless=true` - запускает авто-тесты в headless-режиме (без открытия браузера).
6. Для просмотра отчета Allure в терминале ввести команду:
   `./gradlew allureServe`