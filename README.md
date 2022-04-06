1) Посмотреть где я 

        • pwd 

2) Создать папку 

        • mkdir papka_1

3) Зайти в папку 

        • cd papka_1

4) Создать 3 папки 

        • mkdir papka_11 papka_22 papka_33

5) Зайти в любую папку 

        • cd papka_11

6) Создать 5 файлов (3 txt, 2 json) 
       
        • touch file_1.txt file_2.txt file_3.txt file_4.json file_5.json

7) Создать 3 папки 

         • mkdir folder_1 folder_2 folder_3

8. Вывести список содержимого папки 

         • ls -la

9) Открыть любой txt файл 

         • vim file_1.txt I 

10) написать туда что-нибудь, любой текст.

{       "name": "Inna",
        "age": 28,
        "city": "Minsk"
}

11) сохранить и выйти. 

        • Esc+:wq

12) Выйти из папки на уровень выше 

        • cd ..

13) переместить любые 2 файла, которые вы создали, в любую другую папку. 

        • mv papka_11/file_1.txt papka_33/file_1.txt
        • mv papka_11/file_2.txt papka_33/file_2.txt

14) скопировать любые 2 файла, которые вы создали, в любую другую папку. 

        • cp papka_33/file_1.txt papka_11/file_1.txt
        • cp papka_33/file_2.txt papka_11/file_2.txt

15) Найти файл по имени 

         • find -name file_1.txt

16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.
        
         • tail -f file_1.txt
{       "name": "Inna",
        "age": 28,
        "city": "Minsk"
}

         • grep "Inna" file_1.txt
{       "name": "Inna",

17) вывести несколько первых строк из текстового файла

        • head file_1.txt выводит первые 10 по умолчанию
{       {"name": "Inna",
        "age": 28,
        "city": "Minsk"},
        {"name": "Anna",
        "age": 30,
        "city": "Moscow"

Если вывести первые 2 строки

         • head -2 file_1.txt
{       {"name": "Inna",
        "age": 28,

18) вывести несколько последних строк из текстового файла
        
         • tail file_1.txt выводит последние 10 по умолчанию
        "city": "Minsk"},
        {"name": "Anna",
        "age": 30,
        "city": "Moscow"}




}

Если вывести последние 9 строк

         • tail -9 file_1.txt
        "city": "Minsk"},
        {"name": "Anna",
        "age": 30,
        "city": "Moscow"}




}

19) просмотреть содержимое длинного файла (команда less) изучите как она работает.

         • less file_1.txt

         • less -N file_1.txt

20) вывести дату и время 

         • date
Fri Feb 11 15:24:20 RTZ 2022



Задание *
1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request

 curl "http://162.55.220.72:5005/terminal-hw-request"

Ответ:

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   237  100   237    0     0   2853      0 --:--:-- --:--:-- --:--:--  2890{"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1":"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}

Task_1

 curl "http://162.55.220.72:5005/get_method?name="Inna"&age=28"

Ответ: 
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    14  100    14    0     0    147      0 --:--:-- --:--:-- --:--:--   147["Inna","28"]


2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

cat > script.sh << EOF
#!/bin/bash
pwd
mkdir folder_basic
cd folder_basic
mkdir folder_1 folder_2 folder_3
cd folder_3
touch {1text.txt,2text.txt,3text.txt,1json.json,2json.json}
mkdir script_folder1 script_folder2 script_folder3
ls -la
mv {1text.txt,1json.json} ../folder_3/script_folder2

• chmod +x script.sh

• ./script.sh
