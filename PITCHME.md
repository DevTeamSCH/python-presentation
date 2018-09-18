# Python3  

```python
import this
```

---
@title[The Zen of Python, by Tim Peters]
@snap[west span-50]
1. **Beautiful is better than ugly.**
1. **Explicit is better than implicit.**
1. **Simple is better than complex.**
1. **Complex is better than complicated.**
1. Flat is better than nested.
1. Sparse is better than dense.
1. **Readability counts.**
1. Special cases aren't special enough to break the rules.
1. Although practicality beats purity.
1. Errors should never pass silently.
@snapend
@snap[east span-50]
1. Unless explicitly silenced.
1. In the face of ambiguity, refuse the temptation to guess.
1. There should be one-- and preferably only one --obvious way to do it.
1. Although that way may not be obvious at first unless you're Dutch.
1. Now is better than never.
1. Although never is often better than *right* now.
1. **If the implementation is hard to explain, it's a bad idea.**
1. **If the implementation is easy to explain, it may be a good idea.**
1. Namespaces are one honking great idea -- let's do more of those!
@snapend
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
- list, tuple, dictionary

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

print("---")
	
for x in range(1, 10, 2): # for (int i = 1; i < 10; i += 2)
	print(x)
```

Output:
```
1
2
3
---
1
3
5
7
9
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

### Csomagkezelés

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

