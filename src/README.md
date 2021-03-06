# Отчёт о тестировании Credit Card Number Validator

## Краткое описание

<04.03.2021> - <04.03.2021> было проведено тестирование методами:дымовое,функциональности,граничных значений приложения Credit Card Number Validator.

На тестирование затрачено: 1 час

В результате тестирования выявлены следующие дефекты:
* [Валидатор не допускает карты с номером длиной более 16 цифр](https://github.com/jukkty/java1.1/issues/1)
* [Валидатор не допускает карты American Express](https://github.com/jukkty/java1.1/issues/2)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* [Исходный код программы](https://github.com/jukkty/java1.1/blob/master/src/Main.java)

В качестве тестовых данных использовались данные [Сайт генератора номеров кредитных карт](https://www.freeformatter.com/credit-card-number-generator-validator.html):

**VISA**
  * 4532879462821154 - OK
  * 4024007134815264 - OK
  * 4929818183600629085 - FAIL

**MasterCard**
  * 5162203045708339 - OK
  * 5113061034223037 - OK
  * 2720997279341178 - OK

**AMEX**
  * 346071349220552 - FAIL
  * 348683015029642 - FAIL
  * 379255585735486 - FAIL

Тестирование производилось в следующем окружении:
* Windows 10 64 bit
* openjdk version "11.0.10" 2021-01-19
