# Testy pro modul Ankety 

## Test pro Usecase "Zobrazit výsledky specifických anket učiteli"
Vytvořil Jan Jevčák

### Originální usecase
- Počáteční stav: 
  - Učitel vytvořil specifickou anketu, studenti ji vyplnili, čas je před/po deadlinu
- Normální interakce:
  - Učitel se přihlásí do systému.
  - Učitel otevře modul anket a rozevře specifické ankety.
  - Systém zobrazí učitelovi seznam všech jeho specifických anket pro daný semestr.
  - Učitel může seznam filtrovat pomocí filtru anket.
  - Učitel najde a otevře žádanou specifickou anketu k zobrazení.
  - Systém zobrazí odpovědi studentů na specifickou anketu.

- Chybové situace:
  - Žádné odpovědi pro daný předmět a dané období neexistují.

- Koncový stav:
  - Systém zobrazí učiteli odpovědi pro vybranou specifickou anketu.

### Test conditions
C1 Anketa je vytvořena

C2 Anketa není vytvořena

C3 Učitel se úspěšně přihlásí do systému

C4 Učiteli se nepodaří přihlásit do systému

C5 Otevření modulu anket

C6 Zobrazení všech anket

C7 Zovrazení jedné ankety použitím filtrování

C8 Zovbrazení více anket použitím filtrování

C9 Zobrazení odpovědí pro anketu


### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Zobrazení ankety jednoho předmětu ||||
| Priority | - ||||
| Preconditions | Anketa je vytvořena ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C3, C5, C7 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uživatel načte v prohlížeči stránku SISu | Systém zobrazí domovskou obrazovku SISu ||||
| 2 | Uživatel zadá své přihlašovací jméno a heslo, klikne na tlačítko [Přihlásit] | Systém uživatele přihlásí ||||
| 3 | Uživatel klikne na tlačítko [Anketa] | Systém zobrazí seznam dostupných anket ||||
| 4 | Uživatel vyhledá anketu pro předmět [Úvod do softwarového inženýrství] | Systém zobrazí výsledky vyhledávání. ||||
| 5 | Uživatel zkontroluje vyhledané výsledky. | Systém zobrazil jeden výsledek - předmět "Úvod do sofwarového inženýrství" ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Zobrazení výsledků ankety ||||
| Priority | - ||||
| Preconditions | Existuje jedna anketa s dvěma odpověďmi studentů ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C3, C5, C6, C9 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uživatel načte v prohlížeči stránku SISu | Systém zobrazí domovskou obrazovku SISu ||||
| 2 | Uživatel zadá své přihlašovací jméno a heslo, klikne na tlačítko [Přihlásit] | Systém uživatele přihlásí ||||
| 3 | Uživatel klikne na tlačítko [Anketa] | Systém zobrazí seznam dostupných anket ||||
| 4 | Uživatel zkontroluje zobrazené ankety | Je zobrazena jedna anketa ||||
| 5 | Uživatel klikne na první zobrazenou anketu | Systém zobrazí odpovědi pro danou anketu ||||
| 6 | Uživatel zkontroluje odpovědi pro danou anketu | Daná anketa obsahuje právě 2 odpovědi ||||

___
___

## Test pro Usecase Vytvořit specifickou anketu
Vytvořil Kryštof Žucha

### Originální usecase
- Počáteční stav:
  - Učitel učí alespoň jeden předmět v daném semestru.
- Normální interakce:
  - Učitel se přihlásí do systému a otevře modul anket.
  - Systém zobrazí seznam předmětů, které učitel učí v aktuálním semestru.
  - Učitel vybere předmět, ke kterému chce anketu vytvořit.
  - Učitel vytvoří nějaké číselné otázky a nějaké slovní otázky. V případě slovní otázky si může zaškrtnout filtrování obsahu (obsahuje např. smazání sprostých slov). U každé otázky si může zaškrtnout, jestli je povinná.
  - Učitel nastaví deadline pro vyplnění a pošle anketu ke zpracování.
  - Systém ověří, že anketa obsahuje alespoň jednu otázku a že deadline pro vyplnění je dřív než konec aktuálního semestru.
  - Systém anketu zaznamená, přidá ji do kalendáře deadlinů učiteli a studentům daného předmětu a zpřístupní jim vyplnění.
