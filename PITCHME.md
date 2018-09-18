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

