# Programozási tételek

> A programozási tételek olyan alapvető algoritmusok (megoldási minták), amelyekkel a leggyakoribb adatfeldolgozási feladatokat tudjuk megoldani.

---

## 1. Összegzés tétele

### Leírás

A tétel célja egy sorozat (lista) elemeinek összeadása. Szükségünk van egy `osszeg` nevű változóra, amit a ciklus előtt **0-ra** inicializálunk, majd a ciklusban minden elemet hozzáadunk.

### Alap példa

Egy számokat tartalmazó lista elemeinek összeadása:

```python
szamok = [4, 7, 2, 9, 1]

osszeg = 0
for szam in szamok:
    osszeg = osszeg + szam

print(f"A számok összege: {osszeg}")

```

### Több feltételes példa

A listából csak azoknak a számoknak az összeadása, amelyek **párosak ÉS nagyobbak 10-nél**:

```python
szamok = [12, 5, 24, 8, 15, 30, 3]

osszeg = 0
for szam in szamok:
    if szam % 2 == 0 and szam > 10:
        osszeg = osszeg + szam

print(f"A 10-nél nagyobb páros számok összege: {osszeg}")

```

---

## 2. Megszámlálás tétele

### Leírás

A tétel megadja, hogy egy sorozatban hány darab adott feltételnek megfelelő elem található. Egy `darab` változót **0-ról** indítunk, és valahányszor a feltétel teljesül, megnöveljük az értékét 1-gyel.

### Alap példa

Megszámoljuk, hány fagyos nap volt (0 fok alatti hőmérséklet):

```python
homersekletek = [-2, 3, -5, 0, 8, -1]

fagyos_napok = 0
for fok in homersekletek:
    if fok < 0:
        fagyos_napok = fagyos_napok + 1

print(f"Fagyos napok száma: {fagyos_napok}")

```

### Több feltételes példa

Megszámoljuk, hány olyan dolgozat van, aminek a pontszáma **50 és 80 közé esik ÉS páros szám**:

```python
pontszamok = [45, 82, 90, 60, 52, 77, 64]

megfelelo_db = 0
for pont in pontszamok:
    if pont >= 50 and pont <= 80 and pont % 2 == 0:
        megfelelo_db = megfelelo_db + 1

print(f"A feltételeknek megfelelő dolgozatok száma: {megfelelo_db}")

```

---

## 3. Eldöntés tétele

### Leírás

Azt vizsgáljuk, hogy a sorozatban **van-e legalább egy** olyan elem, amely megfelel a feltételnek. Egy logikai változót (`False`) használunk. Amint találunk egy megfelelő elemet, átállítjuk `True`-ra, és a `break` utasítással azonnal kilépünk a ciklusból, hiszen felesleges tovább keresni.

### Alap példa

Van-e páratlan szám a listában:

```python
szamok = [2, 4, 6, 9, 10, 12]

van_paratlan = False
for szam in szamok:
    if szam % 2 != 0:
        van_paratlan = True
        break

if van_paratlan:
    print("Van páratlan szám a listában.")
else:
    print("Nincs páratlan szám a listában.")

```

### Több feltételes példa

Van-e olyan személy, aki **18 évnél idősebb ÉS nincs jogosítványa**:

```python
# Szerkezet: [kor, van_jogositvany]
szemelyek = [[16, False], [22, True], [19, False], [25, True]]

van_megfelelo = False
for szemely in szemelyek:
    kor = szemely[0]
    jogsi = szemely[1]
    
    if kor >= 18 and jogsi == False:
        van_megfelelo = True
        break

if van_megfelelo:
    print("Van legalább egy 18 év feletti, jogosítvány nélküli személy.")
else:
    print("Nincs ilyen személy az adatok között.")

```

---

## 4. Kiválogatás tétele

### Leírás

Az adatok közül kigyűjtjük egy **új listába** azokat az elemeket, amelyek megfelelnek a megadott feltételnek.

### Alap példa

A pozitív számok kigyűjtése egy külön listába:

