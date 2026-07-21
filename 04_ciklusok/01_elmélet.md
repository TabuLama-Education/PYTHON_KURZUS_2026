## 1. Szint: Mi az a ciklus és miért kell?

Képzeld el, hogy ki kell írnod a képernyőre ötször, hogy `"Szia!"`.
Ciklus nélkül ez így nézne ki:

```python
print("Szia!")
print("Szia!")
print("Szia!")
print("Szia!")
print("Szia!")

```

Ez 5 sornál még elmegy, de mi van, ha **1000-szer** kellene kiírni? Vagy ha a felhasználótól függ, hányszor kell? Erre valók a ciklusok: megmondjuk a gépnek, hogy *mit* csináljon, és hányszor (vagy meddig) ismételje.

A Pythonban **kétfajta ciklus** létezik:

1. **`for` ciklus** (számlálós / gyűjteményen végigmenő)
2. **`while` ciklus** (feltételes)

---

## 2. Szint: A `for` ciklus – Amikor tudjuk, hányszor/min megyünk végig

A `for` ciklust akkor használjuk, ha:

* Egy gyűjtemény (pl. lista, szöveg) **minden egyes elemén** végig akarunk menni.
* Pontosan tudjuk, hányszor szeretnénk valamit megismételni.

### A) Végigmenetel egy listán (Elemenként)

A ciklusváltozó (amit a `for` után írsz, pl. `gyumolcs`) minden körben felveszi a lista következő elemét.

```python
gyumolcsok = ["alma", "banán", "eper"]

for gyumolcs in gyumolcsok:
    print(f"Szeretem a következőt: {gyumolcs}")

```

* **Kimenet:**
```text
Szeretem a következőt: alma
Szeretem a következőt: banán
Szeretem a következőt: eper

```



### B) Ismétlés számszor: a `range()` függvény

Ha nem egy meglévő listán akarsz végigmenni, hanem csak ötször megismételni valamit, a `range()` függvényt használjuk.

```python
# A range(5) a 0, 1, 2, 3, 4 számokat generálja (az 5 már nincs benne!)
for i in range(5):
    print(f"Ez a(z) {i}. ismétlés")

```

A `range()` függvénynek 3 opciója van:

* `range(5)` $\rightarrow$ $0$-tól $4$-ig ($5$ lépés)
* `range(2, 6)` $\rightarrow$ $2$-től $5$-ig ($2, 3, 4, 5$)
* `range(0, 10, 2)` $\rightarrow$ $0$-tól $10$-ig, $2$-esével lépkedve ($0, 2, 4, 6, 8$)

---

## 3. Szint: A `while` ciklus – Amíg a feltétel igaz

A `while` ciklust akkor használjuk, ha **nem tudjuk előre**, hányszor kell futnia a kódnak. A ciklus addig ismétel, amíg a megadott feltétel **igaz (True)**.

```python
szam = 1

while szam <= 3:
    print(f"A szám értéke: {szam}")
    szam = szam + 1  # Nagyon fontos! Ha ezt kihagyod, VÉGTELEN CIKLUS lesz!

```

>  **A végtelen ciklus veszélye:** Ha a `while` feltétele soha nem válik hamissá (`False`), a programod lefagy, mert örökké pörögni fog. (Ezt a szerkesztőkben általában a `Ctrl + C` billentyűkombinációval lehet leállítani).

### Életszerű példa: Jelszóbekérés

Itt tökéletes a `while`, mert nem tudhatjuk, hányszor fogja elrontani a felhasználó:

```python
jelszo = ""

while jelszo != "titok123":
    jelszo = input("Adja meg a jelszót: ")

print("Sikeres belépés!")

```

---

## 4. Szint: Ciklusirányítás – `break` és `continue`

Néha menet közben beleszóltunk a ciklus menetébe. Erre való ez a két kulcsszó:

### A) `break` – Azonnali kilépés

A `break` parancs **azonnal leállítja** a ciklust, és a program a ciklus utáni sorral folytatódik.

