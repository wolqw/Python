```python
Дан прямоугольный торт, который имеет вид таблицы размером r × c. Каждая ячейка таблицы содержит либо гадкую клубничку, либо является пустой.
   Тортминатор намерен съесть этот торт! Каждый раз, когда он ест, он выбирает строку или столбец, не содержащие гадкой клубнички, а содержащие по крайней мере одну несъеденную ячейку торта. Затем Тортминатор поедает все выбранные им ячейки торта. Тортминатор может есть сколько угодно раз. Вот пример того, как он это сделает
Пожалуйста, выведите максимальное количество ячеек, которые может съесть Тортминатор.



n, m = map(int, input().split())
mas = [[i for i in input()] for j in range(n)]
row = []
s = 0
ctrok = 0
stolbov = 0
for i in range(n):
    cnt = 0
    for j in range(m):
        if mas[i][j] != 'S':
            cnt += 1
    if cnt == m:
        ctrok += 1
        s += cnt
for j in range(m):
    cnt = 0
    for i in range(n):
        if mas[i][j] != 'S':
            cnt += 1
    if cnt == n:
        stolbov += 1
        s += cnt
print(s - (stolbov * ctrok))



n, m = map(int, input().split())
c_n = [1] * m
c_m = 0
for _ in range(n):
    s = input()
    if 'S' in s:
        for i in range(m):
            if s[i] == 'S':
                c_n[i] = 0
    else:
        c_m += 1
print(c_m * m + c_n.count(1) * (n - c_m))
