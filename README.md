# Задача 1:
 - Установил MariaDB и совершил первоначальную настройки
 - С помощью скрипта mariadb-secure-installation устранил уязвимости безопасности
 
 <img width="1074" height="595" alt="image" src="https://github.com/user-attachments/assets/5ed259c3-66b1-4548-b72c-98ff587d780a" />

 - Создал базу данных LAB внутри нее три таблицы groups,analysis,orders

 <img width="603" height="578" alt="image" src="https://github.com/user-attachments/assets/a824a23a-b46f-49ab-81e5-8d86dde214c9" />
 
 - Заполнил таблицы данными и запросом получил анализы в промежутке между 5 числом октября и 8 до конца недели

 <img width="706" height="667" alt="image" src="https://github.com/user-attachments/assets/746e55bf-f64c-45e6-88a3-cc069e9470ee" />
|
 <img width="972" height="215" alt="image" src="https://github.com/user-attachments/assets/ec35bca2-478f-4a44-a84b-a0114a7d5a63" />

# Задача 2:
 - Создал базу данных university
 - Создал две таблицы Students и courses и заполнил их
 - Чтоб применить левое соединение использовал 3 таблицу StudentsCourses
 - Само по себе левое подразумевает вытягивание данных из левой таблицы и даже если в правой таблице нет сопоставлений выводится null
 - Написал запрос через левое соединение по id

# Задача 3:
 - Сделал дамп базы sudo mysqldump -u root -p LAB > BackupsDB/28.04.2026-dump.sql и проверил что дамп реально сделался
 
 <img width="733" height="725" alt="image" src="https://github.com/user-attachments/assets/08e8070a-e6f1-4d73-a0f5-d17fc6eda5a7" />

 - Добавил одну строку в orders неверную с 2028 годом и сохранил (изменил базу)

 <img width="727" height="580" alt="image" src="https://github.com/user-attachments/assets/a67f2c63-5cff-439f-a526-543b79ded804" />

 - Восставновил ранее созданный дамп mysql -u root -p LAB < BackupsDB/28.04.2026-dump.sql что и проверил сразу же

 <img width="870" height="719" alt="image" src="https://github.com/user-attachments/assets/b622e875-11f2-4cb5-9625-e8b82e62cb3e" />

 - Написал скрипт который автоматический создает бекапы с периодичностью в 1 минуту

 <img width="1235" height="767" alt="image" src="https://github.com/user-attachments/assets/cd57def9-614c-4847-891f-c11e38f5917a" />
