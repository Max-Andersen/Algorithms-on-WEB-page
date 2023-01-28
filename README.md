# Algorithms on web page
---
Проект создан в рамках модуля Web-разработки на первом курсе Высшей IT-школы ТГУ, и представляет из себя сайт с реализованными алгоритмами на JavaScript:
- [A*](https://ru.wikipedia.org/wiki/A*)
- [Кластеризация методом k-средних](https://ru.wikipedia.org/wiki/Метод_k-средних)
- [Генетический алгоритм](https://ru.wikipedia.org/wiki/Генетический_алгоритм)
- [Муравьиный алгоритм](https://ru.wikipedia.org/wiki/Муравьиный_алгоритм)

Я реализовал алгоритмы A*, генетический и муравьиный.

### A*
Является усовершественной версией [алгоритма Дейкстры](https://ru.wikipedia.org/wiki/Алгоритм_Дейкстры) за счёт введения эвристики и структуры "Приоритетная очередь". Суть алгоритм - найти маршрут с наименьшей стоимостью от одной вершины до другой, по нашему заданию, нужно найти выход из лабиринта. Введение эвристики позволяет вычислять "приоритет ячейки", чем она ближе к целевой точке, тем приоритет больше, следовательно, алгоритм будет выбирать рассматриваемые ячейки ближе к целевой.

Реализовано 2 типа эвристик:
```JavaScript
  Math.abs(current[0] - end[0]) + Math.abs(current[1] - end[1]) // Манхэттенское расстояние
  Math.sqrt(Math.pow(current[0] - end[0], 2) + Math.pow(current[1] - end[1], 2)) // Евклидово расстояние
```
![Манхэттенское расстояние](https://user-images.githubusercontent.com/44117017/215261673-0f7c502a-1924-4398-83e5-4d1fcceb35a3.png) ![Евклидово расстояние](https://user-images.githubusercontent.com/44117017/215261679-48443a37-3921-4ed9-969d-5075e0433a12.png)


### Генетический алгоритм
В рамках нашего задания был использован для решения [задачи коммивояжёра](https://ru.wikipedia.org/wiki/Задача_коммивояжёра).

Схема алгоритма:<br>
<img src=https://user-images.githubusercontent.com/44117017/215261718-6ab9462e-23ea-4865-9994-75444d578cd9.png height = 400>  <img src=https://user-images.githubusercontent.com/44117017/215261751-1ad54fa8-9e9b-4a82-b9db-1d72fe81c7ba.gif height = 400>



### Муравьиный алгоритм
Тоже был использован для решения задачи коммивояжёра. Суть подхода заключается в анализе и использовании модели поведения муравьёв, ищущих пути от колонии к источнику питания. Муравьи, выходящие из каждой вершины решают, по какому пути пойти по формуле:

<img src=https://user-images.githubusercontent.com/44117017/215262061-3c6c72cd-5080-412f-adf9-230053862212.png width = 500>
<img src=https://user-images.githubusercontent.com/44117017/215261756-7387d796-a85d-4df1-870f-6fea3112af00.gif height = 400>


Состав команды:
- Смирнов Кирилл
- Толокнов Максим
- Галяткин Дмитрий
