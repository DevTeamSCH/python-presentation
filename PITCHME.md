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

### Alapok

---

### Változók

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

### Vezérlési szerkezetek

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

### Vezérlési szerkezetek

```python
a = [1, 2, 3]
for x in a:
	print(x)

print("-")
	
for x in range(1, 6, 2): # for (int i = 1; i < 10; i += 2)
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

### Vezérlési szerkezetek

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

### Függvények

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

### Adatszerkezetek

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

### Csomagkezelés

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
pip install virtualenv
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

---

### pipenv

- pip + virtualenv
```
pip install pipenv
pipenv install requests
pipenv install pytest --dev
pipenv lock
pipenv sync [--dev]
```
```
[[source]]
url = "https://pypi.org/simple"
verify_ssl = true
name = "pypi"

[packages]
django-bootstrap4 = "*"
django-markdownx = "*"
pytz = "*"
django-search-views = "*"
Django = "*"
django-registration = "*"

[dev-packages]
django-debug-toolbar = "*"

[requires]
python_version = "3.7"
```

---

### Szintaktika cukorkak

---

### Csomagok

---

### Objektum orientált python

---

### Dekorátorok

---

### Modulok

---

### Std

---

### Toolok

