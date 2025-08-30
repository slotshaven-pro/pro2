 # Introduktion til Python
Programmering B

Vi bruger Python til at lære programmering.

## Oversigt
Vi skal lære om:

- syntaks
- blokke
- simple datatyper som heltal, tekst og sand-falsk

Vi skal bruge følgende værktøjer og programmer:

- en kodeeditor (IDE)
- en kommandolinje (CLI)
- Python 3

&#x24D8; **IDE** er et akronym for _Integrated Development Environment_. Altså, en kodeeditor, det program som vi skriver vores programmer i. Vi bruger VS Code som er en IDE fra Microsoft.

&#x24D8; **CLI** betyder *command line interface*, altså kommandolinjegrænseflade.


### VS Code
Som en snedker har sit træværktøj, har du din kodeeditor. Brug tid på at lære den at kende!  Se fx [denne video](
https://code.visualstudio.com/docs/introvideos/productivity) med tips og tricks.
Eller [denne her](
https://code.visualstudio.com/docs/introvideos/configure) om temaer.

⚠️ Du bør som minimum kende genvejen <kbd>Space</kbd> + <kbd>Ctrl</kbd> + <kbd>P</kbd> (Mac: <kbd>Shift</kbd> + <kbd>&#x2318;</kbd> + <kbd>P</kbd>) - den giver direkte adgang til ALT hvad man kan i VS Code. Prøv den nu.

### Python CLI
Man kan arbejde med python på kommandolinjen på flere måder.

#### Interactive mode

Hvis man skriver kommandoen `python3` i sit CLI, starter man python i _interactive mode_.
```
$>python3
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Derefter kan man "tale interaktivt med" python. _Interactive mode_ kan ses på at prompten er tre vinkler: `>>>`.

For at afslutte "samtalen" skriv `quit()`.

#### Afvikling af python-kode i py.filer
Hvis man vil have python til at afvikle et program som man har gemt i en fil, skriver man
```
python3 min-app.py
```
Her afvikler python programmet i filen `min-app.py` og stopper derefter.

En typisk fejl er at glemme om man befinder sig i _interactive mode_ eller udenfor.

## Syntaks
Python har en lidt speciel syntaks, sammenlignet med mange andre programmeringssprog. Det tilhører nemlig familien af sprog som anvender [_significant whitespace_](https://en.wikipedia.org/wiki/Off-side_rule).

Dette er i modsætning til mange andre programmeringssprog som anvender bestemte tegn, fx krølleparenteser  `{}` (som også kaldes _Tuborg-klammer_}, til at adskille blokke.

### Indrykning
Python bruger udelukkende **indrykning** (_indentation_) til at afgrænse blokke af kode fra hinanden.

For at definere en blok kode sætter man et kolon og rykker næste linje ind med **4 mellemrum**.
Alle linjer, der følger herefter og har samme indrykning, tilhører samme blok.

``` python
1: x, y, swap = 10, 5, True
2: if swap:  # samme blok 2-5
3:     i = x
4:     x = y
5:     y = i
6: i = 0 # anden blok
```
Hvorfor er det vigtigt om to linjer kode tilhører samme blok? Jo, fordi kode der tilhører samme blok, _altid eksekveres sammen_. Det er umuligt at læse og forstå kode, hvis man ikke forstår hvilke linjer der hører sammen i hvilke blokke.

Bemærk i øvrigt det afsluttende **kolon** `:` på første linje i blokken. Det har ingen anden funktion (så vidt vides) end at gøre det nemmere at læse - det betyder altså "her begynder en blok". Næste linje **skal** altså være indrykket, hvis linjen slutter med kolon.

Det samme gælder funktioner som også er en slag blokke. Sammenlign fx definitionen af en funktion i javascript

``` javascript
function greet(name) {
    console.log("Hello, " + name + "!");
}
i = 10; // Tilhører ikke funktionen
```
med python
``` python
def greet(name): # kolon = her begynder blok
    print("Hello, " + name + "!") # 4 mellemrum, tilhører funktionen
i = 10 # Tilhører ikke funktionen
```
VS Code sørger som regel for at indrykningen sker automatisk når man arbejder med `.py`-filer.

Standarden med netop 4 mellemrum som indrykning er _best practice_. I virkeligheden er python ligeglad - sålænge linjerne har samme indrykning, hører de sammen.

### Linjeskift
Tilsvarende er linjeskift også vigtige (syntaktisk signifikante) - hvilket også er forskelligt fra fx javascript og C#.
**I Python kan man afslutte et statement med et linjeskift** - uden semikolon.

Linjeskift indikerer ny statement.
``` python
first_name = "Peter"
last_name = "Nielsen"
full_name = first_name + " " + last_name
```

Det samme kunne skrives med semikolon ...
``` python
first_name = "Peter"; last_name = "Nielsen"; full_name = first_name + " " + last_name
```
... men lad være med! Det er ikke _pythonic_ - det er altså imod ånden i python.

### Opsummering
Vi har i det foregående brugt begreberne linjer og blokke uden rigtigt at definere dem helt præcist. Hvis du ikke er helt sikker på, at du forstår disse begreber endnu, gør det ikke noget.
Det vigtigste er, at du grundlæggende ved hvordan man skal forstå pythons særlige syntaks - altså ved hvordan man læser koden.


## Variabler
Hvad er en variabel? Vi kender dem måske fra matematik, når vi beregner resultat af en funktion.
```
y = f(x)
```
Her beregner vi funktionen af `x` og gemmer værdien som `y`.

i python skriver vi fx
``` python
school = "Slotshaven"
classname = "2r"
student_count = 11
htx = True
hhx = False
```

En variabel er en "beholder" med tre egenskaber:
- et navn
- en værdi
- en datatype (for værdien)

Fakta om variable:

Navnet kan ikke ændre sig. En variabel hedder altid det samme.
Hvis den hedder noget andet, er det en anden variabel.

Værdien derimod - den kan ændre sig.

En værdi har en type - altså tal, tekst, sand/falsk - hvad som helst.

Tænk på en spand eller kasse med et påtrykt navn og en bestemt form.
Det påtrykte navn er variablens navn.
Inde i kassen ligger værdien. Den kan skiftes ud.
Formen på kassen afgør datatypen. Man kan kunne ligge en værdi i kassen som har samme "form" som kassen.


``` python
student_count = 11
print(student_count) // 11
student_count = 10 // Nogen er kommet for sent
print(student_count) // 10
```

Variabler har _datatyper_. Typer kan være simple eller komplekse.
Vi begynder med de simple typer:

- streng (tekst)
- integer (heltal)
- boolean (sandt eller falsk)

De komplekse typer er fx lister af forskellig art, men det kommer vi til.

``` python
age = 11 # heltal (integer)
name = "Peter" # tekst (string)
is_htx = True # sandt/falsk (boolean)
has_car = False # do.
```
Som programmør er det dog meget vigtigt at vide hvilken type en variabel har, da det har betydning for hvilke operationer som man kan udføre med variablen.

Man kan komme galt afsted hvis man ikke har styr på det.

``` python

# name er et heltal - hvilket er underligt men ok ...
name = 15
# men dette er ikke okay ...
name = name.capitalize() # ERROR!
# AttributeError: 'int' object has no attribute 'capitalize'
```
Man kan ikke gøre et heltal til et stort bogstav.

Men man må gerne skifte type på en variabel - Python er ligeglad - men lad være med det.

``` python
name = 15
name = 'anna' # nu er name faktisk et navn
name = name.capitalize() # Anna
```

&#x24D8; Datatyper er et MEGET vigtigt begreb i programmering, men det er også et meget stort emne så det vender vi tilbage til.
