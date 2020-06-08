# Ausbildungsinhalte von Mitutoyo CTL Germany GmbH

# Zum Instagram Post vom 8.6.2020

> ![74LS32](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls32/74ls32.jpg)
> 
> Wird die LED in dieser Schaltung leuchten?
> 
> Mehr über Digitaltechnik lernst Du im Studium der Informationstechnik bei uns.



> ![74LS32](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls32/74ls32-detail.jpg)

Wie im vorherigen Post ist die Schaltung auf dem Steckbrett aufgebaut. Der Chip ist als 74LS32 beschriftet, oder im Detail-Bild als SN74LS32N zu identifizieren. Es handelt sich also wieder um einen Digitalbaustein der 74er-Reihe.

Der Vorsatz SN war eine Abkürzung für "Semiconductor Network" und bedeutete, dass hier mehrere Transistoren zusammengeschaltet waren. Außer Texas Instruments nutzte diese Bezeichnung aber niemand und so wird SN seither mit Texas Instruments in Verbindung gebracht. Neben SN nutzt Texas Instruments auch den Vorsatz TI. 

Das TI Logo ist bei diesem Exemplar nicht besonders gut erkennbar. Wenn Du jedoch öfter mit ICs bastelst, wirst Du mit der Zeit auch Logos in schlechterer Qualität erkennen.

![Logo von Texas Instruments](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls32/ti-logo.png)

Andere Kürzel sind:
* AD: Analog Devices
* AM: Advanced Micro Devices (eher bekannt unter der Abkürzung AMD)
* HD: Hitachi
* LM: National Semiconductor
* Z: Zilog

Der Suffix hängt vom Hersteller ab. Bei Texas Instruments handelt es sich um die Bauform ("package"). N bezeichnet einen Dual In-Line (DIL) Chip aus Plastik. J hätte ein ähnliches Aussehen, wäre aber aus Keramik gefertigt.

Häufiger als DIL wirst Du vermutlich den Begriff DIP für "DIL package" finden. "Dual" steht für die zwei und "Line" für Reihe, d.h. der Chip hat zwei Reihen mit Pins. Es gibt auch SIP (Single In-Line Package) mit nur einer Reihe von Beinchen.

Diese Bauformen sind für die Durchsteckmontage hergestellt. Der englische Begriff THT (through hole technology) macht es deutlich: diese Chips werden in der Anwendung durch Löcher (Bohrungen) gesteckt und dann verlötet.

