# Kram für die Informatikarbeit
Da vermutlich nicht alle ultra Plan haben, was wir in Informatik gemacht haben, hier eine hoffentlich hilfreiche Zusammenfassung.

**Vorab:** 
Im Deutschen werden benutzen Dezimalbrüche (Kommazahlen) ein Komma zur Trennung, international üblich ist allerdings ein Punkt. Deswegen ist die deutsche 4,7 (Vierkommasieben) in Java 4.7

**Begriffserklärung:**
Geschweifte Klammern: {}
Terminal: Das Fenster, in das Java ausgibt, was ihr mit ``System.out.println();`` ausgeben lasst
## Datentypen
Variablen kommen in verschiedenen Formen, genannt Datentypen, vor. Das sind z.B.:

**Strings:**
Generelle Zeichenfolgen aus Buchstaben, Zahlen, Sonderzeichen usw. Strings sind immer von Anführungszeichen umschlossen.
Bsp: "String"

**Integer:**
Ganzzahlen, kurz Int
Bsp: 15

**Float:**
Kommazahl, benutzt man normalerweise nicht
Bsp: 4.7

**Double:**
Kommazahl, kann 2x mehr speichern als Float, wird normalerweise für Kommazahlen benutzt
Bsp: 4.7

**Array:**
Speichert mehrere Variablen gleichzeitig, allerdings nur von einem Datentyp. Es gibt also String-Arrays, die nur Strings speichern, Int-Arrays, die nur Ints speichern, usw. Die Daten werden in geschweiften Klammern angegeben und mit einem Komma getrennt.
Bsp: {1, 2}

## Variablen initialisieren
Variablen haben einen Datentyp, einen Namen und einen Wert. Wenn man Variablen initialisiert (erstellt), gibt man zuerst den Datentyp, dann den Namen und dann den Wert an. Am Ende der Zeile muss ein ``;`` stehen.

**Bsp mit String:**
``String buchname = "Die drei Sonnen";``
**Bsp mit Int:**
``int alter = 32;``
**Bsp mit Double:**
``Double laenge = 5.87;``
**Bsp mit Array:**
``int[] temperaturen = {21, 24, 31};``
``String[] schulfaecher = {"Deutsch", "Englisch", Chemie"};``
**Bsp mit Float:**
``Float hoehe = 3.6;``

## If-Abfrage
In Java kann man mit der If-Abfrage abfragen, ob ein Statement ``true``, also wahr ist. Dazu benutzt man häufig den Vergleichsoperator ``==``. Sollte das Statement ``true`` sein, wird der Code innerhalb der geschweiften Klammern ausgeführt, sonst nicht.
```
int x = 1;
int y = 1;
if (x == y) {
    System.out.println("wahr");
}
```
schreibt ``wahr`` in das Terminal

```
int x = 1;
int y = 2;
if (x == y) {
    System.out.println("wahr");
}
```
gibt gar nichts aus.

## If-else-Abfrage
If-else macht genau das selbe wie die If-Abfrage, allerdings hängt man ein ``else`` dahinter. Sollte der Code der If-Abfrage nicht ausgeführt werden, wird stattdessen der Code in den geschweiften Klammern hinter ``else`` ausgeführt.
```
int x = 1;
int y = 2;
if (x == y) {
    System.out.println("wahr");
} else {
    System.out.println("falsch");
}
```
gibt ``falsch`` aus.

``!=`` ist das Gegenteil von ``==``, es vergleicht, ob etwas ungleich ist.
```
int x = 1;
int y = 2;
if (x != y) {
    System.out.println("wahr");
} else {
    System.out.println("falsch");
}
```
gibt ``wahr`` aus.

## For-Schleife
Die For-Schleife führt den Code innerhalb der geschweiften Klammern mehrfach aus. Dazu erstellt sie einen Integer (oft ``i`` genannt), erhöht diesen Integer bei jedem Ausführen des Codes und hört erst auf, wenn der Integer einen bestimmten Wert erreicht hat.

```
for (int i = 0; i < 3; i++) {
   System.out.println("Code wurde ausgefuehrt");
}
```
gibt aus:
```
Code wurde ausgefuehrt
Code wurde ausgefuehrt
Code wurde ausgefuehrt
```
``int i = 0;`` erstellt die Variable ``i``
``i < 3;`` ist die Bedingung, dass der Code nochmal ausgeführt wird. Sollte ``i`` 3 oder größer sein, wird er nicht wiederholt.
``i++`` erhöht ``i`` am Ende um 1

Man kann auch die Variable ``i`` innerhalb der Schleife verwenden
```
for (int i = 0; i < 3; i++) {
   System.out.println(i);
}
```
gibt aus:
```
0
1
2
```
Warum 0, 1, 2 und nicht 1, 2, 3? Am Anfang ist ``i = 0``. Es wird abgefragt, ob ``i`` kleiner als 3 ist. Ist ``i`` das, wird der Code erst ausgeführt, dann wird ``i`` erst um 1 erhöht.

Wenn jetzt noch Fragen offen sind, ist am Ende nochmal eine For-Schleife Iteration (Durchlauf) für Iteration erklärt.

## While-Schleife
Die While-Schleife wiederholt ebenfalls den Code innerhalb der geschweiften Klammern, allerdings wird, im Gegensatz zur For-Schleife, kein Integer erstellt, der mitzählt, sondern der Code wird einfach solange wiederholt, wie das Statement am in den normalen Klammern ``true`` ergibt, also wahr ist.
```
int x = 1;
int y = 2;
while (x == y) {
    System.out.println("Code wird ausgefuehrt");
}
```
gibt aus:
```
Code wird ausgefuehrt
Code wird ausgefuehrt
Code wird ausgefuehrt
Code wird ausgefuehrt
...
```
(...  heißt, es geht immer so weiter)
