# Python3  

```python
import this
```

---
@transition[none]

### The Zen of Python, by Tim Peters

<div class="half left">
	<ol>
		<li><b>Beautiful is better than ugly.</b></li>
		<li><b>Explicit is better than implicit.</b></li>
		<li><b>Simple is better than complex.</b></li>
		<li><b>Complex is better than complicated.</b></li>
		<li>Flat is better than nested.</li>
		<li>Sparse is better than dense.</li>
		<li><b>Readability counts.</b></li>
		<li>Special cases aren't special enough to break the rules.</li>
		<li>Although practicality beats purity.</li>
	</ol>
</div>

<div class="half right">
	<ol start="10">
		<li>Errors should never pass silently.</li>
		<li>Unless explicitly silenced.</li>
		<li>In the face of ambiguity, refuse the temptation to guess.</li>
		<li>There should be one-- and preferably only one --obvious way to do it.</li>
		<li>Although that way may not be obvious at first unless you're Dutch.</li>
		<li>Now is better than never.</li>
		<li>Although never is often better than <i>right</i> now.</li>
		<li><b>If the implementation is hard to explain, it's a bad idea.</b></li>
		<li><b>If the implementation is easy to explain, it may be a good idea.</b></li>
		<li>Namespaces are one honking great idea -- let's do more of those!</li>
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

