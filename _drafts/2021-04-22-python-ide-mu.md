---
layout: default
title:  Python-IDE Mu
image: /static/python-ide-mu/python-ide-mu.png
date:   2020-05-13
category: tools
---

Die Auswahl an Python-IDEs und -Editoren ist mittlerweile beeindruckend: IDLE, Thonny, PyCharm, uPyCraft oder PyDev, um nur ein paar Vertreter zu nennen.

Einige der Anwendungen wie uPyCraft richten sich dabei speziell an MicroPython-Programmierer. Andere wie IDLE oder Thonny sollen Anfänger bei den ersten Schritten mit Python generell unterstützen.

Die Python-IDE Mu kann beides: Der Editor richtet sich an Einsteiger, verbindet sich dabei aber problemlos mit einem MicroPython-kompatiblen Board wie einen ESP8266/ESP32, einen Lego-Spike, einem BBC micro:bit oder einem Raspberry Pi Pico.  Auch CircuitPython findet sich  in der Modus-Auswahl.

<img src="/static/python-ide-mu/mu-modus.png" alt="Auswahl des Modus in der Python-IDE Mu" class="img-fluid">

Wenn der Editor mit einem der Boards verbunden ist, lässt sich im oberen Bereich der Code schreiben. Die Syntax im Programmcode wird farblich hervorgehoben und Einrückungen werden automatisch vorgenommen. Mit dem Button Prüfen lässt sich der Code auf syntaktische Korrektheit testen, mit Tidy aufräumen und schließlich mit Asuführen auf dem verbundnen Board starten.

Und das war es auch schon fast der Unterstüzung für Prpgrammierer. Die restlichen Funktionen betreffen das Erstellen, Laden und Speichern von Dateien und das Aussehen des Editors.

Nach dem Start wird im unteren Textfeld wird die Kommunikation mit REPL angezeigt. Dieses Fenster lässt sich über den Button REPL auf auf Wunsch ein- oder ausblenden.

<img src="/static/python-ide-mu/mu-repl.png" alt="REPL-Feld in Mu" class="img-fluid">

Mu eignet sich dank der zahlreichen Verbindungsmöglichkeiten für die ersten Schritte mit Micro/CircuitPython auf einem angeschlossenen Board. Für die Entwicklung komplizierter Anwendungen wäre aber beispielsweise ein Debugger ein hilfreiches Feature.
