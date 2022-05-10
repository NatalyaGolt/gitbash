# gitbash
### 1. Посмотреть где я:
    pwd

### 2. Создать папку:
    mkdir folder_name_1

### 3. Зайти в папку:
    cd folder_name_1

### 4. Создать 3 папки:
    mkdir folder_name_2 folder_name_3 folder_name_4

### 5. Зайти в любую папку:
    cd folder_name_4

### 6. Создать 5 файлов (3 txt, 2 json):
    touch file_1.txt file_2.txt file_3.txt file_4.json file_5.json

### 7. Создать 3 папки:
    mkdir folder_name_5 folder_name_6 folder_name_7

### 8. Вывести список содержимого папки:
    ls -la (со скрытыми файлами в столбец),
    ls -l (без скрытых файлов в столбец),
    ls -a (со скрытыми файлами в строчку)

### 9. Открыть любой txt файл:
    cat >> file_1.txt

### 10. Написать туда что-нибудь, любой текст:
    Hello, world!

    welcome

    see you!

### 11. Сохранить и выйти:
    ctrl+c

### 12. Выйти из папки на уровень выше:
    cd ..

### 13. Переместить любые 2 файла, которые вы создали, в любую другую папку:
    mv folder_name_4/file_1.txt folder_name_4/file_2.txt folder_name_4/folder_name_5

### 1. Скопировать любые 2 файла, которые вы создали, в любую другую папку:
    cp folder_name_4/folder_name_5/file_1.txt folder_name_4/folder_name_5/file_2.txt folder_name_4

### 15. Найти файл по имени:
    find folder_name_4/file_4.json

### 16. Просмотреть содержимое в реальном времени (команда grep). Изучить как она работает: 
### Делает поиск по слову (символу) в файле.
### Чтобы в результат попала инфа после изменения файла, нужно сохранить файл.
### Чтобы в результат попала последняя строчка, необходимо завершить ее в файле интером (и не забыть сохранить файл).

    tail -f folder_name_4/file_1.txt |grep !
### Результат: 
    Hello, world!
    see you!

### 17. Вывести несколько первых строк из текстового файла:
    head -3 folder_name_4/file_1.txt
### Результат:
    Hello, world!

    welcome

### 18. Вывести несколько последних строк из текстового файла:
    tail -3 folder_name_4/file_1.txt
### Результат:
      
      
    see you!

### 19. Просмотреть содержимое длинного файла (команда less). Изучите как она работает:
### Команда используется для постраничного просмотра больших текстовых файлов
    less folder_name_4/file_1.txt
### Результат: в гитбаш открывается файл
### Для выхода использовать q

### 20. Вывести дату и время:
    date +"%d.%m.%y %H:%M:%S"
### Результат:
    15.04.22 22:38:58

### 21. Отправить http запрос на сервер http://162.55.220.72:5005/terminal-hw-request
    curl 'http://162.55.220.72:5005/terminal-hw-request'
### Ответ сервера:
    {"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1":"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}
### Отправить второй запрос:
    $ curl 'http://162.55.220.72:5005/get_method?name=Natalya&age=30'
### Ответ от сервера:
    ["Natalya","30"]

### 22. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13:

- Удалить все созданные ранее файлы и папки

- Создать файл:

        cat > automatization.sh
        cd folder_name_1
        mkdir folder_name_2 folder_name_3 folder_name_4
        cd folder_name_4
        touch file_1.txt file_2.txt file_3.txt file_4.json file_5.json
        mkdir folder_name_5 folder_name_6 folder_name_7
        ls -la
        mv /c/Users/user/!folder_name/folder_name_1/folder_name_4/{file_1.txt,file_2.txt} /c/Users/user/!folder_name/folder_name_1/folder_name_4/folder_name_5/

    ### ctrl+c - для выхода из редактирования

- Запустить файл:
  
        bash automatization.sh

### Результат:
    total 8
    drwxr-xr-x 1 user 197121 0 Apr 15 22:16 .
    drwxr-xr-x 1 user 197121 0 Apr 15 22:16 ..
    -rw-r--r-- 1 user 197121 0 Apr 15 22:16 file_1.txt
    -rw-r--r-- 1 user 197121 0 Apr 15 22:16 file_2.txt
    -rw-r--r-- 1 user 197121 0 Apr 15 22:16 file_3.txt
    -rw-r--r-- 1 user 197121 0 Apr 15 22:16 file_4.json
    -rw-r--r-- 1 user 197121 0 Apr 15 22:16 file_5.json
    drwxr-xr-x 1 user 197121 0 Apr 15 22:16 folder_name_5
    drwxr-xr-x 1 user 197121 0 Apr 15 22:16 folder_name_6
    drwxr-xr-x 1 user 197121 0 Apr 15 22:16 folder_name_7