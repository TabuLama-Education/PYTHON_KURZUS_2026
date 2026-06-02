#  Python – Logikai operátorok

##  1. Alap logikai értékek

 `True` → igaz
 `False` → hamis

 Példa:

```python
print(5 > 3)   # True
print(2 == 4)  # False
```

---

##  2. Logikai operátorok

| Operátor | Jelentés                                                  | Példa                  | Eredmény |
| -------- | --------------------------------------------------------- | ---------------------- | -------- |
| `and`    | ÉS → akkor igaz, ha **mindkét feltétel igaz**             | `(5 > 3) and (10 > 2)` | True     |
| `or`     | VAGY → akkor igaz, ha **legalább az egyik feltétel igaz** | `(5 > 10) or (3 > 1)`  | True     |
| `not`    | NEM → megfordítja az értéket                              | `not (5 > 3)`          | False    |

---

##  3. Példák kódban

```python
a = 7
b = 3

print(a > 5 and b < 5)  # True  (mindkettő igaz)
print(a > 10 or b < 5)  # True  (a második igaz)
print(not(a > b))       # False (mert a > b igaz, a not megfordítja)
```

---

## 🔹 4. Igazságtáblák

### `and`

| A     | B     | A and B |
| ----- | ----- | ------- |
| True  | True  | True    |
| True  | False | False   |
| False | True  | False   |
| False | False | False   |

### `or`

| A     | B     | A or B |
| ----- | ----- | ------ |
| True  | True  | True   |
| True  | False | True   |
| False | True  | True   |
| False | False | False  |

### `not`

| A     | not A |
| ----- | ----- |
| True  | False |
| False | True  |

---

##  5. Műveletek sorrendje

A logikai operátorok sorrendben:

1. `not`
2. `and`
3. `or`

 Példa:

```python
eredmeny = True or False and not False
print(eredmeny)  # True (mert először not → False, majd and → False, végül or → True)
```

---
 **Összefoglalva:**

- `and` → csak akkor igaz, ha minden feltétel igaz.
- `or` → elég, ha egy feltétel igaz.
- `not` → megfordítja a logikai értéket.
- A sorrend fontos: először `not`, majd `and`, végül `or`.