Mit Hilfe des [TI Datenblatts für den 74LS32](http://www.ti.com/lit/ds/symlink/sn74ls32.pdf?HQS=TI-null-null-mousermode-df-pf-null-wwe&ts=1591626690153) ermittelst Du wieder die Funktion des Chips, kannst die Belegung der Pins herausfinden und anhand der Drähte die Schaltung analysieren.

Es handelt sich um ein Quadruple 2-Input Positive-Or Gate. "Or Gate" beschreibt die Funktion: es handelt sich um die Oder-Verknüpfung. "Positive" sagt, dass der Chip seine Funktion bei einer "hohen" Spannung ausführt, also bei einer digitalen Eins. "2-Input" sagt, dass die Oder-Funktion zwei Eingänge besitzt. Und "Quadruple" sagt, dass die Funktion viermal verfügbar ist. 

In einer Funktionstabelle für zwei digitale Eingänge würdest Du vielleicht 2²=4 Zeilen erwarten. TI kürzt da jedoch mit einem X für beliebige Werte:

![74LS32](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls32/74ls32-function-table.png)

Das Logik-Diagramm:

![74LS32](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls32/74ls32-logic-diagram.png)

Die Pin-Belegung:

![74LS32](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls32/74ls32-pins.png)

Damit ergibt sich folgende Schaltung:

![74LS32](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls32/74ls32-schematics.png)

Die Aussage HIGH OR LOW ergibt HIGH, womit die LED leuchten sollte, falls alle anderen Voraussetzungen gegeben sind.

## Zum Instagram Post vom 15.5.2020

> ![74LS04](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls04/74LS04.jpg)
>
> Was passiert, wenn die Spannungsversorgung hergestellt wird?
>
> Skill required: Datenblatt lesen

Es handelt sich bei der Abbildung um den Aufbau einer Digitalschaltung auf einem Steckbrett, auch als Breadboard bekannt.

Der verwendete Chip ist als 74LS04 gekennzeichnet. Um herauszufinden, welche Funktionalität dieser Chip bietet, ist entweder ein gutes Erinnerungsvermögen und Erfahrung nötig, oder man zieht ein Datenblatt zu Rate.

Datenblätter gibt es hoffentlich vom Lieferant (wir bestellen z.B. Reichelt oder Conrad), von anderen Lieferanten (z.B. Mouser) oder idealerweise direkt vom Hersteller (z.B. von Texas Instruments). Im Studium ist die Primärquelle vorzuziehen.

In diesem Fall stehen zum Beispiel folgende Quellen zur Verfügung:

* [74LS04 Datenblatt bei Reichelt](https://cdn-reichelt.de/documents/datenblatt/A200/IX645506.pdf)
* Mouser verlinkt direkt auf Texas Instruments
* [74LS04 Datenblatt bei Texas Instruments](http://www.ti.com/lit/ds/symlink/sn74ls04.pdf?HQS=TI-null-null-mousermode-df-pf-null-wwe&ts=1589539758225)

Der Titel des Datenblatts sagt "Hex Inverters". "Inverter" meint die NOT Funktion, "Hex" ist die Anzahl, also 6 Stück davon in diesem Chip.

Wer das nicht schon wusste, findet spätestens auf Seite 2 die zugehörige Logiktabelle:

![Logiktabelle 74LS04](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls04/74LS04-function-table.png)

Die Datenblätter gelten oft nicht nur für einen einzelnen Chip, sondern für alle Ausführungen davon, beispielsweise unterschiedliche Gehäuseformen (THT und SMD). Im vorliegenden Fall gibt es drei Ausführungen:

![74LS04 Housings](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls04/74LS04-housings.png)

Die letzte Bauform passt allein aufgrund der Form nicht zum Bild. Die mittlere Variante gilt nur für die 54er-Version, nicht aber für die 74er-Version. In diesem Fall ist also schon recht schnell geklärt, welche Pinbelegung der Chip haben muss.

Du kannst nun gedanklich den Chip aus dem Datenblatt auf die Schaltung legen. Achte dabei auf die Einkerbung (das Halbrund), also etwa so:

![Überlagerung mit Datenblatt](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls04/74LS04-explained.jpg)

Nun kannst Du schon sehen, wie die Verbindungen hergestellt sind:

* der rote Draht führt von der Plus-Schiene zu Pin 14 (VCC)
* ein schwarzer Draht führt von der Minus-Schiene zu Pin 7 (GND)
* ein grüner Draht führt von Plus zu Pin 13 (6A)
* ein blauer Draht von Pin 12 (6Y) zu Pin 9 (4A)
* ein Widerstand von Pin 8 (4Y) zu Zeile 19 des Breadboards
* eine LED von Zeile 19 des Breadboards zu Zeile 20 des Breadboards
* ein schwarzer Draht von Zeile 20 des Breadboards zu Minus

Das Logikdiagramm auf Seite 3 sagt Dir, wie die NOT-Gatter verschaltet sind, d.h. welche Pins Eingänge und Ausgänge sind:

![LogikDiagramm](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls04/74LS04-logicdiagram.png)

Im vorliegenden Fall kommt also ein HIGH Signal (Plus, grüner Draht) zum Eingang 6A. 
Dieses bewirkt ein LOW Signal am Ausgang 6Y. Von dort wird es weitergeführt (blauer Draht) zum Eingang 4A.
Das LOW Signal von 4A bewirkt ein HIGH Signal am Ausgang 4Y. Von dort wird es über den Widerstand zur LED geleitet.
Sofern die LED richtig herum eingebaut ist (auf dem Bild schlecht erkennbar), und der Ausgang leistungsstark genug ist, um genügend Strom für die LED bereitzustellen, wird die LED leuchten.

![Ergebnis](https://raw.githubusercontent.com/mitutoyo-ctl/mitutoyo-ctl.github.io/master/electronics/74ls04/74LS04-solution.jpg)