```python
szamok = [1, 3, 5, 8, 9, 11]

for szam in szamok:
    if szam % 2 == 0:  # Megkeressük az első páros számot
        print(f"Megvan az első páros szám: {szam}")
        break  # Megtaláltuk, nincs értelme tovább keresni, KILÉPÜNK!

```

### B) `continue` – Lépés a következő körre

A `continue` megszakítja az **aktuális kört**, átugorja a ciklusban utána lévő sorokat, és rátér a következő elemre.

```python
for i in range(1, 6):
    if i == 3:
        continue  # A 3-as számnál kihagyja a kiírást, és megy a 4-re
    print(f"Szám: {i}")

```

* **Kimenet:** $1, 2, 4, 5$ (A $3$-ast átugrotta).

---

## 5. Szint: Ciklusok egymásban (Egymásba ágyazott ciklusok)

Ciklus belsejébe is tehetsz másik ciklust. Ezt hívjuk **egymásba ágyazott ciklusnak** (nested loop).

Képzeld el úgy, mint a mutatókat az órán: a belső ciklusnak teljesen le kell futnia ahhoz, hogy a külső ciklus lépjen egyetlen egyet.

```python
# Szorzótábla egy része (1-től 3-ig)
for i in range(1, 4):         # Külső ciklus (sorok)
    for j in range(1, 4):     # Belső ciklus (oszlopok)
        print(f"{i} * {j} = {i * j}")
    print("---")  # Egy-egy blokk után elválasztó

```

---

## Összefoglaló táblázat: Melyiket mikor használjam?

| Ciklus fajtája | Mikor használd? | Példa |
| --- | --- | --- |
| **`for ... in lista:`** | Ha van egy meglévő listád/szöveged, aminek minden elemén végig kell menni. | Gyümölcsök kiírása, dolgozatok átnézése. |
| **`for ... in range():`** | Ha tudod a pontos darabszámot, hányszor futjon a kód. | "Írd ki 10-szer", "Számolj el 1-től 100-ig". |
| **`while condition:`** | Ha nem tudod, hányszor fut, mert egy feltételtől/felhasználótól függ. | Jelszóbekérés, "Addig játsszunk, amíg ki nem lépsz". |



---

## 1. A `for` ciklus szintaxisa (Lista/Gyűjtemény feldolgozása)

A `for` ciklus egy úgynevezett **iterációs ciklus**, amely egy véges gyűjtemény (pl. lista, karakterlánc, számsorozat) elemeit dolgozza fel egymás után.

### Általános alak:

```python
for ciklusvaltozo in gyujtemeny:
    # Ciklusmag (utasítások)

```

### A szintaktikai elemek részletezése:

* **`for` (kulcsszó):** Jelzi a fordítónak/értelmezőnek a ciklus kezdetét.
* **`ciklusvaltozo` (változó):** Egy tetszőlegesen elnevezett változó. A ciklus minden egyes futásakor (iterációjakor) felveszi a gyűjtemény soron következő elemét. Nem kell előre deklarálni.
* **`in` (operátor/kulcsszó):** Megadja a kapcsolatot a ciklusváltozó és az átvizsgálandó gyűjtemény között.
* **`gyujtemeny` (iterálható objektum):** Az az adatstruktúra (pl. `lista = [10, 20, 30]`), amelynek az elemein a ciklus végighalad.
* **`:` (kettőspont):** **Kritikus szintaktikai elem.** A kettőspont jelzi a kódblokk (ciklusmag) kezdetét. A kettőspont elhagyása szintaktikai hibát (`SyntaxError`) eredményez.
* **Ciklusmag (behúzott sorok):** Az a kódrészlet, ami a ciklus minden egyes körében lefut.

---

## 2. A `range()` függvény szintaxisa (Számlálós ciklus)

Ha a `for` ciklust nem meglévő listán, hanem egy meghatározott darabszámú lépéssorozaton akarjuk végigfuttatni, a `range()` függvényt használjuk.

### Általános alak:

```python
range(start, stop, step)

```

### Paraméterek értelmezése:

