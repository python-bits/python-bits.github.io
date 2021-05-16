# Variablen, Datentypen und Zuweisungen

## Variablen
Vermutlich ist ihnen aus dem Schulunterricht das Konzept von Variablen bekannt. Es handelt sich dabei um Speicherstellen - bildlich ausgedrückt, so etwas wie Schubladen - die man mit Daten füllen kann, beispielsweise 

```python
x = 5
```

Der Variablen namens x wurde hier der Wert 5 zugewiesen. Den Namen der Variablen darf man sich selber aussuchen. Also ist auch beispielsweise `level = 3` vollkommen in Ordnung. Wer schauen will, was in der Variablen grade gespeichert wird, kann das mit der print-Anweisung ausgeben:

```python
print(x)
```

Erwartungsgemäß ist die Ausgabe 5. Ein erneutes Ausführen der print()-Anweisung gibt die Zahl wieder aus (die Schublade wird durch die Ausgabe also nicht etwa geleert). Soll die Variable einen anderen Wert bekommen, wird er einfach zugewiesen:

```python
x = 8
```

Da man hier von Zuweisen spricht, wird das Gleichheitszeichen in diesem Fall auch als *Zuweisungsoperator*\index{Zuweisungsoperator} bezeichnet. Das klingt ein wenig förmlich, sollte man aber mal gehört haben. Im weiteren Verlauf tauchen noch etliche Operatoren auf, zum Beispiel der Vergleichsoperator == (zwei Gleichzeichen), mit dem sich zwei Werte auf Gleichheit testen lassen.

## Datentypen

Anders als im Mathematikunterricht haben Variablen in der Programmierung einen Typ. Das heißt, die Schubladen sind für eine bestimmte Art von Daten gemacht. In vielen Programmiersprachen ist es notwendig den Typ beim Anlegen der Variable anzugeben. Python ist da unkompliziert, der Typ wird einfach zur Laufzeit aus dem zugewiesenen Wert ermittelt. Im Fachjargon nennt sich das dynamische Typisierung. Im Beispiel oben wurde 5 zugewiesen, Python beschließt also dass die Variable für Zahlen gedacht ist.
Mit Zahlen kann man natürlich rechnen:

```python
y = 12
ergebnis = x + y
print(ergebnis)
```

In dem Beispiel oben wird einer zweiten Variable namens *y* der Wert 12 zugewiesen. Anschließend werden x und y (also 8 und 12) addiert und der Variablen *ergebnis* zugewiesen. 

Die anderen Rechenoperationen werden nicht weiter überraschend mit -, *, und / durchgeführt. Wie in anderen Programmiersprachen auch gibt es eine Reihenfolge welche Operationen zuerst ausgeführt werden, wenn mehrere in einem Ausdruck beteiligt sind:

Klammer > Exponent > Multiplikation > Division > Addition > Subtraktion 


Das Prozentzeichen steht in Python für den Modulo-Operator, er gibt den Rest einer Division zurück. Schauen wir uns dazu ein Beipsiel an:

```python
rest = 7 % 3
print(rest)
```

Die drei passt zweimal in die sieben, es bleibt ein Rest eins.

Ganz interessant ist zu untersuchen was passiert, wenn man einer Variablen eine andere zuweist und dann den Wert ändert:

```python
z = x
print(z)
x = 9
print(z)
```

Das Ergebnis der zweiten print-Anweisung ist hier 8. Das Ändern des Wertes von x hat also nicht zu einer Änderung des Wertes von z geführt. Beim Zuweisen wird also der Wert von x in z gespeichert und nicht etwa ein Verweis auf x.

Zahlen in Programmiersprachen sind nicht gleich Zahlen, sie lassen sich weiter unterteilen. In Python sind das die Folgenden

- int (ganze Zahlen)
- float (Gleitkommazahl mit begrenzter Genauigkeit)
- complex (komplexe Zahlen mit Imaginärteil, hier uninteressant)

