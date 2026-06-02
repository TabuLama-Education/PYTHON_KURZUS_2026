#  Python változók

##  1. Mi az a változó?

- Egy **név**, amely egy adott **értékre mutat** a memóriában.
- Segítségével könnyen hivatkozhatunk adatokra, számításokat végezhetünk velük.
- Pythonban nem kell előre megadni a változó típusát – **dinamikusan típusos** nyelv.

 Példa:

```python
szam = 10
nev = "Anna"
atlag = 4.52
```

---

##  2. Változónév szabályai

- Csak **betűt (a–z, A–Z), számot (0–9), és aláhúzást (\_) tartalmazhat**.
- Nem kezdődhet számmal!
- Nem használhatsz **speciális karaktereket** (pl. %, !, -, ékezetes betűk).
- Python **kis- és nagybetű érzékeny** (`nev` ≠ `Nev` ≠ `NEV`).
- Nem használhatsz **foglaltszókat** (pl. `class`, `for`, `if`, `while`).

 Érvényes változónevek:

```python
x = 5
kor = 28
atlag_pont = 4.5
nev1 = "Béla"
```

 Érvénytelen változónevek:

```python
1nev = "Anna"    # nem kezdődhet számmal
átlag = 3.2      # ékezet nem megengedett
for = 10         # foglalt szó
```

---

##  3. Változók típusai

Pythonban a változó típusa az **értéktől függ**, és futás közben változhat.

- **int** – egész számok
- **float** – tört számok
- **str** – szöveg (string)
- **bool** – logikai érték (True/False)
- **list** – lista
- **tuple** – rendezett, de nem módosítható sorozat
- **dict** – szótár (kulcs-érték párok)
- **set** – halmaz

 Példa:

```python
eletkor = 20        # int
atlag = 4.3         # float
nev = "Zsófi"       # str
diak = True         # bool
szamok = [1, 2, 3]  # lista
```

---

##  4. Értékadás

Az **egyenlőségjel (`=`)** használatával adunk értéket egy változónak.

```python
x = 5
y = x + 3
z = "Hello"
```

Egyszerre több érték is adható:

```python
a, b, c = 1, 2, 3
```

---

##  5. Típuskonverzió

Az értékek típusát át lehet alakítani:

```python
x = "100"
y = int(x)   # "100" → 100
z = float(x) # "100" → 100.0
```

---

##  6. Konvenciók (ajánlások)

 **snake\_case** használata javasolt: `nev`, `atlag_pont`, `ossz_ertek`.
 Konstansokhoz (amit nem változtatunk meg): **NAGYBETŰVEL** írjuk:

  ```python
  PI = 3.14159
  ```

---

##  7. Hasznos függvények változókkal

 `type(v)` → megmondja a változó típusát
 `id(v)` → memóriabeli azonosítót ad vissza
 `print(v)` → kiírja az értéket

 Példa:

```python
x = 10
print(type(x))  # <class 'int'>
print(id(x))    # pl. 140712345678912
```
