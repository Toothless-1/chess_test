# Шахматы: куда дальше идём?

Нужно по имеющейся позиции предсказать следующий ход. Идея решения — применить методы Computer Vision, представив, что доска это "изображение" формата [1;8;8]

## EDA
Посмотрим, какие типы ходов представлены в датасете\
<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/c46e6611-f4c6-49c5-b2f6-40658a61c915" align="centre"/>\
Также интересно посмотреть, какие фигуры чаще всего ходят\
<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/ead85887-0a36-4eb0-aa53-09f24e6ca492" />\
Видно, что чаще всего ходят пешки, вторыми по популярности — ладьи и топ-3 это ход конём.

## Разработка моделей
Были рассмотрены несколько архитектур
1. Двухглавая архитектура
2. Архитектура с возвратными блоками и механизмом внимания
3. Двухглавая архитектура с моделью ResNet-50 в качестве backbone
4. Архитектура с возвратными блоками и механизмом внимания и с моделью ResNet-50 в качестве backbone

Результаты обучения для каждой из моделей ниже\
1. Двухглавая архитектура <img width="902" height="603" alt="image" src="https://github.com/user-attachments/assets/1e45d45f-65bd-49c9-bc0a-67cb4dec701f" />
2. Архитектура с возвратными блоками и механизмом внимания\ <img width="895" height="599" alt="image" src="https://github.com/user-attachments/assets/e59004a8-7c97-40a8-860c-d7b5b71b187c" />
3. Двухглавая архитектура с моделью ResNet-50 в качестве backbone <img width="896" height="599" alt="image" src="https://github.com/user-attachments/assets/7dd47f01-36b9-4d86-b29d-d88cc471b5ac" />
4. Архитектура с возвратными блоками и механизмом внимания и с моделью ResNet-50 в качестве backbone <img width="900" height="598" alt="image" src="https://github.com/user-attachments/assets/1295bd4b-f3eb-40c6-898d-bde6fe68f784" />

Было решено остановиться на модели номер 3. Предсказания для неё ниже\
<img width="921" height="720" alt="image" src="https://github.com/user-attachments/assets/3a01e65a-9ec4-452b-b3f4-43bd7ac28440" />
