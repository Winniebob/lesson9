Проблематика: имеется несколько микросервисов (проектов) на spring-boot: reader-service, book-service, issue-service, ...
Хочется, чтобы в каждом из этих проектов работал аспект-таймер, замеряющий время выполнения метода бина, помеченного аннотацией @Timer (см. дз к уроку 8)

Решение: создать стартер, который будет инкапсулировать в себе аспект и его автоматический импорт в подключающий проект.
То есть:
## 1. Пишем стартер, в котором задекларирован аспект и его работа
![image](https://github.com/Winniebob/lesson9/assets/131287620/651f16e0-30b4-4abe-ad7a-13034c56aba7)


##2. Подключаем стартер в reader-service, book-service, issue-service
![image](https://github.com/Winniebob/lesson9/assets/131287620/0e7d9932-1b74-4526-808c-0cee723e9dd5)
![image](https://github.com/Winniebob/lesson9/assets/131287620/568ad667-2205-4618-b874-d88bdfbb8135)
![image](https://github.com/Winniebob/lesson9/assets/131287620/803eebe8-95ea-4830-952f-9fd60638d3ed)


##3. Проверяем работу использую аннотацию Timer над каким то методом или классом
![image](https://github.com/Winniebob/lesson9/assets/131287620/8d72f546-c167-4e08-b834-1af016bd3a4e)
![image](https://github.com/Winniebob/lesson9/assets/131287620/e8630092-8dea-46c8-8aa8-d5b7ba3e6874)
![image](https://github.com/Winniebob/lesson9/assets/131287620/e9dfcc29-623d-4853-9275-a813ec9b70f7)
