# Comprehensive-Python-Cheatsheet
Comprehensive Python Cheatsheet
## ref https://github.com/gto76/python-cheatsheet#coroutines


# Collections
## List
init list
```python
L = list(range(1,10,2))
``` 

add new element
```python
L.append(10)
L+=[10]
L.extend({1,2,3})
L+={1,2,3}
``` 

sort and reverse
```python
L = [3,1,10,2]
L.sort()
L.reverse()
L = sorted(L)
L = sorted(L,key= lambda x: x[0])
L = list(reversed(L))
``` 

```python
L = [3,1,10,2]
print(sum(L))

list_a = [10,20,30]
list_b = [10,10,10]
list_c = [sum(pair) for pair in zip(list_a, list_b)]
print(list_c)
``` 

flattern list
```python
L = [['a','b'],'c']
list(itertools.chain.from_iterable(<list>))

name ="nghiahgs"
print(list(name))
``` 

reduce list
```python
L = [1,2,3,4]
kq = functools.reduce(lambda out, el: out * el, L)
print(kq)
```

```python
L = ['a','c','d']
L.insert(1,'b')
print(L)

L.pop()
print(L)
```

```python
L = ['a','b','c','d']
print(L.count('b'))
print(L.index('b'))
L.remove('b')
print(L)
L.clear()
print(L)
```

## Dictionary

```python
d = {'one':1,'two':2}
L_keys = d.keys()
print(L_keys)
L_values = d.values()
print(L_values)
L_items = d.items()
print(L_items)
```

```python
d = {'one':1,'two':2}
print(d.get('one'))
print(d.get('three'))
```

```python
L = [['nghia',20],['trang',19]]
d = dict(L)

keys = ['nghia','trang']
values = [20,21]
d = dict(zip(keys, values))

keys = ['nghia','trang']
value = 25
d = dict.fromkeys(keys,value)  
```

```python
d = {'nghia':20,'trang':19}
d['nghia'] = 25
print(d)
d.update({'nghia':35})
print(d)
```

```python
d = {'nghia':20,'trang':19,'someone':25}
d.pop('someone')
print(d)
```

```python
d = {'nghia':20,'trang':20,'someone':25}
d2 = {k:v for k, v in d.items() if v == 20}
```

## Counter
```python
from collections import Counter
colors = ['green','blue', 'blue', 'blue', 'red', 'red']
counter = Counter(colors)
print(counter)
counter['yellow'] += 1
print(counter)

# return a list
print(counter.most_common())
```

## Set
```python
s = {1}
s.add(10)
s.add(12)
s.add(10)
print(s)
```

```python
s1 = {1,3,5,7}
s2 = {5,7,9,11}
#union
s3 = s1|s2
print(s3)
#intersection
s4 = s1&s2
print(s4)
#difference
print(s1-s2)
print(s2-s1)

# check is subset or is supper set
print(s1<=s2)
print(s1>=s2)
```

```python
s1 = {1,3,5,7}
# remove fisrt element
s1.pop()
s1.remove(5)  # Raises KeyError if missing.
s1.discard(5) # Doesn't raise an error.
```

```python
L = [1,2,3,4,1]
s = set(L)
# neu la so thi sap xep, chu sap xep chu cai dau
print(s)
```

## Tuple
```python
t = ()
t = (1,)
t = (1,2)
```

## Range
```python
L = list(range(10))
print(L)
L = list(range(5,10))
print(L)
L = list(range(5,10,2))
print(L)


r = range(5,10,2)
start = r.start
stop = r.stop
step = r.step
print(start)
print(stop)
print(step)
```

## Enumerate
```python
L = ['Nguyen','Ba','Nghia']
for i, l in enumerate(L):
    print(i, l)
```

## Iterator