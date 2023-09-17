## HW_28.1.ИТОГОВЫЙ ПРОЕКТ ПО АВТОМАТИЗАЦИИ ТЕСТИРОВАНИЯ
QAP-1035
### Объект тестирования: [Ростелеком IT](https://b2c.passport.rt.ru)

→ [Требования по проекту (.doc)](https://docs.google.com/document/d/18DggAU8-W1-TEcbM9WgnG_L3YDF8uFKQrAS7rjS9w2g/edit?usp=sharing)
___
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
Сформированы тест-кейсы и отчёты о дефектах: [смотреть здесь](https://docs.google.com/spreadsheets/d/1aZWL0gVnk_XShbtlnsnQKIZt6Dn730fDVJlYXYJ-h-U/edit?usp=sharing)
___
Для тестирования интерфейса были использованы:

✅разбиение на классы эквивалентности

✅анализ граничных значений

✅тестирование состояний и переходов

___
**В корневой директории расположены:**
* файл conftest.py - содержит фикстуру для инициализации браузера и закрытия сессии после завершения теста
* файл requirements.py - список внешних зависимостей
* pytest.ini - регистрация маркеров

**В директории /pages расположены:**
* Base_APP.py - необходимые методы для работы с webdriver
* locators.py - локаторы web-элементов
* RandomEmail_APP.py - GET-запросы к временному почтовому ящику на сайте [1secmail.com](https://www.1secmail.com/) для получения валидного E-mail и кода для регистрации на странице/восстановления пароля
* RosTeleCom_APP.py - необходимые методы для работы с web-элементами на страницах авторизации, регистрации и восстановления пароля
* settings.py - исходные статические данные и учётные данные, используемые в проведении тестирования

**В директории /tests расположены:**
* test_positive_reg_page.py - автоматизированные тесты с позитивными сценариями страницы регистрации
* test_positive_auth_page.py - автоматизированные тесты с позитивными сценариями страницы авторизации
* test_positive_new_pass_page.py - автоматизированные тесты с позитивными сценариями страницы восстановления пароля
* test_negative_reg_page.py - автоматизированные тесты с негативными сценариями страницы регистрации
* test_negative_auth_page.py - автоматизированные тесты с негативными сценариями страницы авторизации
* test_negative_new_pass_page.py - автоматизированные тесты с негативными сценариями страницы восстановления пароля

**В директории /tests/screenshots** расположены графические файлы с фиксацией результата тестирования
___

#### Тесты настроены на запуск через Run!

Окружение: Windows 11 Домашняя версия 21H2

Браузер: Google Chrome 112.0.5615.138 (64-bit)



***
**:bookmark_tabs: В корневом каталоге проекта содержаться:**
* [conftest.py](https://github.com/mafaga00/Final_project_QAP1031/blob/master/conftest.py) - содержит условия для выполнения тестов.
* [pytest.ini](https://github.com/mafaga00/Final_project_QAP1031/blob/master/pytest.ini) - содержит указание на автоматическую генерацию html-отчета.
* [README.md](https://github.com/mafaga00/Final_project_QAP1031/blob/master/README.md) - содержит информацию в целом о проекте.
* [requirements.txt](https://github.com/mafaga00/Final_project_QAP1031/blob/master/requirements.txt) - содержит все библиотеки и зависимости проекта.
***
**:bookmark_tabs: Директория pages содержит:**
* [base_page.py](https://github.com/mafaga00/Final_project_QAP1031/blob/master/pages/base_page.py) - содержит все общие методы и утилиты для всех страниц.
* [auth_page.py](https://github.com/mafaga00/Final_project_QAP1031/blob/master/pages/auth_page.py) - содержит специфичные методы и утилиты для страницы авторизации.
***
**:bookmark_tabs: Директория tests содержит:**
* [assets](https://github.com/mafaga00/Final_project_QAP1031/blob/master/tests/assets) - содержит CSS-стили для html-отчёта.
* [base_test.py](https://github.com/mafaga00/Final_project_QAP1031/blob/master/tests/base_test.py) - содержит базовый тестовый класс.
* [test_auth.py](https://github.com/mafaga00/Final_project_QAP1031/blob/master/tests/test_auth.py) - содержит автотесты для страницы авторизации.
***
**:bookmark_tabs: Директория utilities содержит:**
* [locators.py](https://github.com/mafaga00/Final_project_QAP1031/blob/master/utilities/locators.py) - содержит локаторы страницы.
* [test_data.py](https://github.com/mafaga00/Final_project_QAP1031/blob/master/utilities/test_data.py) - содержит все данные для проверок авторизации.
***



→ [Тест-кейсы (.excel)](https://docs.google.com/spreadsheets/d/18tZqTErSz8f-QQOMp14v2XuCOlpA57ZgK445Zc1rid0/edit?usp=sharing)

→ [Баг-репорты (.excel)](https://docs.google.com/spreadsheets/d/1sQ3JHZdVSOD9qhUG3C5WgKHDRY0SQaYjlopVjvIEBmc/edit?usp=sharing)

### При разработке тест-кейсов были применены следующие техники тест-дизайна: 
 
* эквивалентное разбиение
* анализ граничных значений
* предугадывание ошибок
* [диаграмма перехода состояния (.png)](https://drive.google.com/file/d/1wNGMKdT0kgPsPadnHex9vZ1TwRDAKOfT/view?usp=sharing)


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


