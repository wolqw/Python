```python
#Descending Order

def descending_order(num):
    arra = []
    for i in str(num):
        arra.append(i)
    arra.sort(reverse=True)
    num = int(''.join(map(str, arra)))
    return num
