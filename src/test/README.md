e2e тесты пишутся по шаблону. 
Нужно наследоваться от AbstractTestContainers, в нем вся конфигурация по поднятию и миграции контейнера postgres.
После каждого теста все данные в таблице очищаются.

Есть пример написания теста: TestControllerTest

Есть две вспомогательные функции:
1. loadAsString. Используем для парсинга тела запроса из json
2. executeSqlScript. Если нужно заполнить базу тестовыми данными.