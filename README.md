# Palmer Pingvinek Adat elemzése (Palmer Penguins Analysis)

Ez a projekt a **Palmer Penguins** adatbázis felfedező jellegű adatfeltárását (EDA - Exploratory Data Analysis) és vizualizációját tartalmazza Python környezetben, Jupyter Notebook segítségével.

---

## Projekt áttekintése

Az elemzés célja a Palmer-szigetcsoporton gyűjtött pingvinpopuláció morfológiai jellemzőinek, eloszlásának és a változók közötti összefüggéseknek a feltárása.

A vizsgált főbb kérdések:
1. Milyen alapstatisztikák jellemzik a pingvinek testtömegét a teljes populációban?
2. Melyik pingvinfaj rendelkezik a legnagyobb átlagos testtömeggel?
3. Van-e különbség a hímek és a nőstények csőrhossza között?
4. Melyik szigeten milyen fajok élnek és mekkora egyedszámban?
5. Függ-e egymástól az úszószárny hossza és a testtömeg?

---

## Használt technológiák és könyvtárak

* **Python 3.x**
* **Pandas**: Adatbetöltés, adattisztítás és aggregáció.
* **NumPy**: Statisztikai mutatók kiszámítása.
* **Plotly Express**: Interaktív adatvizualizáció (oszlopdiagramok, pontdiagramok).

---

## Elemzési lépések és eredmények

### 1. Adattisztítás
* **Hiányzó értékek eltávolítása**: Az eredeti adathalmazból a hiányzó értékeket tartalmazó sorok szűrésre kerültek (`dropna()`), így a tisztított adathalmaz **334 sorból** áll.

### 2. Testtömeg alapstatisztikák (Teljes populáció)
* **Átlagos testtömeg**: 4209.06 g
* **Medián testtömeg**: 4050.00 g
* **Szórás**: 803.63 g

### 3. Fajok szerinti átlagos testtömeg
* **Gentoo**: ~5090.63 g *(legnagyobb átlagos testtömegű faj)*
* **Chinstrap**: ~3733.09 g
* **Adelie**: ~3706.16 g

### 4. Nemi dimorfizmus (Csőrhossz)
* **Hímek (MALE)** átlagos csőrhossza: **45.85 mm**
* **Nőstények (FEMALE)** átlagos csőrhossza: **42.10 mm**

### 5. Szigetek és fajok eloszlása
* **Biscoe-sziget**: Gentoo (120), Adelie (44)
* **Dream-sziget**: Chinstrap (68), Adelie (55)
* **Torgersen-sziget**: Adelie (47)

### 6. Úszószárny hossz és testtömeg kapcsolata
* **Korrelációs együttható**: **0.87** (erős pozitív lineáris kapcsolat áll fenn az úszószárny hossza és a testtömeg között).

---

## Használat és futtatás

1. Telepítsd a szükséges függőségeket:
   ```bash
   pip install pandas numpy plotly notebook
   ```

2. Győződj meg róla, hogy a `penguins_size.csv` adatfájl a notebookkal azonos könyvtárban található.

3. Indítsd el a Jupyter Notebookot és futtasd a cellákat egymás után:
   ```bash
   jupyter notebook
   ```

---

## Adatforrás
* `penguins_size.csv`: Palmer Station, Antarctica LTER pingvin adatok.