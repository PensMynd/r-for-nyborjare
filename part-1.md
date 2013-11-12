Grundkurs i R
========================================================
transition: linear
css: css/slides.css

Love Hansson och Thomas Reinholdsson, Pensionsmyndigheten

18 november, 2014


Lärandemål
========================================================
type: section

- Sammanställa deskriptiv statistik om data med enklare funktioner
- Använda ggplot och grafiska funktioner för deskription och exploration av data
- Använda och förstå ett flertal datastrukturer
- Installera och använda paket
- Hämta data från olika källor (Excel, MiDAS, Coldbir, Pedal)
- Lagra data i olika format
- Självständigt inhämta ny kunskap och hitta svar på frågor om R (vara en del av R:s community)


Datastrukturer
========================================================
type: section

Det finns flera olika datatyper som används inom R, de vanligaste listas nedan:

- Vektorer
  - Atomic vectors (`vector`)
  - Listor (`list`)
  - Faktorer (`factor`)
- Matriser (`matrix`, `array`)
- Datatabeller
  - Data frame (`data.frame`)
  - Data table (`data.table`)

Atomic vectors
========================================================

De vanligaste typerna av vektorer är:


```r
logical <- c(T, FALSE, TRUE, FALSE)
numeric <- c(1, 2.5, 4.5)
integer <- c(1L, 6L, 10L)
character <- c("these are", "some strings")
```


Vanliga vektorer är inte "nestade": 


```r
c(1, c(2, c(3, 4)))
```

```
[1] 1 2 3 4
```

```r
c(1, 2, 3, 4)
```

```
[1] 1 2 3 4
```



Läs mer om datastrukturer
========================================================

- [Advanced R programming - Data structures](http://adv-r.had.co.nz/Data-structures.html)


Subsetting
========================================================
type: section

När vi har data vill vi kunna arbeta med delar av data. Detta kallas __subsetting__.

Vår metod för att hämta ut delar av data beror på vilken __datatyp__ vi använder oss av.

R erbjuder __flera metoder__ för att hämta ut data för varje datatyp.

Enkla vektorer
========================================================

Data:

```r
x <- c(aa=2.1, bb=4.2, cc=3.3, dd=5.4)
```


Metoder för dataextrahering:

```r
x[c(1,2)] # Välj ett eller flera element
x[order(x)] # Välj alla element, sorterade
x[['aa']] # Välj ett, namngivet eller numrerat, element
```


Listor
========================================================

De metoder som fungerar för listor fungerar _oftast_ även för vektorer.

Data:

```r
ll <- list(2.1, 4.2, 3.3, 5.4)
```


Metoder för dataextrahering:

```r
ll[c(1,2)]
ll[[1]]
```


data.frame()
========================================================


Data:

```r
DF <- data.frame(id=c(1:3),
value=c("Love", "Thomas", "Ole"))
```



Urval kan göras kolumnvis, radvis, eller enligt vissa kriterier. Observera kommatecknet i []-anropet!

```r
DF[c(1,2),]
DF[,c("value")]
DF[DF$value=="Ole",]
```


data.table()
========================================================

data.table fungerar ungefär som data.frame, men skiljer sig i vissa detaljer.


```r
DT <- data.table(id=c(1:3),
value=c("Cédric", "Elin", "Ingemar"))
```






En grundläggande "vokabulär"
========================================================
type: section

20-30 funktioner (?) ur Hadleys "Vocabulary"-avsnitt


Funktioner
========================================================
type: section


Pakethantering
========================================================
type: section


Grafik och dataanalys
========================================================
type: section

- ggplot2


Externa datakällor
========================================================
type: section



Best practices för programdesign
========================================================
type: section


Att lära sig mer om R
========================================================
type: section

- R:s community
- Stack Overflow
- GitHub


Avslutning och utblick
========================================================
type: section


Kurslitteratur
========================================================
type: section




