1. Посмотреть где я
```bash
pwd
```
2. Создать папку
```bash
mkdir fld

или

mkdir -p fld/[имя вложенной папки]
(создание полной структуры подкаталогов)
```
3. Зайти в папку
```bash
cd fld

или

cd !$ 
(зайти в только что созданную папку)
```
4. Создать 3 папки
```bash
mkdir fld_{1,2,3}
```
5. Зайти в любую папку
```bash
cd fld_1
```
6. Создать 5 файлов (3 txt, 2 json)
```bash
touch doc_{1,2,3}.txt docum_{1,2}.json
```
7. Создать 3 папки
```bash
mkdir fld_1_{1,2,3}
```
8. Вывести список содержимого папки
```bash
ls   или   ls -la   или   ll
```
9. Открыть любой txt-файл
```bash
vim doc_1.txt
```
10. Написать туда любой текст
```bash
Insert    (вход в режим редактирования)
```
11. Сохранить и выйти
```bash
Esc       (выход из режима редактирования)

:wq + Enter
```
12. Выйти из папки на уровень выше
```bash
cd ..     (на два уровня выше   cd ../..)
```
13. Переместить любые 2 созданные файла в другую папку
```bash
mv fld_1/doc_{1,3}.txt fld_2/
```
14. Скопировать любые 2 файла в другую папку
```bash
cp fld_2/doc_{1,3}.txt fld_1/fld_1_3/
```
15. Найти файл по имени
```bash
find -name docum_1.json
```
16. Просмотреть содержимое файла в реальном времени
```bash
tail -f ./fld_1/doc_1.txt

Ctrl+C   (для окончания просмотра)
```
Простой просмотр содержимого файла
```bash
tail ./fld_1/doc_1.txt
```
Просмотр новых строк файла с конкретным термином, с показом 3 строк до и после искомого термина
```bash
tail -f log_file | grep -C 3 search-term
```
Провести поиск по тексту файла
```bash
grep "[шаблон искомого текста]" ./fld_1/doc_1.txt
```
17. Вывести несколько первых строк из текстового файла
```bash
head -n 4 doc_1.txt
```
18. Вывести несколько последних строк из текстового файла
```bash
tail -n 4 doc_1.txt
```
19. Посмотреть содержимое длинного файла
```bash
less doc_1.txt
q (для окончания просмотра)

или

less +F doc_1.txt
Ctrl+C
q  (для окончания просмотра)
```
20. Вывести дату и время
```bash
date

date -u (UTC время по Гринвичу)
```
21. Отправить http-запрос на сервер http://162.55.220.72:5005/terminal-hw-request
```bash
curl http://162.55.220.72:5005/terminal-hw-request
curl "http://162.55.220.72:5005/get_method?name=(Alena)&age=(21)"
```
22. Написать скрипт автоматического выполнения пунктов 3, 4, 5, 6, 7, 8, 13
```bash
Создать файл [имя файла].sh

В первой строке файла указать путь  #! + [путь к bash] - (это для Windows):  
#!/bin/bash

В остальных строках файла записать команды скрипта:

cd fld
mkdir fld_{1,2,3}
cd fld_1
touch doc_{1,2,3}.txt docum_{1,2}.json
mkdir fld_1_{1,2,3}
ls -la
mv doc_{1,3}.txt fld_1_1/

Команда запуска скрипта в консоли:
sh [имя файла].sh
```
или записать все команды в одну строку
```bash
cd fld && mkdir fld_{1,2,3} && cd fld_1 && touch doc_{1,2,3}.txt docum_{1,2}.json && mkdir fld_1_{1,2,3} && ls -la && mv doc_{1,3}.txt fld_1_1/
```

