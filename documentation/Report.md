# Отчет о тестировании
## Описание
**Было проведено тестирование сервиса, который взаимодействует с СУБД и API Банка.**

Приложение является веб-сервисом, который предоставляет возможность купить тур по определённой цене с помощью двух способов:
1. Оплата по дебетовой карте
1. Выдача кредита по данным банковской карты

Сначала было проведено исследовательское (ручное) тестирование для ознакомления с проектом.  
Затем были созданы авто-тесты, исходя из **[Плана](https://github.com/Alex-stagemaster/QA_Diploma/blob/master/documentation/plan.md)**

**Тестирование было проведено с использованием двух баз данных - MySQL и PostgreSQL.**

Перечень выявленных ошибок: **[issues](https://github.com/Alex-stagemaster/QA_Diploma/issues)**
## Количество тест-кейсов и % успешных/не успешных
**Количество тест-кейсов - 30, % успешных/неуспешных  70/30 (9 упавших тест-кейсов).**

**Отчет Allure:**

![image](https://user-images.githubusercontent.com/78262386/206032137-82a5a11a-7e13-4aab-8e1a-deb042cdb1fc.png)



## Общие рекомендации:
- Другим способом оформить требования для данного приложения, разработать спецификацию;
- Исправить выявленные дефекты;
- Добавить "тестовые" атрибуты в приложение для повышения устойчивости авто-тестов;
- Заменить предупреждения "Неверный формат" на более информативные.