In Python 2 gab es noch den Typ long für große Ganzzahlen, in Python wurden int und long zusammengelegt und es gibt nur noch int.

Bei einer Zuweisung einer ganzen Zahl wie wir es oben gesehen haben wird deshalb standardmäßig eine Variable vom Typ int (für Integer – englisch für Gannzahl - angelegt).

Immer wenn die Zahl einen Dezimalpunkt enthält, kommt der Typ float zur Verwendung:

```python
pi = 3.1415
```

Es gibt noch eine Reihe von anderen Datentypen in Python, die wichtigsten sind strings, numbers, lists, tuples, dictionaries und files.

### Boolenas


### String

Strings\index{String} haben nichts mit dem gleichnamigen Kleidungsstück zu tun, es handelt sich hier um Textwerte (Zeichenketten) wie Buchstaben, Worte, Sätze, die in doppelten oder einfachen Anführungsstrichen angegeben werden. 

```python
strasse = "Nibelungenallee"
hausnummer = '3a'
```

Strings lassen sich mit dem Plus-Operator zusammenketten, man spricht hier auch von *konkatenieren*:

```python
strasse = strasse + " " + hausnummer
print(strasse)
```

Variablen verschiedenen Typs (beispielsweise Integer und String) lassen sich auf diese Weise nicht zusammenfügen, man erhält einen Typ-Error:

```python
strasse = "Nibelungenallee"
hausnummer = 3	
strasse = strasse + " " + hausnummer
```
Da es oft vorkommt, das Integer-Werte zusammen mit String ausgegeben werden sollen lassen sich diese mit der str()-Funktion in Strings umwandeln:

strasse = strasse + " " + str(hausnummer)

Funktionen werden im weiteren Verlauf noch genau beschrieben.

## Kommentare\index{Kommentare}
In komplexerem Quellcode finden sich oft Kommentare. Entwickler hinterlassen dort Informationen (für sich selber wenn sie irgendwann den Code zu einem späteren Zeitpunkt wieder einmal lesen oder für andere Entwickler) warum sie etwas getan haben. Damit der Python-Interpreter die Kommentare ignoriert und nicht etwa versucht sie auszuführen, beginnen die Kommentare mit einem Hash-Zeichen (#):

```python
# Level 10 ist noch nicht fertig!
maxLevel = 9
```
Das # muss leider vor jede auskommentierte Zeile. Es ist also nicht möglich wie in anderen Sprachen größere Abschnitte durcj eine beginnende und einen endende Kommentarmarkierung auszukommentieren. Entwicklungsumgebungen bieten aber unterstützung indem sie für einen markierten Block (also mehrere Zeilen) die # vor jede Zeile setzen. In IDLE findet man die Funktion unter *Format > Comment Out Region* bzw. *Format > Uncomment Region*.

Gute Kommentare beschreiben übrigens übrigens **warum** etwas getan wurde. **Das** etwas getan wurde und **wie** es getan wurde sieht man ja im Code.



--------------------


einfacher Backslash ist in Python reserviert -> Slash oder doppelten Backslash verwenden

String-Vergleich mit ==
mit "in" kann auf Teilinhalte überprüft werden: print str2 in str1
Man kann auf die Buchstaben eines String wie auf die Elemente eines Array zugreifen: myString[0]
Bei negativen Indizes wird von rechts gesucht: myString[-4]

Teile extrahieren: mYTSring[1:3] (obere Grenze wird nicht eingeschlossen)

Weglassen von Grenzen macht von Anfang bzw. bis zum Ende: myString[:5] -> 0-4

Trimmen:
strip (beide Seiten), rstrip, lstrip

myString.find("a") (gibt -1 zurcük kein Vorkommen )
replace
upper, lower
isalnum, isalpha, isdigit
split (Trennzeichen ist space wenn nicht angegeben)

Übersicht über die Standardfunktionen: __builtins__

len()


Als Exponential-Operator wird "**" verwendet

abs()
max()
round()

Umwandlung von Datentypen:
int(x)
long(x)
str(x)

