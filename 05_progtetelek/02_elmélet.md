## 7. Másolás tétele

### Leírás

A tétel során egy meglévő sorozat minden egyes elemét valamilyen szabály vagy művelet alapján átalakítjuk, és az eredményeket egy új sorozatba (listába) másoljuk át egy az egyben.

### Alap példa

Nettó árak átalakítása 27%-os bruttó árakká:

```python
netto_arak = [1000, 2500, 5000, 10000]

brutto_arak = []
for ar in netto_arak:
    brutto_ar = int(ar * 1.27)
    brutto_arak.append(brutto_ar)

print(f"Bruttó árak: {brutto_arak}")

```

### Több feltételes példa

Fizetések emelése: Csak azoknak a dolgozóknak emeljük meg a fizetését 15%-kal, akiknek a jelenlegi fizetésük **300 000 Ft alatti ÉS legalább 3 éve** a cégnél dolgoznak. A többiek fizetése változatlan marad:

```python
# Szerkezet: [név, fizetés, tapasztalat_években]
dolgozok = [
    ["Péter", 250000, 3],
    ["Anna", 450000, 5],
    ["Gábor", 280000, 1],
    ["Éva", 290000, 4]
]

uj_fizetesek = []
for ember in dolgozok:
    nev = ember[0]
    fizetes = ember[1]
    tapasztalat = ember[2]
    
    if fizetes < 300000 and tapasztalat >= 3:
        uj_fizetes = int(fizetes * 1.15)
    else:
        uj_fizetes = fizetes
        
    uj_fizetesek.append([nev, uj_fizetes])

print(f"Új fizetések listája: {uj_fizetesek}")

```

---

## 8. Szétválogatás tétele

### Leírás

Egy forráslista elemeit egy megadott feltétel alapján **két különálló listába** osztjuk szét (például: sikeres/sikertelen, páros/páratlan, megfelel/nem felel meg).

### Alap példa

Pozitív és negatív számok szétválogatása két külön listába:

```python
szamok = [12, -5, 0, 7, -3, 18, -1]

pozitivak = []
negativak = []

for szam in szamok:
    if szam >= 0:
        pozitivak.append(szam)
    else:
        negativak.append(szam)

print(f"Pozitív számok és nulla: {pozitivak}")
print(f"Negatív számok: {negativak}")

```

### Több feltételes példa

Diákok szétválogatása ösztöndíjas és pótlehetőségest igénylő csoportra. Ösztöndíjas az, akinek az **átlaga legalább 4.0 ÉS a hiányzása legfeljebb 10 óra**:

```python
# Szerkezet: [név, átlag, hiányzás]
diakok = [
    ["Anna", 4.8, 2],
    ["Bence", 3.8, 15],
    ["Csilla", 4.2, 5],
    ["Dávid", 4.9, 12]
]

osztondijasok = []
tobbiek = []

for diak in diakok:
    nev = diak[0]
    atlag = diak[1]
    hianyzas = diak[2]
    
    if atlag >= 4.0 and hianyzas <= 10:
        osztondijasok.append(nev)
    else:
        tobbiek.append(nev)

print(f"Ösztöndíjra jogosultak: {osztondijasok}")
print(f"Ösztöndíjból kimaradók: {tobbiek}")

```

---

## 9. Metszet tétele

### Leírás

Két meglévő sorozat (lista) **közös elemeit** gyűjtjük ki egy harmadik listába. Azokat az elemeket keressük, amelyek az első és a második listában is szerepelnek.

### Alap példa

Két számlista közös elemeinek megkeresése:

```python
lista_a = [1, 3, 5, 7, 9, 11]
lista_b = [3, 6, 7, 10, 11, 14]

metszet = []
for elem in lista_a:
    if elem in lista_b:
        metszet.append(elem)

print(f"A két lista közös elemei: {metszet}")

```

### Több feltételes példa

Két üzlet kínálatából azoknak a termékeknek a kigyűjtése, amelyek **mindkét boltban kaphatók ÉS mindkét helyen az áruk 2000 Ft alatt van**:

