# Лабораторная работа №3
# Дисциплина: информационная безопасность
# Студент: Подорога Виктор Александрович

# Цель работы

Получить практические навыки работы в консоли с атрибутами файлов для групп пользователей.

# Выполнение лабораторной работы

1. Добавляем гостевого пользователя (видно, что он ранее был добавлен в предыдущей работе): 

   ![Добавление гостевого пользователя](image/1.png)

   *Рис. 1. Добавление гостевого пользователя*

2. Настраиваем пароль для гостевого пользователя:

   ![Настройка пароля для гостевого пользователя](image/2.png)

   *Рис. 2. Настройка пароля для гостевого пользователя*

3. Заходим в суперпользователя root и проделываем то же самое, чтобы разрешить доступ, а также создаём guest2:

   ![Те же действия от root и создание guest2](image/3.png)

   *Рис. 3. Те же действия от root и создание guest2*

4. Добавляем гостевого пользователя в группу guest:

   ![Добавление гостевого пользователя в группу guest](image/4.png)

   *Рис. 4. Добавление гостевого пользователя в группу guest*

5. В разных терминалах осуществили вход в систему от пользователей guest и guest2:

   ![Вход от guest и guest2](image/5.png)

   *Рис. 5. Вход от guest и guest2*

6. Для обоих пользователей командой pwd определили директорию, в которой находимся:

   ![Определение директории](image/6.png)

   *Рис. 6. Определение директории*

7. Уточняем имя нашего пользователя, его группу, а также группы, куда входит пользователь, командой id и groups:

   ![Уточнение для guest с помощью id и groups](image/7.1.png)

   *Рис. 7.1. Уточнение для guest с помощью id и groups*

   ![Уточнение для guest2 с помощью id и groups](image/7.2.png)

   *Рис. 7.2. Уточнение для guest2 с помощью id и groups*

   В результате командой groups и id -Gn получаем одинаковый вывод - названия групп пользователей, а id -G получаем число - id группы пользователей.

8. Просмотрим файл /etc/group командой cat /etc/group:

   ![Просмотр файла](image/8.1.png)

   *Рис. 8.1. Просмотр файла*

   ![Мои пользователи](image/8.2.png)

   *Рис. 8.2. Мои пользователи*

9. От имени пользователя guest2 выполним регистрацию пользователя guest2 в группе guest:

   ![Регистрация guest2 в guest](image/9.png)

   *Рис. 9. Регистрация guest2 в guest*

10. От имени пользователя guest изменим права директории /home/guest, разрешив все действия для пользователей группы:

    ![Изменение прав директории /home/guest](image/10.png)

    *Рис. 10. Изменение прав директории /home/guest*

    Расширенные атрибуты увидеть не удалось - гостевому пользователю отказано в доступе.

11. От имени пользователя guest снимем с директории /home/guest/dir1 все атрибуты, потом будем менять атрибуты и смотреть, что происходит с доступом:

    ![Снятие атрибутов с dir1](image/11.1.png)

    *Рис. 11.1. Снятие атрибутов с dir1*

    ![Определение атрибутов](image/11.2.png)

    *Рис. 11.2. Определение атрибутов*

    ![Проверка тестовым документом](image/11.3.png)

    *Рис. 11.3. Проверка тестовым документом*

    ![Изменение атрибутов и очередная проверка](image/11.4.png)

    *Рис. 11.4. Изменение атрибутов и очередная проверка*

    ![Изменение атрибутов и очередная проверка](image/11.5.png)

    *Рис. 11.5. Изменение атрибутов и очередная проверка*

    ![Изменение атрибутов и очередная проверка](image/11.6.png)

    *Рис. 11.6. Изменение атрибутов и очередная проверка*

    ![Изменение атрибутов и очередная проверка](image/11.7.png)

    *Рис. 11.7. Изменение атрибутов и очередная проверка*

    ![Изменение атрибутов и очередная проверка](image/11.8.png)

    *Рис. 11.8. Изменение атрибутов и очередная проверка*

    ![Изменение атрибутов и очередная проверка](image/11.9.png)

    *Рис. 11.9. Изменение атрибутов и очередная проверка*

    ![Изменение атрибутов и очередная проверка](image/11.10.png)

    *Рис. 11.10. Изменение атрибутов и очередная проверка*

    ![Таблица атрибутов](image/11.11.jpg)

    *Рис. 11.11. Таблица атрибутов*

    ![Таблица минимальных прав](image/11.12.jpg)

    *Рис. 11.12. Таблица минимальных прав*

# Вывод

В ходе лабораторной работы я получил практические навыки работы с атрибутами файлов для групп пользователей в условиях ОС Linux.