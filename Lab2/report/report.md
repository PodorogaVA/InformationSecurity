# Лабораторная работа №2
# Дисциплина: информационная безопасность
# Студент: Подорога Виктор Александрович

# Цель работы

Получить практические навыки работы в консоли с атрибутами файлов, закрепить теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux.

# Выполнение лабораторной работы

1. Добавляем гостевого пользователя: 

   ![Добавление гостевого пользователя](image/1.png)

   *Рис. 1. Добавление гостевого пользователя*

2. Настраиваем пароль для гостевого пользователя:

   ![Настройка пароля для гостевого пользователя](image/2.png)

   *Рис. 2. Настройка пароля для гостевого пользователя*

3. Заходим в суперпользователя root и проделываем то же самое, чтобы разрешить доступ:

   ![Те же действия от root](image/3.png)

   *Рис. 3. Те же действия от root*

4. Заходим в гостевого пользователя:

   ![Логин](image/4.png)

   *Рис. 4. Логин*

5. Командой pwd проверяем путь до директории, в которой оказались:

   ![Проверка pwd](image/5.png)

   *Рис. 5. Проверка pwd*

6. Уточняем имя нашего пользователя командой whoami:

   ![Уточнение имени пользователя](image/6.png)

   *Рис. 6. Уточнение имени пользователя*

7. Уточняем имя нашего пользователя, его группу, а также группы, куда входит пользователь, командой id и groups:

   ![Уточнение с помощью id](image/7.png)

   *Рис. 7. Уточнение с помощью id и groups*

   В результате получает одни и те же группы пользователя (в обоих случаях guest)

8. Просмотрим файл /etc/passwd командой cat /etc/passwd:

   ![Просмотр файла](image/8.1.png)

   *Рис. 8.1. Просмотр файла*

   ![Мой пользователь](image/8.2.png)

   *Рис. 8.2. Мой пользователь*

9. Определим существующие в системе директории командой ls -l /home/:

   ![Определение существующих в системе директорий](image/9.png)

   *Рис. 9. Определение существующих в системе директорий*

   Список директорий получен, на директориях установлены права чтения, записи и исполнения, что соответствует атрибуту 700 в таблице.

10. Проверим расширенные атрибуты командой lsattr /home:

    ![Проверка расширенных атрибутов](image/10.png)

    *Рис. 10. Проверка расширенных атрибутов*

    Расширенные атрибуты увидеть не удалось - гостевому пользователю отказано в доступе.

11. Создадим в домашней директории поддиректорию dir1 командой mkdir dir1 и определим атрибуты:

    ![Создание dir1](image/11.1.png)

    *Рис. 11.1. Создание dir1*

    ![Определение атрибутов](image/11.2.png)

    *Рис. 11.2. Определение атрибутов*

12. Снимем с директории dir1 все атрибуты командой chmod 000 dir1 и проверим правильность командой ls -l:

    ![Снятие всех атрибутов и проверка](image/12.png)

    *Рис. 12. Снятие всех атрибутов и проверка*

13. Попытаемся создать в директории dir1 файл file1 командой echo "test" > /home/guest/dir1/file1:

    ![Попытка создания файла](image/13.png)

    *Рис. 13. Попытка создания файла*

    Файл создать не удается, это связано с тем, что у директории dir1 отсутствует право на создание в ней файлов, ее атрибуты 000. 

14. Выполняя команды 14.1 - 14.4, анализируем атрибуты директории и файла в ней:

    ![Обнуление прав директории](image/14.1.png)

    *Рис. 14.1. Обнуляем права директории*

    ![Права на исполнение](image/14.2.png)

    *Рис. 14.2. Выдаем директории право на исполнение*

    ![Права на запись](image/14.3.png)

    *Рис. 14.3. Выдаем директории право на запись*

    ![Права на исполнение и запись](image/14.4.png)

    *Рис. 14.4. Выдаем директории право на исполнение и запись*

    ![Таблица атрибутов](image/14.5.jpg)

    *Рис. 14.5. Таблица атрибутов*

# Вывод

В ходе лабораторной работы я получил практические навыки работы с атрибутами файлов и директории с использованием консоли операционной системы CentOS Linux, а также закрепил теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux.