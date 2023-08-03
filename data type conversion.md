```python
# data type conversion

# Преобразование массива в число
number = int(''.join(map(str, array)))
# Преобразование цифровых элементов массива в число
number = int(''.join(map(str, [x for x in array if isinstance(x, int)])))
