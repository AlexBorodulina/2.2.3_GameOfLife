# Клеточный автомат "Жизнь"

Реализуйте клеточный автомат “Игра Жизнь”. Подробное описание смотрите [здесь](en.wikipedia.org/wiki/Conway’s_Game_of_Life).

## Правила игры (для данной задачи)

+ Место действия игры - двумерный массив размерности `(M, N)`.
+ Каждая клетка - т.е. ячейка массива - может находиться в двух состояниях: быть живой или мёртвой.
+ Клетка имеет восемь соседей, окружающих её.
+ Следующий шаг рассчитывается в зависимости от текущего состояния по следующим правилам:
  + Жизнь зарождается в пустой клетке, если рядом с ней ровно ровно три других живых клетки
  + Если у живой клетки две или три живые соседки, то она продолжает жить, иначе умирает.
+ Игровое поле зациклено по вертикали и по горизонтали. Например, клетка `(k, N - 1)` является соседкой клетки `(k, 0)`.

*(взято с [Википедии](https://ru.wikipedia.org/wiki/%D0%98%D0%B3%D1%80%D0%B0_%C2%AB%D0%96%D0%B8%D0%B7%D0%BD%D1%8C%C2%BB#%D0%9F%D1%80%D0%B0%D0%B2%D0%B8%D0%BB%D0%B0))*

## Задание

Необходимо реализовать единственную функцию `step` в файле `life.py`.
+ Функция принимает один аргумент - текущее состояние игры - двумерный массив `numpy`, в ячейках которого лежит `True`, если соответствующая клетка жива, или `False`, если мертва.
+ Функция должна возвращать массив такой же размерности с состоянием игры на следующем шаге.

Проверить правильность работы функции можно в `life.ipynb`.

## Тестирование

Запустить автоматические тесты можно так:

```bash
python -m pytest -sv
```