- Alternativní scénář:
  - Učitel žádný předmět neučí, nelze pokračovat v postupu.
  - Pokud anketa žádnou otázku neobsahuje, vrací se učitel do bodu číslo 4.
  - Pokud je deadline až po konci semestru, vrací se učitel do bodu 5.
- Koncový stav:
  - Anketa je zaznamenána v systému.
  - Začne se zobrazovat v seznamu anket pro daný předmět daným studentům a v kalendáři deadlinů.

### Test conditions
C1 - Učitel se dokáže přihlásit do systému 

C2 - Učitel dokáže otevřít anketní modul

C3 - Systém vypíše všechny učitelem vyučované předměty

C4 - Učitel dokáže zvolit svůj předmět a založit pro něj specifickou anketu

C5 - Učitel dokáže vytvořit číselnou otázku

C6 - Učitel dokáže vytvořit textovou otázku

C7 - Učitel dokáže nastavit otázkám parametry
   - C7a - otázka má zadání
   - C7b - otázka má parametr povinnosti vyplnit
   - C7c - textové otázce lze nastavit filtr zabanovaných slov

C8 - Učitel dokáže anketě parametr - deadline

C9 - Učitel dokáže anketu odeslat ke zpracování

C10 - Systém dokáže ověřit korektnost přijaté ankety
   - C10a - anketa obsahuje alespoň 1 otázku
   - C10b - deadline ankety se nachází v budoucnu
   - C10c - každá otázka má zadání

C11 - Systém vrátí učiteli přijatou nekorektní anketu k opravě

C12 - Systém přijatou korektní anketu zařadí do paměti, a zpřístupní ji k vyplnění zapsaným studentům

<br>

### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Vytvoření korektní ankety ||||
| Priority | Normal ||||
| Preconditions | Učitel, jež vyučuje aspoň 1 předmět, je přihlášen v systému a má otevřen modul ankety ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C3, C4, C5, C7a, C8, C9, C10, C12 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Učitel klikne na tlačítko výpis předmětů | Zobrazí se seznam předmětů, jež učitel vyučuje. Díky Preconditions alespoň jeden takový existuje ||||
| 2 | Učitel vybere první předmět v seznamu a stiskne volbu "Vytvořit specifickou anketu" | Zobrazí se prostředí tvorby specifické ankety ||||
| 3 | Učitel vytvoří číselnou otázku, ke které napíše zadání "Test1" | Otázka je přidána ||||
| 4 | Učitel nastaví deadline na zítřejší datum | Parametr deadline je nastaven ||||
| 5 | Učitel stiskne tlačítko odeslání otázky | Otázka je odesílána do systému. Ovládací prvky zešednou ||||
| 6 | Systém provede ověření přijaté ankety | Anketa je ověřena a vyhodnocena jako korektní ||||
| 7 | Systém anketu uveřejní | Učitel je přesměrován zpět na domovskou stránku modulu Ankety. Anketa je uveřejněna v systému ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Vytvoření zcela nekorektní ankety ||||
| Priority | Normal ||||
| Preconditions | Učitel, jež vyučuje aspoň 1 předmět, je přihlášen v systému a má otevřen modul ankety ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C3, C4, C9, C10, C11 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Učitel klikne na tlačítko výpis předmětů | Zobrazí se seznam předmětů, jež učitel vyučuje. Díky Preconditions alespoň jeden takový existuje ||||
| 2 | Učitel vybere první předmět v seznamu a stiskne volbu "Vytvořit specifickou anketu" | Zobrazí se prostředí tvorby specifické ankety ||||
| 4 | Učitel stiskne tlačítko odeslání otázky | Otázka je odesílána do systému. Ovládací prvky zešednou ||||
| 5 | Systém provede ověření přijaté ankety | Anketa je ověřena a vyhodnocena jako nekorektní ||||
| 6 | Systém anketu vrátí k opravě | Ovládací prvky se znovu zaktivují a učiteli je vypsána hláška, že anketa neobsahuje žádnou otázku a že nemá nastaven validní deadline ||||

___
___

