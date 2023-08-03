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

## Regex validate PIN code
def validate_pin(pin):
    
    s = str(pin)
    ss = list(s)
    sss = []
    for i in ss:
        if i.isnumeric():
            sss.append(i)
    if (len(sss)) == 4 and len(ss) == 4 or (len(sss)) == 6 and len(ss) == 6:
        return(True)
    else:
        return(False)
#or
def validate_pin(pin):
    return len(pin) in (4, 6) and pin.isdigit()
