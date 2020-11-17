# Kram für die Informatikarbeit
Da vermutlich nicht alle ultra Plan haben, was wir in Informatik gemacht haben, hier eine hoffentlich hilfreiche Zusammenfassung.

**Vorab:** 
Im Deutschen werden benutzen Dezimalbrüche (Kommazahlen) ein Komma zur Trennung, international üblich ist allerdings ein Punkt. Deswegen ist die deutsche 4,7 (Vierkommasieben) in Java 4.7.

Wenn im Code ``//`` vorkommt, ist das ein Kommentar. Dort kann man hinterschreiben, was auch immer man möchte, Java ignoriert diese Zeile einfach.

**Begriffserklärung:**
Normale Klammern: ()
Eckige Klammern: []
Geschweifte Klammern: {}
Terminal: Das Fenster, in das Java ausgibt, was ihr mit ``System.out.println();`` ausgeben lasst
# Inhalt
1. [Datentypen](#datentypen)
2. [Operatoren](#operatoren)
3. [Variablen](#variablen)
4. [If-Abfrage](#if)
5. [If-Else](#ifelse)
6. [While-Schlefe](#while)
7. [Arrays](#arrays)
8. [Einzelne Bauteile aus dem Unterricht](#more)
9. [Nassi-Shneiderman-Diagramme](#diagram)
10. [Code auskommentieren (erklären)](#kommentieren) 
11. [For - De­tail­liert](#fordetail) 
12. [Nachwort](#nachwort) 
## Datentypen <a name="datentypen"></a>
Variablen kommen in verschiedenen Formen, genannt Datentypen, vor. Das sind z.B.:

**Strings:**
Generelle Zeichenfolgen aus Buchstaben, Zahlen, Sonderzeichen usw. Strings sind immer von Anführungszeichen umschlossen.
Bsp: "String"

**Char:**
Ein einzelner Buchstabe.
Bsp: "c"

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

## Operatoren<a name="operatoren"></a>
Die Rechenoperatoren in Java sind identisch zu den Allgemeinen
|Operator|Aktion|
|--------|--------|
|+|addieren|
|-|subtrahieren|
|*|multiplizieren|
|/|dividieren|

Möchte man zwei Variablen zusammenrechnen, kann man das also ganz einfach tun.
```java
int x = 2;
int y = 3;
System.out.println(x + y);
```
gibt 5 aus.

Wenn mann zwei Strings addiert, werden sie einfach aneinander gehangen.
```java
String a = "Haus";
String b = "boot";

System.out.println(a + b);
```
gibt ``Hausboot`` aus

Möchte man zu einer Variable dauerhaft etwas hinzufügen, sind diese beiden Wege möglich.

Weg 1:
```java
int x = 3;

x = x + 1;
```

Weg 2
```java
int x = 3;

x += 1;
```
Weg 2 ist einfach nur kürzer, sonst gibt es keine Unterschiede. Neben ``+=`` gibt es natürlich auch noch ``-=``, ``*=`` und ``/=``.

Möchte man einen Integer um genau 1 erhöhen, kann man auch 
```java
int x = 3;
x++;
```
benutzen. Gleiches geht natürlich auch bei der Subtraktion:
```java
x--
```
zieht genau 1 ab.

## Variablen initialisieren<a name="variablen"></a>
Variablen haben einen Datentyp, einen Namen und einen Wert. Wenn man Variablen initialisiert (erstellt), gibt man zuerst den Datentyp, dann den Namen und dann den Wert an. Am Ende der Zeile muss ein ``;`` stehen.

**Bsp mit String:**
```java
String buchname = "Die drei Sonnen";
```
**Bsp mit Char:**
```java
char buchstabe = "g";
```
**Bsp mit Int:**
```java
int alter = 32;
```
**Bsp mit Double:**
```java
double laenge = 5.87;
```
**Bsp mit Array:**
```java
int[] temperaturen = {21, 24, 31};
String[] schulfaecher = {"Deutsch", "Englisch", "Chemie"};
```
**Bsp mit Float:**
```java
float hoehe = 3.6;
```

Man muss Variablen allerdings keinen Wert zuweisen. Man kann sie auch einfach erstellen.
```java
int x;
```
``x`` existiert nun, hat aber keinen Wert.

Möchte man Variablen später verändern kann man das einfach mit ``name = wert``
Bsp:
```java
//Variable wird erstellt
int x = 3;

//Variable wird später verändert
x = 4;
```
Man muss jedoch beachten, dass man der Variable nur Werte, die der Datentyp erlaubt, zuordnen kann.
```java
int x = 3;
x = "test";
```
gibt also einen Fehler.

## If-Abfrage<a name="if"></a>
In Java kann man mit der If-Abfrage abfragen, ob ein Statement ``true``, also wahr ist. Dazu benutzt man häufig den Vergleichsoperator ``==``. Sollte das Statement ``true`` sein, wird der Code innerhalb der geschweiften Klammern ausgeführt, sonst nicht.
```java
int x = 1;
int y = 1;
if (x == y) {
    System.out.println("wahr");
}
```
gibt ``wahr`` ausl

```java
int x = 1;
int y = 2;
if (x == y) {
    System.out.println("wahr");
}
```
gibt gar nichts aus.

## If-else-Abfrage<a name="ifelse"></a>
If-else macht genau das selbe wie die If-Abfrage, allerdings hängt man ein ``else`` dahinter. Sollte der Code der If-Abfrage nicht ausgeführt werden, wird stattdessen der Code in den geschweiften Klammern hinter ``else`` ausgeführt.
```java
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
```java
int x = 1;
int y = 2;
if (x != y) {
    System.out.println("wahr");
} else {
    System.out.println("falsch");
}
```
gibt ``wahr`` aus.

Hinter ``else`` kann man eine weitere If-Abfrage machen, um so mehr als eine Möglichkeit zu berücksichtigen.
```java
int x = 1;
int y = 2;
if (x == y) {
    System.out.println("gleich");
} else if (x != y) {
    System.out.println("ungleich");
} else {
    System.out.println("etwas anderes");
}
```
gibt ``ungleich`` aus

## For-Schleife<a name="for"></a>
Die For-Schleife führt den Code innerhalb der geschweiften Klammern mehrfach aus. Dazu erstellt sie einen Integer (oft ``i`` genannt), erhöht diesen Integer bei jedem Ausführen des Codes und hört erst auf, wenn der Integer einen bestimmten Wert erreicht hat.

```java
for (int i = 0; i < 3; i++) {
   System.out.println("Code wurde ausgefuehrt");
}
```
gibt aus:
```java
Code wurde ausgefuehrt
Code wurde ausgefuehrt
Code wurde ausgefuehrt
```
``int i = 0;`` erstellt die Variable ``i``
``i < 3;`` ist die Bedingung, dass der Code nochmal ausgeführt wird. Sollte ``i`` 3 oder größer sein, wird er nicht wiederholt.
``i++`` erhöht ``i`` am Ende um 1

Man kann auch die Variable ``i`` innerhalb der Schleife verwenden
```java
for (int i = 0; i < 3; i++) {
   System.out.println(i);
}
```
gibt aus:
```java
0
1
2
```
Warum 0, 1, 2 und nicht 1, 2, 3? Am Anfang ist ``i = 0``. Es wird abgefragt, ob ``i`` kleiner als 3 ist. Ist ``i`` das, wird der Code erst ausgeführt, dann wird ``i`` erst um 1 erhöht.

Wenn jetzt noch Fragen offen sind, ist am Ende nochmal eine For-Schleife Iteration (Durchlauf) für Iteration erklärt.

## While-Schleife<a name="while"></a>
Die While-Schleife wiederholt ebenfalls den Code innerhalb der geschweiften Klammern, allerdings wird, im Gegensatz zur For-Schleife, kein Integer erstellt, der mitzählt, sondern der Code wird einfach solange wiederholt, wie das Statement am in den normalen Klammern ``true`` ergibt, also wahr ist.
```java
int x = 1;
int y = 2;
while (x == y) {
    System.out.println("Code wird ausgefuehrt");
}
```
gibt aus:
```java
Code wird ausgefuehrt
Code wird ausgefuehrt
Code wird ausgefuehrt
Code wird ausgefuehrt
...
```
(...  heißt, es geht immer so weiter)

## Arrays<a name="arrays"></a>
Ein Array speichert mehrere Variablen gleichzeitig, allerdings nur von einem Datentyp. Es gibt also String-Arrays, die nur Strings speichern, Int-Arrays, die nur Ints speichern, usw. Die Daten werden in geschweiften Klammern angegeben und mit einem Komma getrennt.
```java
int[] temperaturen = {21, 24, 31};
String[] schulfaecher = {"Deutsch", "Englisch", "Chemie"};
```
Möchte man auf einen bestimmten Wert zugreifen, schreibt man den Namen des Arrays, dahinter eckige Klammern und darein, an welcher Stelle im Array der Wert ist.
```java
String[] schulfaecher = {"Deutsch", "Englisch", "Chemie"};

//ich möchte wissen, was an zweiter Stelle im Array steht
System.out.println(schulfaecher[1]);
```
gibt ``Englisch`` aus. Warum ``schulfaecher[1]``, wenn ich doch die zweite Stelle im Array möchte? Weil man bei Arrays bei 0 anfängt zu zählen. Der erste Wert ist also an Stelle 0, der zweite an Stelle 1, usw.

Werte innerhalb des Arrays ändern geht genau wie bei anderen Variablen, nur das man die Stelle, an welcher man den Wert ändern möchte, angeben muss:
```java
String[] schulfaecher = {"Deutsch", "Englisch", "Chemie"};

schulfaecher[1] = "Geschichte";
System.out.println(schulfaecher[1]);
```
gibt ``Geschichte`` aus.

## Einzelne Bauteile aus dem Unterricht<a name="more"></a>
**Scanner:**
Der Scanner kann Eingaben aus dem Terminal lesen und einer Variable zuordnen. Er am Anfang des Codes muss mit 
```java
import java.util.Scanner;
```
importiert werden. Dann kann ein neuer Scanner erstellt werden. Diesem gibt man einen Namen, den man später braucht, um ihn zu benutzen, hier ``neuerScanner``:
```java
Scanner neuerScanner = new Scanner(System.in);
```
Dann kann man Daten aus dem Terminal zu Variablen hinzufügen. Je nach Datentyp geht das anders:
```java
//String
String name = neuerScanner.nextLine();

//Integer
int nummer = neuerScanner.nextInt();

//double
double dezimalzahl = neuerScanner.nextDouble();

//float
float kommazahl = neuerScanner.nextFloat();
```

**Länge von Variablen:**
braucht man die Länge einer Variable, kann man ``<var>.length()`` benutzen:
```java
String stadt = "Berlin";
System.out.println(stadt.length());
```
gibt 6 (als Integer) aus.

## Nassi-Shneiderman-Diagramme<a name="diagram"></a>
Nassi-Shneiderman-Diagramm zeigen einen theoretischen Programmablauf.
![Nassi-Shneidermann-Diagramm](https://external-content.duckduckgo.com/iu/?u=http://de.academic.ru/pictures/dewiki/83/StruktErweitert.png&f=1&nofb=1)
Dieses Diagramm beschreibt einen Programmablauf, der den Nutzer nach seiner Zensur (1-6) fragt und diese in ``zahlZensur`` speichert. Danach setzt das Programm den String ``zeichenZensur`` jeweils zum Wortpendant und gibt ihn aus.

Der Ablauf ist folgender:
1. Variablen ``zahlZensur`` (Integer) und ``zeichenZensur`` (String) werden erstellt.
2. Programm gibt aus "Geben Sie die Zensur als Zahl ein."
3. Programm speichert die Benutzereingabe in ``zahlZensur``
4. Das Programm entscheidet, welchen Wert es ``zeichenZensur`` zuordnet. Dafür vergleicht das Programm den Integer ``zahlZensur`` zuerst mit 1. Ist ``zahlZensur == 1`` wahr, setzt das Programm ``zeichenZensur`` zu "sehr gut".
Sollte ``zahlZensur == 1`` aber nicht wahr sein, vergleicht es ``zahlZensur`` mit 2. Sollte ``zahlZensur == 2`` wahr sein, setzt es ``zeichenZensur``  zu "gut". 
Sollte auch das nicht wahr sein, versucht es 3, usw. 
Wenn selbst ``zahlZensur == 6 `` nicht wahr sein sollte, setzt es ``zeichenZensur`` zu "ungültig"
5. Am Ende gibt das Programm dann "Ihre eingegebene Zensur in Worten: " und ``zeichenZensur`` aus.

Gibt man also 2 ein, gibt das Programm ``Ihre eingegebene Zensur in Worten: gut`` aus.

Das ganze in Java-Code würde so aussehen:
```java
// 1. Schritt  
int zahlZensur;  
String zeichenZensur;  
Scanner eingabe = new Scanner(System.in);  
  
// 2. Schritt  
System.out.println("Geben Sie die Zensur als Zahl ein.");  
  
// 3. Schritt  
zahlZensur = eingabe.nextInt();  
  
// 4. Schritt  
if (zahlZensur == 1) {  
    zeichenZensur = "sehr gut";  
} else if (zahlZensur == 2) {  
    zeichenZensur = "gut";  
} else if (zahlZensur == 3) {  
    zeichenZensur = "befriedigend";  
} else if (zahlZensur == 4) {  
    zeichenZensur = "ausreichend";  
} else if (zahlZensur == 5) {  
    zeichenZensur = "mangelhaft";  
} else if (zahlZensur == 6) {  
    zeichenZensur = "ungenügend";  
}  
else {  
    zeichenZensur = "ungültig";  
}  
  
// 5. Schritt  
System.out.println("Ihre eingegebene Zensur in Worten: " + zeichenZensur);
```

## Code auskommentieren (erklären)<a name="kommentieren"></a>

In der Arbeit müssen wir vielleicht in einem fertigen Code erklären, was gewisse Teile machen. Das macht man mit Kommentaren im Code (oben erklärt). Als Beispiel der Code von Gerade:
```java
//Die Variablen sowie der Scanner werden erstellt
int zahlZensur;  
String zeichenZensur;  
Scanner eingabe = new Scanner(System.in);  
  
//Der Benutzer wird aufgefordert, eine Zahl einzugeben
System.out.println("Geben Sie die Zensur als Zahl ein.");  
  
//Das Programm weist zahlZensur den eingegebenen Wert zu
zahlZensur = eingabe.nextInt();  
  
//Das Programm weißt zeichenZensur einen Wert zu, 
//je nach dem, welchen Wert zahlZensur hat
if (zahlZensur == 1) {  
    zeichenZensur = "sehr gut";  
} else if (zahlZensur == 2) {  
    zeichenZensur = "gut";  
} else if (zahlZensur == 3) {  
    zeichenZensur = "befriedigend";  
} else if (zahlZensur == 4) {  
    zeichenZensur = "ausreichend";  
} else if (zahlZensur == 5) {  
    zeichenZensur = "mangelhaft";  
} else if (zahlZensur == 6) {  
    zeichenZensur = "ungenügend";  
}  
else {  
    zeichenZensur = "ungültig";  
}  
  
//Das Programm gibt den gerade bestimmten Wert aus
System.out.println("Ihre eingegebene Zensur in Worten: " + zeichenZensur);
```

## For - De­tail­liert<a name="fordetail"></a>
Unser Code ist folgender:
```java
for (int i = 0; i < 3; i++) {
   System.out.println(i);
}
```
Er gibt aus:
```java
0
1
2
```

**Warum macht er das?**
In
```java
for (int i = 0; i < 3; i++) {
```
wird zuerst ein Integer erstellt: ``i``. Dieser hat den Wert 0.
Als nächstes wird abgefragt, ob dieser Wert eine bestimmte Bedingung erfüllt, in diesem Fall, dass ``i`` kleiner als 3 ist.
Der Letzte Teil erhöht ``i`` um genau 1.

Wenn das Programm läuft und zu dieser Stelle im Code kommt, passiert also folgendes:
1. Die Variable wird erstellt.
2. Das Programm guckt, ob die Bedinung erfüllt ist.
3. Falls ja, wird der Code innerhalb der geschwungenen Klammern wird ausgeführt, sonst überspringt das Programm die for-Schleife
4. ``i`` wird um 1 erhöht
5. Das Programm guckt erneut, ob die Bedingung erfüllt ist.
6. Falls ja, wird der Code erneut ausgeführt, sonst überspringt das Programm die for-Schleife
7. ``i`` wird um 1 erhöht
8. usw.

```java
for (int i = 0; i < 3; i++) {
   System.out.println(i);
}
```
In diesem Praxisbeispiel würde das also heißen: 

1. ``i`` wird mit dem Wert 0 erstellt.
2. ``i`` ist unter 3
3. Der Code in den geschweiften Klammern wird ausgeführt, das Programm schreibt also ``i`` (momentan 0) in das Terminal
4. ``i`` wird um 1 erhöht, ist jetzt also 1
5.  ``i`` ist weiterhin unter 3
6. Der Code in den geschweiften Klammern wird erneut ausgeführt, das Programm schreibt also ``i`` (momentan 1) in das Terminal
7. ``i`` wird um 1 erhöht, ist jetzt 2
8. ``i`` ist weiterhin unter 3
9. Der Code in den geschweiften Klammern wird erneut ausgeführt, das Programm schreibt also ``i`` (momentan 2) in das Terminal
10. ``i`` wird um 1 erhöht, ist jetzt 3
11. ``i`` ist nicht mehr unter 3
12. Der Code in den geschweiften Klammern wird nicht nochmal ausgeführt, stattdessen führt das Programm das aus, was nach der for-Schleife steht

## Nachwort<a name="nachwort"></a>
Das war jetzt sehr viel auf einmal, sollte aber möglichst alles wichtige, was im Unterricht behandelt wurde, beinhalten. Bei Fragen stehe ich natürlich immer zur Verfügung, zur Not mit Videokonferenz, falls das jemand wirklich will. Das Thema ist unfangreich und am Anfang schwer zu begreifen. Wer mit dem Programmieren tatsächlich vertrauter werden möchte, könnte zum Beispiel folgendes tun:

* in Java-Kurse reinschauen und lernen.
* sich ein kleines Projekt ausdenken, und einfach versuchen, das zu programmieren. Je nach Projekt ist man dann sehr viel am Googlen, gerade am Anfang, und kommt schlecht voran. Das kann sehr frustrierend sein, gerade wenn man nicht besonders viel Spaß am Programmieren hat. Also vielleicht nicht die beste Idee.
* https://scratch.mit.edu/ ist eine Website, auf der man mit graphischen Blöcken Programme schreiben kann. Anstatt einem Meer von komischen Wörter in Eclipse hat man dort farbige Blöcke, die man zusammenschieben kann, hat also große Ähnlichkeit zur Programmierung von Lego Mindstorms. Um die Grundideen hinter bestimmten Dingen besser zu verstehen, kann Scratch hilfreich sein.
