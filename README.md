# CTF_writeups
CTF_writeups

Hackosint2024_bonus_tasks

Криптография

Тык-Тык

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