## Test pro Usecase Vyplnit generickou anketu pro předmět
Vytvořila Nicol Čačalová

### Originální usecase
- Počáteční stav:
  - Generické ankety byly vytvořeny systémem.
  - Je období vyplňování anket.
  - Student je zapsaný do daného předmětu.
- Normální interakce:
  - Student se přihlásí do systému.
  - Student otevře modul anket.
  - Modul anket zobrazí studentovi seznam všech anket.
  - Student může seznam filtrovat pomocí filtru anket.
  - Student najde a otevře žádanou generickou anketu pro předmět k vyplnění.
  - Student anketu vyplní, zvolí si, zda chce mít odpovědi anonymizovány a jestli si jeho odpovědi mohou zobrazit i studenti.
  - Student vyplněnou anketu odešle.
  - Systém zkontroluje, zda jsou všechna povinná pole vyplněna.
  - Systém odpovědi zaznamená.
- Chybové situace:
  - Neexistují žádné ankety odpovídající filtru, které student může vyplnit. Systém toto oznámí.
  - Student nevyplní odpověď na povinnou otázku.
  - Systém zobrazí rozpracovanou anketu a zvýrazní místo, kde chybí odpověď.
- Koncový stav:
  - Anketa je zaznamenána v systému.
  - Začne se zobrazovat v seznamu odpovědí podle volby anonymizace.

### Test conditions
C1 Anketa sa vytvorila 

C2 Dnesny datum nie je skorsi nez datum vyplnovania

C3 Dnesny datum nie je neskorsi nez datum vyplnovania

C4 student je zapisany na predmet

C5 student je prihlaseny v systeme

C6 spravne sa ukazuju vsetky ankety

C7 filter zonamu ankiet funguje spravne

C8 otvorí sa spravna anketa

C9 anketa sa vsetkym zobrazuje anonymne

C10 Ostatny studenti vidia ankety odkliknute ako viditelne

C11 Ostatny studenti nevidia ankety neodkliknute ako viditelne

C12 anketa sa odoslala

C13 povinne polia ankety su vyplnene 

C14 system spravne zobrazuje uz v minulosti rozpracovanu anketu

C15 chybajuca odpoved v ankete je zvyraznena

C16 vsetky odpovede studenta su zaznamenane

C17 filter neobsahujuci ziadne ankety da oznamenie

C18 odpovede sa zobrazuju vyucujucim

### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Student si zobrazuje vsetky zverejnene odpovede k danej ankete ||||
| Priority | High ||||
| Preconditions | Student je prihlaseny do SISu, anketa ma odoslanych niekolko typov odpovedi od inych studentov - niektore su anonymne, neverejne ||||
| Postconditions | Výstupní podmínky ||||
| Role | Student ||||
| Test data | - ||||
| Covered test conditions | C8, C9, C10, C11 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uzivatel otvori stranku v SISe s anketami | Je nacitana stranka pro ankety ||||
| 2 | Uzivatel klikne na konkretnu anketu ktoru chce zobrazit | Zobrazi sa obsah spravnej ankety ||||
| 3 | Uzivatel stlaci tlacidlo "zobrazit odpovede" | Zobrazi sa zoznam odoslanych odpovedi ktore su verejne a kde niektory autori su anonymny ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Student pri vyplnani ankety nevyplni povinne policko ||||
| Priority | High ||||
| Preconditions | Student je prihlaseny,je obdobie vyplnovania||||
| Postconditions | Výstupní podmínky ||||
| Role | Student ||||
| Test data | - ||||
| Covered test conditions | C13, C14, C15 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uzivatel otvori stranku pre ankety v sise| Prehlidac otvori pozadovanu stranku a zobrazi zoznam ankiet ||||
| 2 | Uzivatel klikne na konkretnu anketu | Otvori sa mu anketa s otazkami a uz vyplnenymi odpovedmi z minulosti - ak este neboli vyplnene tak bez odpovede ||||
| 3 | Uzivatel ciastocne vyplni anketu a vynecha 1 povinnu odpoved | stranka zobrazuje vsetky jeho odpovede na otazky v ankete ||||
| 4 | Uzivatel odosle odpovede | system ho vrati na anketu obsahujucu odpovede ktore vyplnil pred odoslanim a zvyrazni vynechanu povinnu otazku ||||

