Разное
------

Не вижу
--------

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/897bf936-bb0a-4fb2-9429-b635ac0ffe57)

Скачиваем файл и открываем его в stegsolve и выбираем Stereogram Solver

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/06d68e9b-57b6-46fc-97f2-62238cf3f4ea)

Подбираем смещение и получаем флаг

Discard
--------

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/b798f8a4-b54d-4e4f-b097-65d93fc75834)

Смотрим файл

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/36040802-73b3-45b4-9550-4294a9a79338)

У нас данные в hex. Идём в Кибершефа и пробуем разные варианты шифров, к примеру ROT13 и 47

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/984e4780-6692-47b3-80b0-66f6229d7377)

И ROT47 нам даёт результат

Переходим по ссылке в discord и присоединяемся к каналу CTF

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/28cc8e14-5d26-4ee1-83fd-c9658c1a0ac7)

В этом канале куча других каналов, нам предстоит найти нужный

У нас есть подсказка к таску, смотрим чаты голосовых каналов и находим нужный чат

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/15e1802c-ab81-4ace-8e71-e306a02f1090)

Скачиваем файл и смотрим содержимое

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/3dd976da-f426-4a49-89e7-1fdd6e43d180)

Далее в hex редакторе смотрим что в файле WoW.img

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/34eb28e6-67c8-480c-9e6f-af0e390e42fd)

Это png картинка, меняем расширение и получаем картинку

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/69218c7c-c7b7-41cc-b5bd-e1702b71d20f)

Проверяем картинку в Aperisolve

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/2afe5cdd-9db4-4bf8-81e2-b4b3a6bbb0f2)

И находим интересный файл в Strings

Скорее всего это пароль, пробуем

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/3ea700fc-8e33-4a46-9a47-b908694babe7)

Видим что Binwalk извлёк скрытые файлы, скачиваем их

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/04f566ba-e65e-4e1c-a664-31295beb4e0d)

Больше всего нам интересен файл WhatLiesInside.txt ,смотрим, что в нём

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/d88f1848-5b6a-43ca-aa38-6501b973cb6f)

Между строк есть необычные пробелы и в тексте часто втречается слово Snow, пробуем утилиту stegsnow и получаем флаг

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/2a7a1467-ca31-4bec-a56c-72fca00b102e)
















