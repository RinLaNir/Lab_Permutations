# Лабораторна робота знаходнження добудку циклів, які рухают не більше 5 елементів, мінімальної довжини.

Нехай ми маємо перестановку <img src="https://latex.codecogs.com/gif.latex?%5CPi">, яку можна відобразити у вигляді добутку
незалежних циклів.

Всі цикли довжини 5 або менше ми можемо одразу записати в результат, бо вони
не рухают жодного елемента при добутку.

Інші елементи ми повинні розбити на менші цикли, тому хоча б 1 елемент будет
спільним. Щоб отримати мінімальну кількість циклів тільки один елемент може
бути спільним.

n<k<m, (n ... m) - деякий цикл з добутку
=> Ми можемо розкласти його у вигляді (n ... k)(k+1 ... m)
Щоб кожеш цикл рухав не більше 5 елементів він повинен буди довжини не більше 5.
=> k <= n+4

Звідси, ми маємо розкласти кожен з циклів довжини >5 у добуток циклів довжини 5,
поки не отримаемо в кінці цикл довжини <=5.
Всі цикли довжини 5 ми відправляемо до результату. Залишилися остатки від розиття
(цикли довжини <5).

Але вони не мают спільних елементів, бо походять від різних незалежних циклів
(від неперетинаючих класів). Звідси, при добудтку один на інший ми не
отримуємо нові цикли більшої довжини. Тому ми можемо відправити усі ці цикли до
результату. Більше циклів не залишилося.
