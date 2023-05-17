# Testy pro modul Ankety 


## Test pro Usecase xyz
Vytvořil Pepa Novák

### Test conditions
C1 ... 

C2 ...

C3 ...

C4 ...


### Test cases
||||||
|---|---|---|---|---|
| ID | 1 ||||
| Title | Titulek ||||
| Priority | - ||||
| Preconditions | Vstupní podmínky ||||
| Postconditions | Výstupní podmínky ||||
| Role | Role ||||
| Test data | - ||||
| Covered test conditions | C1, C2 & C3 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Akce 1 | Výsledek 1 ||||
| 2 | Akce 2 | Výsledek 2 ||||
| 3 | Akce 3 | Výsledek 3 ||||
| 4 | Akce 4 | Výsledek 4 ||||


||||||
|---|---|---|---|---|
| ID | 2 ||||
| Title | Titulek ||||
| Priority | - ||||
| Preconditions | Vstupní podmínky ||||
| Postconditions | Výstupní podmínky ||||
| Role | Role ||||
| Test data | - ||||
| Covered test conditions | C4 ||||
| Test steps |||||
| Number | Action | Expected result | Result | Comment |
| 1 | Akce 1 | Výsledek 1 ||||
| 2 | Akce 2 | Výsledek 2 ||||
| 3 | Akce 3 | Výsledek 3 ||||
| 4 | Akce 4 | Výsledek 4 ||||

___

## Test pro Usecase "Zobrazit výsledky specifických anket učiteli"
Vytvořil Jan Jevčák

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

## Test pro Usecase Vytvořit specifickou anketu
Vytvořil Štof

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

____

## Test pro Usecase Vyplnit generickou anketu pro předmět
Vytvořila Nicol

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

## Test pro Zobrazení kalendář deadlinů učitel
Vytvořil Jan Svojanovský

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
