```python
#Descending Order

def descending_order(num):
    arra = []
    for i in str(num):
        arra.append(i)
    arra.sort(reverse=True)
    num = int(''.join(map(str, arra)))
    return num

#or
def Descending_Order(num):
    return int("".join(sorted(str(num), reverse=True)))