___
___


## Test pro Usecase Zobrazení kalendáře deadlinů učitelem
Vytvořil Jan Svojanovský

### Originální usecase
- Počáteční stav:
  - Učitel je přihlášený do systému.
- Normální interakce:
  - Učitel otevře modul anket v něm rozklikne kalendář deadlinů.
  - Systém zobrazí učitelovi tabulku kalendáře s deadliny pro daný měsíc.
  - Učitel najede myší na anketu v některém dni.
  - Systém zobrazí drobné vyskakovací okénko s informacemi o anketě.
  - Učitel klikne na některou z anket v kalendáři.
  - Učitel může prodloužit deadline pro nakliklou anketu.
  - Učitel si může prohlédnout doposud odeslané odpovědi na specifické ankety.
- Alternativní scénář:
  - Učitel otevře modul anket v něm rozklikne kalendář deadlinů, a zvolí možnost "zobrazit jako seznam".
  - Systém zobrazí učitelovi seznam anket řazených podle data deadlinu (bez funkce kalendáře).
  - Není žádná anketa k zobrazení.
- Koncový stav:
  - Učitel zjistil deadliny jím zadaných specifických anket a případně některé z nich prodloužil, či si přečetl vyplněné ankety.

### Test conditions
C1 Otevření kalendáře deadlinů 

C2 Zobrazení všech deadlinů pro daný měsíc

C3 Zobrazení všech deadlinů v jiném měsíci

C4 Změnit datum deadline pro danou anketu

C5 Přehled prozatimních odpovědí na anketu

C6 Podle mě můžu překopírovat půlku věcí co má písek IDK


### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Zobrazení kalendáře deadline ||||
| Priority | - ||||
| Preconditions | Anketa je vytvořena ||||
| Postconditions | - ||||
| Role | Učitel ||||
| Test data | - ||||
| Covered test conditions | C1, C2 & C3 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uživatel načte v prohlížeči stránku SISu | Systém zobrazí domovskou obrazovku SISu |||
| 2 | Uživatel zadá své přihlašovací jméno a heslo, klikne na tlačítko [Přihlásit] | Systém uživatele přihlásí |||
| 3 | Uživatel klikne na tlačítko [Anketa] | Systém zobrazí seznam dostupných anket |||
| 4 | Uživatel klikne na tlačítko [deadliny] | Systém zobrazí nabídku měsíců |||
| 5 | Uživatel klikne na tlačítko [zobrazit] | Systém zobrazí deadliny anket pro daný měsíc |||

||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Zobrazení prozatimních výsledků ankety ||||
| Priority | - ||||
| Preconditions | Anketa je vytvořena ||||
| Postconditions |  ||||
| Role | učitel ||||
| Test data | - ||||
| Covered test conditions | C5 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Uživatel načte v prohlížeči stránku SISu | Systém zobrazí domovskou obrazovku SISu |||
| 2 | Uživatel zadá své přihlašovací jméno a heslo, klikne na tlačítko [Přihlásit] | Systém uživatele přihlásí |||
| 3 | Uživatel klikne na tlačítko [Anketa] | Systém zobrazí seznam dostupných anket |||
| 4 | Uživatel vybere konkrétní anketu a klikne na zobrazit výsledky | Systém zobrazí prozatimní výsledky ankety |||

___
___

## Test pro Usecase Vytvoření generické ankety
Vytvořil Jaroslav Švarc

### Originální usecase
- Počáteční stav:
  - Zkouškové období semestru, pro který chceme vytvořit generické ankety, doposud nezapočalo.
- Normální interakce:
  - Vedoucí katedry se přihlásí do systému.
  - Vedoucí katedry otevře modul anket a přesune se do části pro vytváření anket.
  - Vedoucí katedry vytvoří číselné a slovní otázky a u každé si zvolí, zda-li je povinná. V případě slovních otázek si navíc může zaškrtnout filtrování dle obsahu (například cenzura vulgarismů).
  - Systém ověří, že anketa obsahuje alespoň jednu otázku.
  - Vedoucí katedry explicitně zvolí předměty, pro které se ankety generovat nemají.
  - Systém si uloží generickou anketu a na začátku zkouškového období vytvoří tuto anketu pro všechny vyučované předměty, zpřístupní ji studentům k vyplnění a přidá velký červený banner do kalendáře deadlinů.