```python
szamok = [-3, 5, 0, -8, 12, 7]

pozitivak = []
for szam in szamok:
    if szam > 0:
        pozitivak.append(szam)

print(f"A pozitiv számok listája: {pozitivak}")

```

### Több feltételes példa

Azoknak a diákoknak a kigyűjtése, akiknek az **átlaga legalább 4.5 ÉS a hiányzásuk legfeljebb 5 óra**:

```python
# Szerkezet: [név, átlag, hiányzott_órák]
diakok = [
    ["Anna", 4.8, 2],
    ["Bence", 4.2, 12],
    ["Cecília", 4.9, 0],
    ["Dávid", 4.6, 8]
]

osztondijasok = []
for diak in diakok:
    nev = diak[0]
    atlag = diak[1]
    hianyzas = diak[2]
    
    if atlag >= 4.5 and hianyzas <= 5:
        osztondijasok.append(nev)

print(f"Ösztöndíjra jogosult diákok: {osztondijasok}")

```

---

## 5. Lineáris keresés tétele

### Leírás

A keresés tételénél nemcsak azt akarjuk megtudni, hogy létezik-e az elem, hanem **meg akarjuk határozni annak pozícióját (indexét vagy sorszámát)**, vagy magát az objektumot. Amint megtaláljuk az első megfelelőt, a ciklust leállítjuk.

### Alap példa

Megkeressük az első `0` érték indexét a listában:

```python
szamok = [15, 8, 0, 23, 0, 4]

keresett_index = -1
for i in range(len(szamok)):
    if szamok[i] == 0:
        keresett_index = i
        break

if keresett_index != -1:
    print(f"A nullás érték első előfordulási helye (indexe): {keresett_index}")
else:
    print("Nem található 0 a listában.")

```

### Több feltételes példa

Megkeressük az első olyan terméket, aminek az **ára 5000 Ft alatti ÉS raktáron van**:

```python
# Szerkezet: [terméknév, ár, raktáron_van_e]
termekek = [
    ["Kabát", 25000, True],
    ["Cipő", 12000, False],
    ["Zokni", 1200, True],
    ["Póló", 4500, True]
]

talalt_termek = None
for termek in termekek:
    nev = termek[0]
    ar = termek[1]
    raktaron = termek[2]
    
    if ar < 5000 and raktaron == True:
        talalt_termek = nev
        break

if talalt_termek != None:
    print(f"Az első megfelelő olcsó, raktáron lévő termék: {talalt_termek}")
else:
    print("Nincs a feltételeknek megfelelő termék.")

```

---

## 6. Szélsőérték-meghatározás (Maximum/Minimum kiválasztás)

### Leírás

A sorozat legnagyobb (vagy legkisebb) elemét keressük. Kezdésként a feltételezett maximumot **a lista legelső elemére** (`lista[0]`) állítjuk be. Ezután a ciklussal végigmegyünk a többi elemen, és ha találunk akkorit, ami nagyobb az addigi maximumunknál, felülírjuk a változó értékét.

### Alap példa

A legnagyobb szám megkeresése:

```python
szamok = [14, 52, 9, 83, 31]

legnagyobb = szamok[0]
for szam in szamok:
    if szam > legnagyobb:
        legnagyobb = szam

print(f"A legnagyobb szám a listában: {legnagyobb}")

```

### Több feltételes példa

A **legidősebb AKTÍV** klubtag megkeresése (akinek az állapota `True`):

```python
# Szerkezet: [név, kor, aktív_tag]
tagok = [
    ["Éva", 25, False],
    ["Gábor", 62, False],
    ["Kati", 50, True],
    ["Péter", 38, True]
]

legidosebb_nev = ""
max_kor = -1

for tag in tagok:
    nev = tag[0]
    kor = tag[1]
    aktiv = tag[2]
    
    if aktiv == True and kor > max_kor:
        max_kor = kor
        legidosebb_nev = nev

if legidosebb_nev != "":
    print(f"A legidősebb aktív tag: {legidosebb_nev} ({max_kor} éves)")
else:
    print("Nincs egyetlen aktív tag sem.")

```