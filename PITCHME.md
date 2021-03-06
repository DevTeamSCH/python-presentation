# Python3  

```python
import this
```

---

### The Zen of Python, by Tim Peters

<div class="half left">
  <ol>
  @size[24px](<li><b>Beautiful is better than ugly.</b></li>)
  @size[24px](<li><b>Explicit is better than implicit.</b></li>)
  @size[24px](<li><b>Simple is better than complex.</b></li>)
  @size[24px](<li><b>Complex is better than complicated.</b></li>)
  @size[24px](<li>Flat is better than nested.</li>)
  @size[24px](<li>Sparse is better than dense.</li>)
  @size[24px](<li><b>Readability counts.</b></li>)
  @size[24px](<li>Special cases aren't special enough to break the rules.</li>)
  @size[24px](<li>Although practicality beats purity.</li>)
  @size[24px](<li>Errors should never pass silently.</li>)
  @size[24px](<li>Unless explicitly silenced.</li>)
  @size[24px](<li>In the face of ambiguity, refuse the temptation to guess.</li>)
  </ol>
</div>

<div class="half right">
  <ol start="13">
  @size[24px](<li>There should be one-- and preferably only one --obvious way to do it.</li>)
  @size[24px](<li>Although that way may not be obvious at first unless you're Dutch.</li>)
  @size[24px](<li>Now is better than never.</li>)
  @size[24px](<li>Although never is often better than <i>right</i> now.</li>)
  @size[24px](<li><b>If the implementation is hard to explain, it's a bad idea.</b></li>)
  @size[24px](<li><b>If the implementation is easy to explain, it may be a good idea.</b></li>)
  @size[24px](<li>Namespaces are one honking great idea -- let's do more of those!</li>)
  </ol>
</div>

---

### import this

```python
s = """Gur Mra bs Clguba, ol Gvz Crgref
Ornhgvshy vf orggre guna htyl.
Rkcyvpvg vf orggre guna vzcyvpvg.
Fvzcyr vf orggre guna pbzcyrk.
Pbzcyrk vf orggre guna pbzcyvpngrq.
Syng vf orggre guna arfgrq.
Fcnefr vf orggre guna qrafr.
Ernqnovyvgl pbhagf.
Fcrpvny pnfrf nera'g fcrpvny rabhtu gb oernx gur ehyrf.
Nygubhtu cenpgvpnyvgl orngf chevgl.
Reebef fubhyq arire cnff fvyragyl.
Hayrff rkcyvpvgyl fvyraprq.
Va gur snpr bs nzovthvgl, ershfr gur grzcgngvba gb thrff.
Gurer fubhyq or bar-- naq cersrenoyl bayl bar --boivbhf jnl gb qb vg.
Nygubhtu gung jnl znl abg or boivbhf ng svefg hayrff lbh'er Qhgpu.
Abj vf orggre guna arire.
Nygubhtu arire vf bsgra orggre guna *evtug* abj.
Vs gur vzcyrzragngvba vf uneq gb rkcynva, vg'f n onq vqrn.
Vs gur vzcyrzragngvba vf rnfl gb rkcynva, vg znl or n tbbq vqrn.
Anzrfcnprf ner bar ubaxvat terng vqrn -- yrg'f qb zber bs gubfr!"""

d = {}
for c in (65, 97):
    for i in range(26):
        d[chr(i+c)] = chr((i+13) % 26 + c)

print("".join([d.get(c, c) for c in s]))
```

---

### Basics

---

### Variables

```python
a = 2
b = 3.2
d = 2+4j
x = False
str = "string"
str2 = str * 2
str3 = str2 + "abc"
```

- number (integer, floating point, complex)
- boolean
- string
- list, tuple, dictionary, ...

---

### If

```python
b = False
x = 3
if not b and x <= 6:
    print("Hello")
```

Output:
```
Hello
```

---

### For(each)

```python
a = [1, 2, 3]
for x in a:
    print(x)

print("-")

for x in range(1, 6, 2): # for (int i = 1; i < 6; i += 2)
    print(x)
```

Output:
```
1
2
3
-
1
3
5
```

---

### While

```python
i = 1
while i < 6:
    print(i)
    i += 1
```

Output:
```
1
2
3
4
5
```

---

### Functions

```python
def fun(x, mul=False):
    if mul:
        return x * 2
        return x + 2

print(fun(4))
print(fun(4, True))
print(fun(4, mul=True))
```

Output:
```
6
8
8
```

---

### Data Structures

---

### List

```python
list = ['a', 'b', 'c', 1, 2, 3]
list[4] = 22
for a in list:
    print(a)
```

Output:
```
a
b
c
1
22
3
```
---

### Tuple

```python
tuple = ('a', 'b', 3)
item = tuple[2]
for a in tuple:
    print(a)
a, b, c = tuple
print(c)
```
Output:
```
a
b
3
3
```
---

### Dictionary
```python
dict = {
  "name": "John Smith",
  "age": 35
}
print(dict)
print(dict['name'] + " is " + str(dict['age']) + " years old")
for a in dict:
    print(a)
for key, value in dict.items():
    print(key + ":" + str(value))
```
Output:
```
{'name': 'John Smith', 'age': 35}
John Smith is 35 years old
name
age
name:John Smith
age:35
```

---

### Set
```python
set = {1, 3, 5}
print(1 in set)
print(2 in set)
set.add(2)
set.update([4,6])
for a in set:
    print(a)
```
Output:
```
True
False
1
2
3
4
5
6
```
---

### Deque
```python
from collections import deque
deque([1,2,3], 5)
deque.append(4)
deque.appendleft(0)
print(deque)
deque.extend([5,6,7])
print(deque)
print(deque.pop())
print(deque.popleft())
print(deque)
```
Output:
```
deque([0, 1, 2, 3, 4], maxlen=5)
deque([3, 4, 5, 6, 7], maxlen=5)
7
3
deque([4, 5, 6], maxlen=5)
```
---

### Package Managemenet

---

### Pip

```
pip install requests
```
```
import requests
...
```

---
### Virtualenv

```
python -m venv ~/virtualenvs/test
source ~/virtualenvs/test/bin/activate
```
- Virtualenvwrapper
- Saját környezet minden projekthez

```
mkvirtualenv test
workon test
pip install requests
deactivate
rmvirtualenv test
```

---

### requirements.txt

```
certifi==2018.8.24
chardet==3.0.4
idna==2.7
pkg-resources==0.0.0
requests==2.19.1
urllib3==1.23
```
```
pip install -r requirements.txt
pip freeze
```

---

### pip-tools

```
requests
```
- requirements.in -> requirements.txt (pip-compile)
- pip-compile --upgrade
- pip-sync
- Külön development és production dependeciák kezelése
---

### pipenv

- pip + virtualenv

```
pip install pipenv
pipenv install requests
pipenv install pytest --dev
pipenv lock
pipenv sync [--dev]
pipenv run ./script.py
pipenv shell
```

---

### Pipfile

```
[[source]]
url = "https://pypi.org/simple"
verify_ssl = true
name = "pypi"

[packages]
requests = "*"

[dev-packages]
pytest = "*"

[requires]
python_version = "3.7"
```

---

### Syntactic Sugar

---

### f-string

```python
name = 'Bill'
age = 6
text = f'My name is {name.upper()} and I'm {age*10**23} years old.'
print(text)
```

Output:
```
My name is BILL and i am 600000000000000000000000 years old.
```

---

### Slice array

```python
data = [1, 2, 3, 4, 5, 6, 7, 8, 9]
ret = []
i=2
while i < 4:
    ret.append(data[i])
    i=i+1
```

```python
data = [1, 2, 3, 4, 5, 6, 7, 8, 9]
ret = data[2:4]
```

---

### List comprehension

```python
list = []
for i in range(1, 11):
    if i % 2 == 0:
        list.append(i*i)

list = [i*i for i in range(11) if i % 2 == 0]

print(list)
```

Output:
```
[0, 4, 16, 36, 64, 100]
```

---

### Yield
```python
def fun():
    for i in range(6):
        yield i*i

gen = (i*i for i in range(11) if i % 2 == 0)
gen2 = fun()
for i in gen2:
    print(i)
```
Output:
```
0
1
4
9
16
25
```

---

### With
```python
import json

with open('test.json', 'rt') as fp:
    data = json.load(fp)
```

```
file = open('file.txt', 'w')
data = json.load(file)
file.close()

with open('test.json', 'rt') as fp:
    data = json.load(fp)
```

---

### Exception handling

```python
file = None
try:
    file = open('output.txt', 'r')
    data = file.read()
    if data == "error":
        raise Exception("File contains error")
except FileNotFoundError as e:
    print("File not found")
except Exception as e:
    print(e)
except:
    print("Some other error occurred")
else:
    print("Completed with no errors")
finally:
    if file is not None:
        file.close()
```

---

### args, kwargs
```python
def funny_args(a, *args, **kwargs):
    print(kwargs['hello'])
    print(args[0])

funny_args(1, 'World!', hello='Hello')
```
 Output:
```
Hello
World!
```
---

### Async / Await
```python
import asyncio

async def main():
     print('hello')
     await asyncio.sleep(1)
     print('world')

asyncio.run(main())
```
Output:
```
hello
world
```
---

### Type Hints

```python
from typing import List
Vector = List[float]

def scale(scalar: float, vector: Vector) -> Vector:
    return [scalar * num for num in vector]

new_vector = scale(2.0, [1.0, -4.2, 5.4])
```

---
### Decorators

```python
def my_decorator(func):
    def wrapper():
       print("Before")
       func()
       print("After")

    return wrapper

@my_decorator
def hello():
    print("Hello")
````
Output:

```
Before
Hello
After
```

---

### Object Oriented Python
```python
class A:
  b = 'Foo'
  def __init__(self):
    self.a = 1

class B(A):
    def __init__(self, a):
        self.a = a

     @classmethod
     def without(cls):
         return cls(5)

     @staticmethod
     def foo():
        pass

a = A()
b = B.without()
```
---



### Modules
[https://docs.python.org/3/tutorial/modules.html](https://docs.python.org/3/tutorial/modules.html)
---

### Standard Library

[https://docs.python.org/3/library/](https://docs.python.org/3/library/)

---

### Tools

* flake8 / pyflakes
* pyls
* pydocstyle
* pylint
* ...
