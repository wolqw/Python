```python
#################
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

##########################
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

###################
#Is this a triangle?
def is_triangle(a, b, c):
    if (a + b) > c and (a + c) > b and (b + c) > a and a > 0 and b > 0 and c > 0:
        return True
    else:
        return False
#or
def is_triangle(a, b, c):
    a, b, c = sorted([a, b, c])
    return a + b > c

#################
#Find the odd int
def find_it(seq):
    if len(seq) == 1:
        return seq[0]
    else:
        for i in seq:
            if seq.count(i) % 2 != 0:
                return i
#or

###############
#Friend or Foe
def find_it(seq):
    return [x for x in seq if seq.count(x) % 2][0]

def friend(x):
    a=[]
    for i in x:
        if len(i) == 4:
            a.append(i)
    return a
#or
def friend(x):
    return [f for f in x if len(f) == 4]

### odd or even
def oddOrEven(arr):
    return ('even', 'odd')[sum(arr) % 2]

##Split string
def solution(s):
    ss = list(s)
    a=[]
    for i in range(0,len(ss)):
        if i % 2 != 0:
            a.append(ss[i-1]+ss[i])
    if len(ss) % 2 != 0:
        a.append(ss[-1]+'_')
    return a
