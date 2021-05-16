# Kontrollstrukturen\index{Kontrollstrukturen}

Mit dem bisherigen Wissen lassen sich nur sehr einfache Abfolgen von Anweisungen und Zuweisungen schreiben. Mit den in diesem Kapitel vorgestellten Kontrollstrukturen wird das deutlich spannender. Kontrollstrukturen ermöglichen aus mehreren verschiedenen Wegen im Programmfluss einen zu beschreiten (Verzweigungen) oder Teile des Codes zu wiederholen (Schleifen). 

## Verzweigungen\index{Verzweigungen}

### if / else / elif



Die if-Bedingung\index{if} ist vermutlich so alt wie der Computer selbst. Sie prüft eine hinter dem Schlüsselwort *if* angegebene Bedingung und führt bei Zutreffen der Bedingung den darunter eingerückten Code aus. Etwas salopp formuliert handelt es sich also um ein "Wenn dies, mach' das":

```python
if alter >= 18:
	print("volljährig")
	print("Wird auch nur ausgeführt wenn true")
print("Wird immer ausgeführt")
	
```
Bei der Bedingung muss es sich um einen Ausdruck handeln, der einen booleschen Wert ergeibt, also True oder False.

Bitte beachten Sie unbedingt die Code-Einrückung\index{Einrückung} in Form von vier Spaces unter dem if. Python kennt keine geschweiften Klammern zur Blockbildung von Anweisungen, wie sie in anderen Programmiersprachen üblich sind. Alle auf das if folgende eingerückten Anweisungen werden ausgeführt wenn die Bedingung erfüllt ist. Die letzte Anweisung im Beispiel oben hat folglich nicht mehr mir dem if zu tun und wird auf jeden Fall ausgeführt.

Oft hat man nun den Fall dass auch beim Nicht-zutreffen der Bedingung eine Anweisung ausgeführt werden soll. Dazu dient er else-Zweig der Bedingung. Er wird nur ausgeführt wenn die Bedingung nicht erfüllt ist (man könnte ihn auch als "ansonsten"-Fall bezeichnen):

```python
age = 17
if age >= 18:
	print("volljährig")
else:
	print("nicht volljährig")
```



if  elif   else
Keine Klammern, Doppelpunkt nach Bedingung

not, and, or

## Schleifen\index{Schleifen}

Schleifen dienen dazu Teile des Programms mehrfach hintereinander rauszuführen. Die Wiederholung findet statt bis eine Abbrichbedingung eingetreten ist. 

### while\index{while}

Die einfachste Schleife ist die while-Schleife. Der eingerückte Schleifenrumpf mit den Anweisungen wird wiederholt, solange die Bedingung hinter dem Schlüsselwort *while* und dem Doppelpunkt wahr ist:

```python
i = 0
while i<10:
    print(i)
    i=i+1
```

In einigen Programmiersprachen ist die Bedingung in runden Klammern zu setzen, Python ist hier tolerant.  

### for\index{for}
counted loop:

for x in range (1, 5):
 print x

Geht auch ohne startwert (ist dann 0):

for x in range (5):
 print x

Man kann auch rückwärts zählen (Startwert > Endwert). Schrittgröße erforderlich:
for x in range (10,1, -1):

for x in "WURSTFETT":
 print x


List loop:
numList = [1, 2, 3]
for x in numList:
 printx

Der normale Ablauf einer for-Schleife lässt sich auf zwei Arten unterbrechen. 

#### continue\index{continue}
 
Durch die Anweisung *continue* wird der Ablauf der aktuellen Iteration an der Stelle des continues abgebrochen und mit dem nächsten Durchlauf weitergemacht. Das Ausführen des folgenden Codestücks führt deshalb zur Ausgabe der Werte 1,2,4. Beim dritten Durchlauf wird vor dem Ausführen der print-Anweisung mit dem nächsten Durchlauf weitergemacht:

```python
for x in range (1,5):
    if x == 3: continue
    print(x)
```


#### break\index{break}
Die break-Anweisung funktioniert ähnlich wie continue, allerdings wird hier die Schleife gleich ganz abgebrochen:

```python
for x in range (1,5):
    if x == 3: break
    print(x)
```

Ausgegeben werden hier deshalb lediglich die Werte 1 und 2.