- Alternativní scénář:
  - Pokud vedoucí katedry explicitně nevytvoří otázky pro ankety, použijí se defaultní.
  - Vedoucí katedry se pokusí ankety zadat po začátku zkouškového období. Systém nedovolí přistoupit na formulář pro vygenerování generických anket neboť právě probíhají.
  - Vedoucí katedry nezadal žádnou otázku. Systém ho upozorní a požádá o nápravu.
- Koncový stav:
  - Systém má seznam otázek pro generické ankety, které se zobrazí na začátku zkouškového období u všech předmětů vyučovaných v daném semestru, které nebyly explicitně vyfiltrovány Vedoucím katedry.

### Test conditions
C1 - Není zkouškové období

C2 - Je zkouškové období

C3 - Vedoucí katedry je přihlášen do systému

C4 - Vedoucí katedry není přihlášen do systému

C5 - Vedoucí katedry otevře modul anket 

C6 - Vedoucí katedry se přesune do části pro vytváření anket

C7 - Vedoucí katedry vytvoří číselnou otázku

C8 - Vedoucí katedry vytvoří slovní otázku

C9 - Vedoucí katedry nevytvoří žádnou otázku

C10 - U otázky lze zvolit, zda-li je otázka povinná

C11 - U otázky lze nastavit filtrování obsahu

C12 - Anketa obsahuje alespoň jednu otázku 

C13 - Je možné vyřadit některé předměty z ankety

C14 - Systém si uloží generickou anketu

C15 - Na začátku zkouškového období vytvoří systém anketu pro všechny vyučované  předměty, 

C16 - Na začátku zkouškového období zpřístupní nově vytvořenou anketu studentům k vyplnění

C17 - Na začátku zkouškového období přidá velký červený banner do kalendáře deadlinů

C18 - Vedoucí katedry se pokusí ankety zadat po začátku zkouškového období

C19 - Vedoucí katedry se pokusí ankety zadat před začátkem zkouškového období

C20 - Systém nedovolí přistoupit na formulář pro vygenerování generických anket neboť právě probíhají

### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Vytvoření ankety s povinnou slovní otázkou ||||
| Priority | - High ||||
| Preconditions | Zkouškové období semestru, pro který chceme vytvořit generické ankety, doposud nezapočalo||||
| Postconditions | Anketa vytvořena||||
| Role | Vedoucí katedry ||||
| Test data | - ||||
| Covered test conditions | C3, C5, C6, C8, C10, C12, C14,  ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Vedoucí katedry se přihlásí do systému  | Vedoucí katedry je přihlášen  ||||
| 2 | Vedoucí katedry otevře modul anket  | Modul je úspěšně otevřen ||||
| 3 | Vedoucí katedry se přesune do části pro vytváření anket | Šablona ankety úspěšně otevřena ||||
| 4 |Vedoucí katedry přidá slovní otázku| Otázka úspěšně přidána ||||
| 5 |Vedoucí katedry označí otazku jako povinnou| Otázka je nastavena jako povinná ||||
| 6 |Vedoucí katedry uloží anketu| Anketa zkontroluje existenci alespoň jedné otázky a anketa je uložena ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Neúspěšné vytvoření ankety ||||
| Priority | - High ||||
| Preconditions | Je zkouškové období a právě probíhají ankety ||||
| Postconditions | Systém nedovolí vytvořit anketu pro současné zkouškové období ||||
| Role | Vedoucí katedry ||||
| Test data | - ||||
| Covered test conditions | C2, C3, C5, C6, C18, C20  ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Vedoucí katedry se přihlásí do systému  | Vedoucí katedry je přihlášen  ||||
| 2 | Vedoucí katedry otevře modul anket  | Modul je úspěšně otevřen ||||
| 3 | Vedoucí katedry se přesune do části pro vytváření anket | Systém zamítne vytvořit anketu pro dané zkouškové období ||||
