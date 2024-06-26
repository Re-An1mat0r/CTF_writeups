# CTF_writeups
CTF_writeups

Hackosint2024_bonus_tasks
-------------------------

Криптография
------------
Тык-Тык
--------

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/149f884a-735a-4552-aacc-7e3c1efba952)

По подсказке понимаем, что это шифр Решётки Кардано.

Заменяем символы в шифротексте RB801BWWD7NH89U48T6T1478804W80G049WW согласно подсказкам

Получаем RB_01BWWD{NH_}U4_T$T14{__04W_0G04}WW

Ищем декодер для шифра Кардано

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/cfc65f72-3d57-4335-88c9-f4df45e843fe)

https://merri.cx/enigmator/cipher/grille.html

Решётка у нас 6 х 6 так как в шифротексте 36 символов.
 
Зная формат флага B0NU${ подбираем дырки:

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/29070c28-91c0-4082-b707-442702d8d424)

Получаем B0NU${_H4_4_}T404WW{_1_}

Далее по смыслу скорее всего у нас буква W, проверяем

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/6374b56b-df33-4402-b6e9-6fcd62a7d969)

Пробуя разные 0 получаем

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/cae7e653-9dd5-45fa-8716-dd3f68c573c5)

Получили такой текст B0NU${W0_WH4T_4_1D}T404WW{__1_0} в нём есть слово WH4T это то что нам нужно

Подбираем последний ряд букв и получаем флаг

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/4374db41-ca68-48fb-a587-6b20755dfd16)

Флаг: B0NU${W0W_WH4T_4_GR1D}

SomDef
------

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/2e0298c3-520f-44ef-8d67-1c28745e464d)

Шифротекст:

THECAPTUREFLAGTHECAPTURETHETHEFLAGTHECAPTURETHETHE
CAPTURETHECAPTURETHEFLAGTHECAPTUREFLAGTHECAPTURECAPTURETHEFLAGTHETHETHEFLAGTHECAPTURETHECAPTURETHECAPTURE
CAPTURETHECAPTURECAPTUREFLAGCAPTURECAPTURECAPTUREFLAGTHETHECAPTURE
CAPTURETHECAPTUREFLAGCAPTURETHEFLAGCAPTURECAPTURECAPTUREFLAGTHECAPTURECAPTURE
THETHECAPTURETHEFLAGTHECAPTURETHETHEFLAGTHECAPTUREFLAGCAPTURECAPTURETHE
THETHECAPTURETHEFLAGCAPTURECAPTURECAPTUREFLAGTHECAPTURETHEFLAGCAPTURECAPTUREFLAGTHECAPTUREFLAGCAPTUREFLAGTHECAPTURETHECAPTURETHECAPTURE
CAPTURECAPTUREFLAGCAPTURECAPTURECAPTURECAPTURECAPTUREFLAGTHECAPTURETHEFLAGCAPTURECAPTURETHETHEFLAGCAPTURECAPTURECAPTURECAPTURETHEFLAGCAPTURETHEFLAGCAPTURETHECAPTUREFLAGTHECAPTUREFLAGTHECAPTURETHECAPTURETHECAPTURE

Слово FLAG у нас не повторяется дважды подряд, скорее всего это какой-то разделитель в шифре, предположим что это шифр морзе, значит FLAG у нас пробел, заменяем:

THECAPTURE THECAPTURETHETHE THECAPTURETHETHE
CAPTURETHECAPTURETHE THECAPTURE THECAPTURECAPTURETHE THETHETHE THECAPTURETHECAPTURETHECAPTURE
CAPTURETHECAPTURECAPTURE CAPTURECAPTURECAPTURE THETHECAPTURE
CAPTURETHECAPTURE CAPTURETHE CAPTURECAPTURECAPTURE THECAPTURECAPTURE
THETHECAPTURETHE THECAPTURETHETHE THECAPTURE CAPTURECAPTURETHE
THETHECAPTURETHE CAPTURECAPTURECAPTURE THECAPTURETHE CAPTURECAPTURE THECAPTURE CAPTURE THECAPTURETHECAPTURETHECAPTURE
CAPTURECAPTURE CAPTURECAPTURECAPTURECAPTURECAPTURE THECAPTURETHE CAPTURECAPTURETHETHE CAPTURECAPTURECAPTURECAPTURETHE CAPTURETHE CAPTURETHECAPTURE THECAPTURE THECAPTURETHECAPTURETHECAPTURE

Далее к примеру THE меняем на "." а CAPTURE на "-", заменяем:

.- .-.. .-..
-.-. .- .--. ... .-.-.-
-.-- --- ..-
-.- -. --- .--
..-. .-.. .- --.
..-. --- .-. -- .- - .-.-.-
-- ----- .-. --.. ----. -. -.- .- .-.-.-

Идём в Кибершефа и получаем флаг

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/85a3f3c0-3625-4d73-9aa1-4c5675b89b84)

Флаг: B0NU${M0RZ9NKA}

Билибизяка
----------

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/88a11973-45f6-4009-b4c3-45751a13cbf9)

Идём в Кибершеф

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/86bdf0be-c3c7-40e4-be08-73bb5f5ddb02)

From Binary

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/e838800c-6b87-4cc3-a76a-eed766bdc4bc)

Дальше я спросил Чат гпт

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/c52eeb3c-3922-495f-b7bf-93971e02d126)

Так, число с плавающей точкой, значит нам нужен рецепт From float

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/2ccfef91-79a5-4e58-894c-6da798fa0f2f)

Получили какую то фигню, применим Magic

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/3e2e25ab-da78-4745-a61c-227f77b3ccbc)

И Кибершеф нам даёт ещё пару рецептов, применяем их и получаем ссылку

https://steamcommunity.com/id/oqnxyr/

Переходим и в аккаунте видим флаг

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/867fb197-cc89-4759-8221-c79eab9ce528)

Флаг: B0NU${S00M3t33XXtt}

IDK
----

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/1e7f24fc-f0ff-4705-a71b-c815183135d7)

Открываем файл в hex редакторе

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/1b3795cb-d33b-4d39-af1c-570703b9dc56)

Видим, что это картика jpeg, меняем расширение файла на jpg

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/91a9a658-d633-4f87-b625-2496a52d2e26)

Далее загружаем картинку в Aperisolve https://aperisolve.com/ и смотрим вывод

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/0f98b48a-6426-4916-9717-8ed35f8543a8)

Внутри картинки спрятан файл, скачиваем и смотрим

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/6a392a18-2bca-458f-927a-111b42a31a90)

Тут нам поможет подсказка к заданию, гуглим её

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/aa62d488-497b-4403-a108-1f247dbdc034)

Так у нас тут XOR, но у нас base64 текст. Заходим в Кибершефа и преобразуем base64 в байты убрав "ThereIsNoKey" и сохраняем файл

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/41fd5e6c-edfe-463f-a340-4370aab71e84)

Далее запускаем xortool и выясняем длину ключа

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/93e603c1-d93a-4748-898c-852db4b1b001)

С наибольшей вероятностью у нас в ключе 14 символов

Затем используем https://www.dcode.fr/ и инструмент XOR указав ему шифрованный текст в байтах и длину ключаа

![image](https://github.com/Re-An1mat0r/CTF_writeups/assets/127856250/1b580f48-0664-4a90-a112-ddfa9a6ea2bf)

И получаем флаг

Флаг: B0NU${x0R_cRyP70@n4L1sy$_KP4}








