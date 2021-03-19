---
layout: default
title: Python auf dem Raspberry Pi
image: /static/python-raspberry-pi/raspberry-pi-idle.png
category: hardware
tags:	raspberry-pi
vgwort:
---

**Python** ist die bevorzugte Programmiersprache für den **Raspberry Pi** und seit der Version 4 des Minirechners lässt sich auch ganz passabel darauf entwickeln. Der Beitrag stellt die verschiedenen Möglichkeiten vor.

Ausgegangen wird hier von der Desktop-Variante von Raspberry Pi OS (32 Bit), die mit dem Raspberry Pi Imager schnell geschrieben ist.

Standardmäßig sind in dem Betriebssystem sowohl Python 2 als auch Python 3 installiert. Mit dem Kommando python --version bzw. python3 --version kann man sich davon überzeugen:

<img src="/static/python-raspberry-pi/python-versionen.png" alt="Python 2 und 3 auf dem Raspberry Pi" class="img-fluid">

Durch Eingabe von python bzw. python3 landet man in der interaktiven Python-Shell. Hinter dem Python-Prompt (die drei >>> -Zeichen) lassen sich Python-Kommandos eingeben und ausführen. Grade bei längeren Programmen ist das aber eher unkomfortabel, weshalb man sie eher in einer Textdatei mit Endung .py speichert und die Datei dem Python-Aufruf als Argument mitgibt:

    python3 test.py

Prinzipiell lassen sich so Python-Programme entwickeln, aber auch das ist noch mühsam. Fehler im Code lassen sich nur schwer finden, weshalb man in der Praxis eher auf eine Entwicklungsumgebung (IDE) zurückgreift.

## IDLE
Die bekannteste IDE für Python ist vermutlich IDLE. Die Entwicklungsumgebung ist zunächst nicht installiert, lässt sich aber durch Eingabe des folgenden Kommandos in ein Terminalfenster leicht nachrüsten:

    sudo apt install idle3

IDLE findet sich danach im Applications-Menü (die Himbeere am oberen Bildschirmrand) unter *Entwicklung*.

<img src="/static/python-raspberry-pi/raspberry-pi-idle.png" alt="IDLE auf dem Raspberry Pi" class="img-fluid">

Im IDLE-Shell Window, das sich nach dem Start öffnet, kann man Python-Kommandos eingeben, die werden dann direkt ausgeführt. Für ganze Programme öffnet man mit _File > New File_ ein IDLE-Editorfenster. Ausgeführt werden die Scripte dann mit  _Run > Run Module_, wobei hier zunächst ein Speicherort anzugeben ist. IDLE beherrscht unter anderem Syntax-Higlighting (das Färben unterschiedlicher Code-Bestandteile in unterschiedlichen Farben), Code-Completion (das Vervollständigen von Funktionsnamen) und Debugging.

## Thonny
Bereits vorhanden, und ebenfalls unter *Entwicklung* zu finden ist [Thonny](https://thonny.org/). Die IDE richtet sich speziell an Anfänger und ist ähnlich IDLE aufgebaut. Anders als bei IDLE sind bei Thonny aber Code- und Shell-Bereich in einem Fenster zusammengefasst.

<img src="/static\python-raspberry-pi\raspberry-pi-thonny.png" alt="Thonny auf dem Raspberry Pi" class="img-fluid">

Auch diese IDE verfügt über die oben genannten IDE-Standards, so dass hier keine Präferenz für das eine oder das andere ausgesprochen werden kann. IDLE ist vielleicht ein wenig etablierter und bekannter, Thonny ein wenig frischer und kompakter und setzt in seinen Features eher auf das Erklären. Mit beiden lassen sich aber die ersten Schritte unter Python unternehmen und die Idee einer Entwicklungsumgebung mit ihren Features vermitteln.



Der Raspberry Pi ist kein super-performanter Entwicklungsrechner, aber zum Reinschnuppern reichen die kleinen IDEs auf alle Fälle. Grade für Schulen bietet sich der Pi wegen des günstigen Preises und der Möglichkeit, das Betriebssystem durch Einschieben einer neuen SD-Karte zu resetten, an. Insbesondere das an den C64 erinnernden [Raspberry Pi 400 Kit](https://amzn.to/314BnrL), mit dem in die Tastatur eingebauten Pi, dürfte hier eine interessante Wahl sein.

Eine Einführung in die Python-Entwicklung auf dem Pi findet sich im Buch [Raspberry Pi programmieren mit Python](https://amzn.to/2Qor0NB) von Michael Weigend.
