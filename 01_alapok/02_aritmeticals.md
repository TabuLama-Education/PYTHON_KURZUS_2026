#  Python – Aritmetikai műveletek

##  1. Alapműveletek


| Művelet          | Operátor | Példa    | Eredmény   |
| ---------------- | -------- | -------- | ---------- |
| Összeadás        | `+`      | `5 + 3`  | `8`        |
| Kivonás          | `-`      | `10 - 4` | `6`        |
| Szorzás          | `*`      | `7 * 2`  | `14`       |
| Osztás (tört)    | `/`      | `8 / 3`  | `2.666...` |
| Egész osztás     | `//`     | `8 // 3` | `2`        |
| Maradék (modulo) | `%`      | `8 % 3`  | `2`        |
| Hatványozás      | `**`     | `2 ** 3` | `8`        |

---

##  2. Példák kódban

```python
a = 15
b = 4

print(a + b)   # 19
print(a - b)   # 11
print(a * b)   # 60
print(a / b)   # 3.75
print(a // b)  # 3
print(a % b)   # 3
print(a ** b)  # 50625
```

---

##  3. Műveletek sorrendje

Python ugyanazt a **matematikai sorrendet** követi, mint amit megszoktál:

1. Zárójelek `()`
2. Hatványozás `**`
3. Szorzás, osztás, egész osztás, maradék `* / // %`
4. Összeadás, kivonás `+ -`

 Példa:

```python
eredmeny = 2 + 3 * 4    # = 14
eredmeny2 = (2 + 3) * 4 # = 20
```

---

##  4. Rövidített értékadás (augmented assignment)

Ha egy változót saját magával szeretnénk frissíteni:

| Rövid forma | Hosszú forma | Példa        |
| ----------- | ------------ | ------------ |
| `x += 3`    | `x = x + 3`  | növelés      |
| `x -= 2`    | `x = x - 2`  | csökkentés   |
| `x *= 5`    | `x = x * 5`  | szorzás      |
| `x /= 2`    | `x = x / 2`  | osztás       |
| `x //= 2`   | `x = x // 2` | egész osztás |
| `x %= 2`    | `x = x % 2`  | maradék      |
| `x **= 2`   | `x = x ** 2` | hatványozás  |

 Példa:

```python
x = 10
x += 5   # 15
x *= 2   # 30
x -= 4   # 26
```

---

##  5. Számok típusai aritmetikában

- Ha **mindkét operandus egész** → eredmény int (kivéve `/`, ami mindig float).
- Ha **egyik operandus float** → eredmény float.

 Példa:

```python
print(5 / 2)   # 2.5 (float)
print(5 // 2)  # 2   (int)
print(5.0 // 2) # 2.0 (float)
```

---

##  6. Beépített függvények számokhoz

- `abs(x)` → abszolút érték
- `round(x, n)` → kerekítés n tizedesre
- `pow(a, b)` → hatványozás (ugyanaz mint `a ** b`)
- `divmod(a, b)` → egyszerre adja az egész osztást és a maradékot

 Példa:

```python
print(abs(-7))      # 7
print(round(3.1415, 2))  # 3.14
print(pow(2, 5))    # 32
print(divmod(17, 5)) # (3, 2)
```

---

 **Összefoglalva:**

- Python minden alap aritmetikai műveletet támogat.
- Figyelni kell az osztás (`/` → float, `//` → egész) különbségére.
- Van rövidített értékadás is (`+=`, `-=`, …).
- A sorrend a matematikában megszokott (zárójel előnyt élvez).