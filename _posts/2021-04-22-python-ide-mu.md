---
layout: default
title:  Python-IDE Mu
image: /static/python-ide-mu/python-ide-mu.png
category: tools
tags: ide, micropython, pico
---

Die Auswahl an Python-IDEs und -Editoren ist beeindruckend: IDLE, Thonny, PyCharm, uPyCraft oder PyDev, um nur ein paar Vertreter zu nennen.

Einige der Anwendungen wie uPyCraft richten sich dabei speziell an MicroPython-Programmierer. Andere wie IDLE oder Thonny sollen Anfänger bei den ersten Schritten mit Python generell unterstützen.

Der **Python-Editor Mu** kann Beides. Er richtet sich an Einsteiger, verbindet sich dabei aber problemlos mit einem MicroPython-kompatiblen Board wie einem ESP8266/ESP32, einen Lego-Spike, einem BBC micro:bit oder einem Raspberry Pi Pico.  Auch CircuitPython findet sich  in der Modus-Auswahl.

<img src="/static/python-ide-mu/mu-modus.png" alt="Auswahl des Modus in der Python-IDE Mu" class="img-fluid">

Wenn der Editor mit einem der Boards verbunden ist, lässt sich im oberen Bereich der Code schreiben. Die Syntax im Programm wird farblich hervorgehoben und Einrückungen automatisch vorgenommen. Mit dem Button _Prüfen_ lässt sich der Code auf syntaktische Korrektheit testen, mit _Tidy_ aufräumen und schließlich mit _Ausführen_ auf dem Board starten.

Nach dem Start des Python-Scripts wird im unteren Textfeld die Kommunikation mit REPL angezeigt. Dieses Fenster lässt sich über den Button _REPL_ auf Wunsch ein- oder ausblenden.

<img src="/static/python-ide-mu/mu-repl.png" alt="REPL-Feld in Mu" class="img-fluid">

Im Python 3-Modus lassen sich neben den Zeilennummern Breakpoints setzen und mit den üblichen Kommandos durch den Code steppen. Die Inhalte von Variablen werden dabei im _Debugging Inspector_ auf der rechten Seite des Fensters angezeigt.

Weitere Funktionen betreffen das Erstellen, Laden und Speichern von Dateien und das Aussehen des Editors.

[Mu](https://codewith.mu) ist für Windows, macOS oder als Python-Paket für Linux erhältlich und eignet sich dank der zahlreichen Verbindungsmöglichkeiten hervorragend für die ersten Schritte mit Micro/CircuitPython.
