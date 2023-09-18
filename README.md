## HW_28.1.ИТОГОВЫЙ ПРОЕКТ ПО АВТОМАТИЗАЦИИ ТЕСТИРОВАНИЯ
QAP-1035
### Объект тестирования: [Ростелеком IT](https://b2c.passport.rt.ru)

→ [Требования по проекту (.doc)](https://docs.google.com/document/d/18DggAU8-W1-TEcbM9WgnG_L3YDF8uFKQrAS7rjS9w2g/edit?usp=sharing)

**Заказчик передал вам следующее задание:**

1. Протестировать требования.
2. Разработать тест-кейсы (не менее 15). Необходимо применить несколько техник тест-дизайна.
3. Провести автоматизированное тестирование продукта (не менее 20 автотестов). Заказчик ожидает по одному автотесту на каждый написанный тест-кейс. Оформите свой набор автотестов в GitHub.
4. Оформить описание обнаруженных дефектов. Во время обучения вы работали с разными сервисами и шаблонами, используйте их для оформления тест-кейсов и обнаруженных дефектов. (если дефекты не будут обнаружены, то составить описание трех дефектов)

**Ожидаемый результат**

1. Перечислены инструменты, которые применялись для тестирования.

   * Почему именно этот инструмент и эту технику.
   * Что им проверялось.
   * Что именно в нем сделано.
   
2. К выполненному заданию прикреплены:

   * Набор тест-кейсов;
   * Набор автотестов на GitHub. Обратите внимание, что в репозитории должен находиться файл README.md, где будет описано, что именно проверяют данные тестовые сценарии и какие команды необходимо выполнить для запуска тестов. Описанные команды должны работать на любом компьютере с установленными Python3 и PyTest;
   * Описание оформленных дефектов.

→ [Протестированные требования (.doc)](https://docs.google.com/document/d/1CGkBrCJ-5bS-VqMzsyX0Xakinjvp4bG6-4LIPTXHYEs/edit?usp=sharing)

В рамках проекта произведено ручное и автоматизированное тестирование нового интерфейса авторизации в личном кабинете с применением PyTest и Selenium Webdriver

Тесты проверяют:
* Авторизацию в личном кабинете
* Регистрацию в личном кабинете
* Восстановление пароля в личном кабинете
___
Сформированы тест-кейсы и отчёты о дефектах: [смотреть здесь](https://docs.google.com/spreadsheets/d/1045_wAYBXBWABqTyiGLeQmq2eslhoFgMuW6y5fRI29o/edit?usp=sharing)
___
При разработке тест-кейсов были применены следующие техники тест-дизайна:

✅разбиение на классы эквивалентности

✅анализ граничных значений

✅предугадывание ошибок
___
#### Тесты настроены на запуск через Run!

Окружение: Windows 11 Pro

Браузер: Google Chrome Версия 117.0.5938.89 (Официальная сборка), (64 бит)
***
**В корневом каталоге проекта содержаться:**
* [conftest.py](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/conftest.py)- содержит условия для выполнения тестов.
* [pytest.ini](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/pytest.ini) - содержит указание на автоматическую генерацию html-отчета.
* [README.md](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/README.md) - содержит информацию в целом о проекте.
* [requirements.txt](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/requirements.txt) - содержит все библиотеки и зависимости проекта.
***
**Директория pages содержит:**
* [base_page.py](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/pages/base_page.py) - содержит все общие методы и утилиты для всех страниц.
* [auth_page.py](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/pages/auth_page.py) - содержит специфичные методы и утилиты для страницы авторизации.
***
**Директория tests содержит:**
* [assets](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./tree/master/tests/assets) - содержит CSS-стили для html-отчёта.
* [base_test.py](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/tests/base_test.py) - содержит базовый тестовый класс.
* [test_auth.py](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/tests/test_auth.py) - содержит автотесты для страницы авторизации.
***
**Директория utilities содержит:**
* [locators.py](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/utilities/locators.py) - содержит локаторы страницы.
* [test_data.py](https://github.com/Anzhylik/HW_28_Final_project_Rostelecom_Ryabinina_A.M./blob/master/utilities/test_data.py) - содержит все данные для проверок авторизации.
***
### Инструменты, которые применялись для тестирования.

* Для тестирования сайта был использован 
интсрумент [Selenium](https://www.selenium.dev/).
* Специальный тестовый фреймворк [Pytest](https://docs.pytest.org/).
* Плагин для pytest, который генерирует HTML-отчет по результатам тестов [pytest-html](https://pytest-html.readthedocs.io/en/latest/).
* Опционально можете установить плагин [allure-pytest](https://pypi.org/project/allure-pytest/) и скачать для неё [командную строку](https://repo.maven.apache.org/maven2/io/qameta/allure/allure-commandline/) для генерации красивых html-отчётов.
* Для определения локаторов использовались 
следующие инструменты: [DevTools](https://developer.chrome.com/docs/devto), [ChroPath](https://chrome.google.com/webstore/detail/chropath/ljngjbnaijcbncmcnjfhigebomdlkcjo).

### Запуск тестов:
* установить все библиотеки и зависимости: `pip install -r requirements.txt`.
* убедитесь что у вас присутствуют основные браузеры для тестирования - в файле conftest.py у фикстуры initialize_driver можете изменить браузер.
* запустить тесты: `pytest tests/test_auth.py`.
* запустить один тест: `pytest tests/test_auth.py::TestAuth::название_нужного_теста`.

### P.S.
Вследствие того, что для тестирования предоставлена продуктовая среда, была добавлена фикстура для пропуска тестов если на странице присутствует капча. Рекомендуется запускать не более 2-3 тестов, связанных с авторизацией, чтобы избежать появление капчи.

Если возникли проблемы с кодировкой html-отчёта - настройте кодировку в вашей IDE.