```python
# Szerkezet: [terméknév, ár]
bolt_a = [
    ["Tej", 400],
    ["Kenyér", 700],
    ["Sajt", 1800],
    ["Kávé", 2500]
]

bolt_b = [
    ["Sajt", 1900],
    ["Kávé", 2200],
    ["Kenyér", 750],
    ["Csoki", 500]
]

kozos_olcsok = []

for termek_a in bolt_a:
    nev_a = termek_a[0]
    ar_a = termek_a[1]
    
    for termek_b in bolt_b:
        nev_b = termek_b[0]
        ar_b = termek_b[1]
        
        if nev_a == nev_b and ar_a < 2000 and ar_b < 2000:
            kozos_olcsok.append(nev_a)

print(f"Mindkét boltban kapható, 2000 Ft alatti termékek: {kozos_olcsok}")

```

---

## 10. Unió tétele

### Leírás

Két sorozat elemeit egyesítjük egyetlen közös listába úgy, hogy a **duplikációkat kiszűrjük** (egy elem csak egyszer szerepelhet a végeredményben).

### Alap példa

Két lista egyesítése ismétlődések nélkül:

```python
lista_a = [1, 2, 3, 4, 5]
lista_b = [4, 5, 6, 7, 8]

unio = []

for elem in lista_a:
    unio.append(elem)

for elem in lista_b:
    if elem not in unio:
        unio.append(elem)

print(f"A két lista uniója (ismétlődés nélkül): {unio}")

```

### Több feltételes példa

Két klub tagjainak egyesítése egy közös listába duplikáció nélkül, de csak azokat gyűjtjük be, akik **2020 után csatlakoztak ÉS aktívak**:

```python
# Szerkezet: [név, csatlakozás_éve, aktív_tag]
klub_1 = [
    ["Kovács Péter", 2021, True],
    ["Nagy Anna", 2019, True],
    ["Szabó Gábor", 2022, False]
]

klub_2 = [
    ["Kovács Péter", 2021, True],
    ["Tóth Éva", 2023, True]
]

egyesitett_tagok = []

# Első klub szűrése
for tag in klub_1:
    nev = tag[0]
    ev = tag[1]
    aktiv = tag[2]
    
    if ev >= 2020 and aktiv == True:
        egyesitett_tagok.append(nev)

# Második klub szűrése duplikáció-ellenőrzéssel
for tag in klub_2:
    nev = tag[0]
    ev = tag[1]
    aktiv = tag[2]
    
    if ev >= 2020 and aktiv == True and nev not in egyesitett_tagok:
        egyesitett_tagok.append(nev)

print(f"A szűrt, egyesített aktív tagok listája: {egyesitett_tagok}")

```

---

## 11. Egyszerű cserés rendezés

### Leírás

A sorozat elemeit növekvő vagy csökkenő sorrendbe állítjuk. Egymás után összehasonlítjuk az elemeket, és ha nincsenek a helyes sorrendben, kicseréljük őket.

### Alap példa

Számok rendezése növekvő sorrendbe:

```python
szamok = [42, 12, 88, 3, 25]

for i in range(len(szamok)):
    for j in range(i + 1, len(szamok)):
        if szamok[i] > szamok[j]:
            temp = szamok[i]
            szamok[i] = szamok[j]
            szamok[j] = temp

print(f"Rendezett számok (növekvő): {szamok}")

```

### Több feltételes (összetett) példa

Versenyzők rendezése **elsődlegesen pontszám szerint csökkenő** sorrendbe. Ha két versenyzőnek **ugyanannyi a pontszáma, akkor a koruk alapján növekvő** sorrendbe állítjuk őket (a fiatalabb előrébb kerül):

```python
# Szerkezet: [név, pontszám, kor]
versenyzok = [
    ["Péter", 85, 20],
    ["Anna", 95, 22],
    ["Gábor", 85, 18],
    ["Éva", 95, 19]
]

for i in range(len(versenyzok)):
    for j in range(i + 1, len(versenyzok)):
        pont_i = versenyzok[i][1]
        kor_i = versenyzok[i][2]
        
        pont_j = versenyzok[j][1]
        kor_j = versenyzok[j][2]
        
        # Cserélünk, ha j-nek TÖBB pontja van, VAGY ugyanannyi pontjuk van, de j FIATALABB
        if pont_j > pont_i or (pont_i == pont_j and kor_j < kor_i):
            temp = versenyzok[i]
            versenyzok[i] = versenyzok[j]
            versenyzok[j] = temp

print("Rendezett versenyzők listája (Pont csökkenő, azonos pontnál kor növekvő):")
for v in versenyzok:
    print(f"{v[0]} - Pont: {v[1]}, Kor: {v[2]}")

```