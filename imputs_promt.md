```python
a = input()
a = int(input())
a = float(input())
a,b = map(int,input().split())
a,b,c = map(float,input().split())
l = list(map(int,input().split()))
pattern = [input() for i in range(4)]
s = set(map(int,input().split()))
t = tuple(map(float,input().split()))
d = dict(zip(map(str,input().split()), map(int,input().split())))
matrix = [list(map(int,input().split())) for _ in range(3)]
graph = [[int(x) for x in input().split()] for _ in range(5)]
