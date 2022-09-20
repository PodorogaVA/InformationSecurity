# Лабораторная работа №3

# Что нужно было сделать?

Получить практические навыки работы в консоли с атрибутами файлов для групп пользователей.

# Ход работы

- Добавляем гостевого пользователя (видно, что он ранее был добавлен в предыдущей работе): 

  ![Добавление гостевого пользователя](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\1.png)

  *Рис. 1. Добавление гостевого пользователя*

# Ход работы

- Настраиваем пароль для гостевого пользователя:

  ![Настройка пароля для гостевого пользователя](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\2.png)

  *Рис. 2. Настройка пароля для гостевого пользователя*

# Ход работы

- Заходим в суперпользователя root и проделываем то же самое, чтобы разрешить доступ, а также создаём guest2:

  ![Те же действия от root и создание guest2](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\3.png)

  *Рис. 3. Те же действия от root и создание guest2*

# Ход работы

- Добавляем гостевого пользователя в группу guest:

  ![Добавление гостевого пользователя в группу guest](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\4.png)

  *Рис. 4. Добавление гостевого пользователя в группу guest*

# Ход работы

- В разных терминалах осуществили вход в систему от пользователей guest и guest2:

  ![Вход от guest и guest2](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\5.png)

  *Рис. 5. Вход от guest и guest2*

# Ход работы

- Для обоих пользователей командой pwd определили директорию, в которой находимся:

  ![Определение директории](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\6.png)

  *Рис. 6. Определение директории*

# Ход работы

- Уточняем имя нашего пользователя, его группу, а также группы, куда входит пользователь, командой id и groups:

  ![Уточнение для guest с помощью id и groups](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\7.1.png)

  *Рис. 7.1. Уточнение для guest с помощью id и groups*

# Ход работы

- ![Уточнение для guest2 с помощью id и groups](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\7.2.png)

  *Рис. 7.2. Уточнение для guest2 с помощью id и groups*

  В результате командой groups и id -Gn получаем одинаковый вывод - названия групп пользователей, а id -G получаем число - id группы пользователей.

# Ход работы

- Просмотрим файл /etc/group командой cat /etc/group:

  ![Просмотр файла](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\8.1.png)

  *Рис. 8.1. Просмотр файла*

# Ход работы

- ![Мои пользователи](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\8.2.png)

  *Рис. 8.2. Мои пользователи*

# Ход работы

- От имени пользователя guest2 выполним регистрацию пользователя guest2 в группе guest:

  ![Регистрация guest2 в guest](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\9.png)

  *Рис. 9. Регистрация guest2 в guest*

# Ход работы

- От имени пользователя guest изменим права директории /home/guest, разрешив все действия для пользователей группы:

  ![Изменение прав директории /home/guest](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\10.png)

  *Рис. 10. Изменение прав директории /home/guest*
  

# Ход работы

- От имени пользователя guest снимем с директории /home/guest/dir1 все атрибуты, потом будем менять атрибуты и смотреть, что происходит с доступом:

  ![Снятие атрибутов с dir1](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.1.png)

  *Рис. 11.1. Снятие атрибутов с dir1*
  
  ![Определение атрибутов](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.2.png)
  
  *Рис. 11.2. Определение атрибутов*

# Ход работы

- ![Проверка тестовым документом](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.3.png)

  *Рис. 11.3. Проверка тестовым документом*

  ![Изменение атрибутов и очередная проверка](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.4.png)
  
  *Рис. 11.4. Изменение атрибутов и очередная проверка*

# Ход работы

- ![Изменение атрибутов и очередная проверка](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.5.png)

  *Рис. 11.5. Изменение атрибутов и очередная проверка*
  
  ![Изменение атрибутов и очередная проверка](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.6.png)
  
  *Рис. 11.6. Изменение атрибутов и очередная проверка*

# Ход работы

- ![Изменение атрибутов и очередная проверка](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.7.png)

  *Рис. 11.7. Изменение атрибутов и очередная проверка*

  ![Изменение атрибутов и очередная проверка](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.8.png)

  *Рис. 11.8. Изменение атрибутов и очередная проверка*

# Ход работы

- ![Изменение атрибутов и очередная проверка](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.9.png)

  *Рис. 11.9. Изменение атрибутов и очередная проверка*

  ![Изменение атрибутов и очередная проверка](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.10.png)

  *Рис. 11.10. Изменение атрибутов и очередная проверка*

# Ход работы

- Таблица атрибутов![Таблица атрибутов](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.11.jpg)

  *Рис. 11.11. Таблица атрибутов*

# Ход работы

- Таблица минимальных прав![Таблица минимальных прав](D:\Файлы с диска С\Учеба\Информационная безопасность\Lab 3\report\image\11.12.jpg)

  *Рис. 11.12. Таблица минимальных прав*

# Вывод

В ходе лабораторной работы я получил практические навыки работы с атрибутами файлов для групп пользователей в условиях ОС Linux.

# Спасибо за внимание!