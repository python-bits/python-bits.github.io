---
layout: default
title:  Python-Installation und erste Schritte
image:
date:   2021-05-16
category: grundlagen
---

## Python 2 oder 3?
todo

## Installation von
Python ist eine interpretierte Sprache, das heißt der Programmcode muss zur Laufzeit in Anweisungen für den Computer übersetzt werden. Der Code wird dadurch etwas langsamer als Maschinencode ausgeführt, läuft aber dafür auf allen Systemen für die der Interpreter verfügbar ist. Der Interpreter ist entweder schon auf Ihrem Rechner installiert, oder kann von https://www.python.org/downloads/ bezogen werden. Auf die Installation wird hier nicht näher eingegangen, ein lauffähiges System wird im Folgenden vorausgesetzt. Dieses erkennt man an einer Ausgabe ähnlich der Folgenden wenn man `python` oder `python3` in einem Terminal-Fenster/Eingabeaufforderung eingibt.

![Python 3](images/python.png)

Wie der Ausgabe entnommen werden kann ist hier im Beispiel Python 3.7.0, also ein Python 3-Release installiert. Dies ist die aktuellste Version, aber die 2.7er Version erfreut sich immer noch großer Beliebtheit (weil es Aufwand darstellt, den bestehenden Code auf die Version 3 umzustellen).

## Interaktiver Modus
Der Interpreter befindet sich nach dem Start interaktiven Modus, und erwartet eine Eingabe. Man erkennt das an den drei Größerzeichen (>>>). Um ihn etwas zu beschäftigen, bietet sich eine erste Eingabe an:

    >>> 3 + 5
    8

Der interaktive Modus kann übrigens mit der Tastenkombination ctrl-D wieder verlassen werden.

## File
Der interaktive Modus ist praktisch um kleinere Aufgaben zu erledigen oder Dinge auszuprobieren. Für komplexere Programme ist das Eingeben und direkt Ausführen von Anweisungen eher unpraktisch. Stattdessen wird der gesamte Programmcode in einer oder mehreren Textdateien gesammelt und dann dem Interpreter zur Ausführung übergeben.

Um das auszuprobieren öffnen Sie mit dem Texteditor Ihrer Wahl eine leere Textdatei. In die Textdatei werden beispielsweise folgende Zeilen geschrieben:

UTF-8-Hinweis!

    x = 3
    print(x)

Die Datei wird anschließend mit der Endung *.py*, also zum Beispiel *Test.py* gespeichert und dann in Terminal/Eingabeaufforderung mit `python Test.py` dem Interpreter zu Ausführung übergeben. Erwartungsgemäß lautet die Ausgabe *3*.
