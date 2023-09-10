```python

from random import randint
n = 5
m = 3
a = [[randint(1,6) for j in range(m)] for i in range(n)]
for i in a:
    print(i)
