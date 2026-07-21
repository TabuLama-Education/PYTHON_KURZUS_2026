

## 2. Feladat: Csomagküldő logisztikai rendszer

Készíts egy programot, amely egy logisztikai cég automata raktárának működését szimulálja! A program ellenőrzi a futárok azonosítóját, a csomag méretét, és kiszámítja a szállítási díjat a távolság alapján.

### Adatok

```python
futarok = ["F01", "F02", "F03"]
elfogadott_csomagok = []  # Ide kerülnek a sikeres csomagok [futar_id, meret] formában

alap_szallitasi_dij = 1200  # Ft

```

### A program működése

1. **Adatbekérés és azonnali validálás:**
* Kérd be a **futár azonosítóját**. Ha a futár nincs a `futarok` listában, írd ki: `"Hibás futár azonosító!"`, és a program **azonnal lépjen ki**.
* Kérd be a **csomag méretét** (lehetséges értékek: `S`, `M`, `L`). Ha a megadott méret egyik sem ezek közül, írd ki: `"Nem támogatott csomagméret!"`, és a program **azonnal lépjen ki**.
* Kérd be a **szállítási távolságot** kilométerben (egész szám).


2. **Díj kalkuláció:**
* Ha a távolság **nagyobb, mint 50 km**, akkor a fizetendő díjhoz **adj hozzá 800 Ft** extra távolsági díjat.
* Ha a távolság 50 km vagy az alatti, nincs extra díj.


3. **Adatok rögzítése:**
* Mentse el a csomagot az `elfogadott_csomagok` listába `[futar_id, meret]` formátumban.


4. **Kimenet:**
* Írd ki a csomag regisztrációjának tényét, a végső szállítási díjat, valamint az összesített listát.



### Példa futásra 1 (Sikeres regisztráció extra díjjal)

```text
Futár azonosítója: F01
Csomag mérete (S/M/L): M
Szállítási távolság (km): 65

Csomag sikeresen regisztrálva!
Végső szállítási díj: 2000 Ft
Aktuális csomagok: [['F01', 'M']]

```

### Példa futásra 2 (Hibás méret miatti leállás)

```text
Futár azonosítója: F01
Csomag mérete (S/M/L): XL
Nem támogatott csomagméret!

```