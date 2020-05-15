# Elektrotechnik

Zum Instagram Post vom 15.5.2020.

> ![74LS04](electronics/75ls04/74LS04.jpg)
>
> Was passiert, wenn die Spannungsversorgung hergestellt wird?
>
> Skill required: Datenblatt lesen

Es handelt sich bei der Abbildung um den Aufbau einer Digitalschaltung auf einem Steckbreatt, auch als Breadboard bekannt.

Der verwendete Chip ist als 74LS04 gekennzeichnet. Um herauszufinden, welche Funktionalität dieser Chip bietet, ist entweder ein gutes Erinnerungsvermögen und Erfahrung nötig, oder man zieht ein Datenblatt zu Rate.

Datenblätter gibt es hoffentlich vom Lieferant (wir bestellen z.B. Reichelt oder Conrad), von anderen Lieferanten (z.B. Mouseer) oder direkt vom Hersteller (z.B. von Texas Instruments).

In diesem Fall stehen zum Beispiel folgende Quellen zur Verfügung:

* [74LS04 Datenblatt bei Reichelt](https://cdn-reichelt.de/documents/datenblatt/A200/IX645506.pdf)
* Mouser verlinkt direkt auf Texas Instruments
* [74LS04 Datenblatt bei Texas Instruments](http://www.ti.com/lit/ds/symlink/sn74ls04.pdf?HQS=TI-null-null-mousermode-df-pf-null-wwe&ts=1589539758225)

Der Titel des Datenblatts sagt "Hex Inverters". "Inverter" meint die NOT Funktion, "Hex" ist die Anzahl, also 6 Stück davon in diesem Chip.

Wer das nicht schon wusste, findet spätestens auf Seite 2 die zugehörige Logiktabelle:

![Logiktabelle 74LS04](electronics/75ls04/74LS04-function-table.png)

Die Datenblätter gelten oft nicht nur für einen einzelnen Chip, sondern für alle Ausführungen davon, beispielsweise unterschiedliche Gehäuseformen (THT und SMD). Im vorliegenden Fall gibt es drei Ausführungen:

![74LS04 Housings](electronics/75ls04/74LS04-housings.png)

Die letzte Bauform passt allein aufgrund der Form nicht zum Bild. Die mittlere Variante gilt nur für die 54er-Version, nicht aber für die 74er-Version. In diesem Fall ist also schon recht schnell geklärt, welche Pinbelegung der Chip haben muss.

Du kannst nun gedanklich den Chip aus dem Datenblatt auf die Schaltung legen. Achte dabei auf die Einkerbung (das Halbrund), also etwa so:

![Überlagerung mit Datenblatt](electronics/75ls04/74LS04-explained.jpg)

Nun kannst Du schon sehen, wie die Verbindungen hergestellt sind:

* der rote Draht führt von der Plus-Schiene zu Pin 14 (VCC)
* ein schwarzer Draht führt von der Minus-Schiene zu Pin 7 (GND)
* ein grüner Draht führt von Plus zu Pin 13 (6A)
* ein blauer Draht von Pin 12 (6Y) zu Pin 9 (4A)
* ein Widerstand von Pin 8 (4Y) zu Zeile 19 des Breadboards
* eine LED von Zeile 19 des Breadboards zu Zeile 20 des Breadboards
* ein schwarzer Draht von Zeile 20 des Breadboards zu Minus

Das Logikdiagramm auf Seite 3 sagt Dir, wie die NOT-Gatter miteinander verschaltet sind:

![LogikDiagramm](electronics/75ls04/74LS04-logicdiagram.png)

Im vorliegenden Fall kommt also ein HIGH Signal (Plus, grüner Draht) zum Eingang 6A. 
Dieses bewirkt ein LOW Signal am Ausgang 6Y. Von dort wird es weitergeführt (blauer Draht) zum Eingang 4A.
Das LOW Signal von 4A bewirkt ein HIGH Signal am Ausgang 4Y. Von dort wird es über den Widerstand zur LED geleitet.
Sofern die LED richtig herum eingebaut ist (auf dem Bild schlecht erkennbar), und der Ausgang leistungsstark genug ist, um genügend Strom für die LED bereitszustellen, wird die LED leuchten.

![Ergebnis](electronics/75ls04/74LS04-solution.jpg)
