# Python
```Python
#5.9_11
phrase = 'Take only the words that start with t in this sentence'
n1 = phrase.split()
print([i for i in n1 if i[0] == 't' or i[0] == 'T'])