* **`start` (kezdőérték):** *Opcionális.* A sorozat első száma. Ha elhagyjuk, az alapértelmezett érték: `0`.
* **`stop` (végérték):** **Kötelező.** A sorozat eddig a számig tart, de **ez az érték már NICS benne** a sorozatban (alulról zárt, felülről nyílt intervallum: $[start, stop)$).
* **`step` (lépésköz):** *Opcionális.* Két egymást követő szám közötti különbség. Alapértelmezetten: `1`.

### Szintaktikai példák:

```python
range(5)          # Generált értékek: 0, 1, 2, 3, 4
range(2, 6)       # Generált értékek: 2, 3, 4, 5
range(1, 10, 2)    # Generált értékek: 1, 3, 5, 7, 9

```

---

## 3. A `while` ciklus szintaxisa (Feltételes ciklus)

A `while` ciklus egy **elöltesztelő ciklus**. A ciklusmagban lévő utasítások addig ismétlődnek, amíg a ciklusfejben megadott logikai feltétel értéke `True` (igaz).

### Általános alak:

```python
while logikai_feltetel:
    # Ciklusmag (utasítások)
    # Feltételt befolyásoló változó módosítása

```

### A szintaktikai elemek részletezése:

* **`while` (kulcsszó):** Jelzi a feltételes ciklus kezdetét.
* **`logikai_feltetel` (kifejezés):** Egy olyan állítás vagy összefüggés, amelynek kiértékelése kizárólag `True` (igaz) vagy `False` (hamis) lehet (pl. `i < 10` vagy `valasz != "nem"`).
* **`:` (kettőspont):** A kódblokk nyitása (hasonlóan a `for` és `if` szerkezetekhez).
* **Változó módosítása a ciklusmagban:** A `while` szintaxisának logikai feltétele megköveteli, hogy a ciklusmagon belül **módosítsuk** a feltételben szereplő legalább egyik változót. Ennek hiányában a feltétel értéke soha nem változik `False`-ra, ami **végtelen ciklust** okoz.

---

## 4. A Python blokkszerkezete: Az Indentáció (Behúzás)

Sok más nyelvtől (C, C++, C#, Java) eltérően a Python **nem használ kapcsos zárójeleket `{}**` a kódblokkok határainak jelölésére. A blokkokat kizárólag a **behúzás (indentáció)** határozza meg.

### Szintaktikai szabályok:

1. A kettőspont (`:`) után következő sorokat beljebb kell húzni (alapértelmezetten **4 szóköz** vagy 1 tabulátor).
2. Mindegyik olyan sor, amely ugyanazon a behúzási szinten van, **ugyanahhoz a ciklusmaghoz** tartozik.
3. Amint visszaállunk az eredeti behúzási szintre, a ciklusmag véget ér.

### Példa a blokkszerkezetre:

```python
for i in range(3):
    print("Ez a ciklusmag belseje.")      # Ciklushoz tartozik
    print(f"Aktuális érték: {i}")         # Ciklushoz tartozik

print("Ez már a ciklus utáni sor.")      # NEM tartozik a ciklushoz (nincs behúzva)

```

Ha a behúzás pontatlan vagy hiányzik, a Python `IndentationError` hibaüzenettel leállítja a programot.

---

## 5. Ciklusvezérlő utasítások szintaxisa

Néha a ciklus normál lefutását fel kell függeszteni vagy módosítani kell. Erre két speciális kulcsszó szolgál:

### `break` (Megszakítás)

Azonnal kilép az adott ciklusból, a ciklusmag maradék része nem fut le, és a program a ciklus utáni első soron folytatódik.

```python
for szam in [1, 2, 3, 4, 5]:
    if szam == 3:
        break  # Amint a szám 3, a ciklus azonnal véget ér
    print(szam)

```

### `continue` (Lépés a következő iterációra)

Átugorja a ciklusmag **mögötte lévő** utasításait az aktuális körben, és azonnal a következő iterációra (lépésre) ugrik.

```python
for szam in [1, 2, 3, 4, 5]:
    if szam == 3:
        continue  # A 3-as számnál a print nem fut le, megy a 4-esre
    print(szam)

```

