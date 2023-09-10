```python

from random import randint
n = 5
m = 3
a = [[randint(1,6) for j in range(m)] for i in range(n)]
for i in a:
    print(i)

import names
for i in range(0,10):
    nn1 = names.get_full_name()
    nn2 = names.get_last_name()
    result = nn1 + nn2
    print(result)
