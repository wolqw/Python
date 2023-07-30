```python
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
