---
layout: default
title: "Die Python IDE Thonny"
image: /static/python-ide-thonny/thonny-logo.png
category: tools
tags: ide, micropython, pico
vgwort: <img src="https://vg08.met.vgwort.de/na/c85cbdd920214ff7a7a10450efbfabec" width="1" height="1" alt="">

# KW: thonny
---

**Thonny, die Python IDE for Beginners**, ist eine kompakte Python-IDE, die sich hervorragend zum Lernen der Sprache, aber auch für das Programmieren von ESP-Boards oder den Raspberry Pi Pico eignet.

Um mit MicroPython auf einem ESP-Board oder dem neuen Raspberry Pi Pico zu kommunizieren, kann man REPL nutzen. Die Shell nimmt einzelne Benutzereingaben auf und gibt das Ergebnis an den Benutzer zurück. Das funktioniert, ist aber nicht sonderlich komfortabel. Eine Alternative ist die kleine IDE [Thonny](https://thonny.org), die nur etwas über 80 MB Platz auf der Platte belegt. Im Download enthalten ist der aktuelle Python-Interpreter in der Version 3.7.9, so dass für den Start nichts weiter benötigt wird.

Der folgende Screenshot zeigt die IDE nach dem Start:

<img src="/static/python-ide-thonny/thonny.png" alt="Thonny, eine kleine IDE für MicroPython" class="img-fluid">

Wie man erkennen kann, beschränkt sich die IDE auf das Wesentliche. Im oberen Textfeld lässt sich Programmcode eingeben. Ausgeführt wird er nach dem Speichern mit dem grünen Pfeil in der Toolbar. Die Ausgaben erscheinen dann in der Konsole im unteren Bereich.

**Thonny** ist mit den gängigen IDE-Features ausgestattet. Die Syntax des Codes wird durch Highlighting in verschiedenen Farben hervorgehoben. Funktionen werden beim Tippen durch Auto-Completion vervollständigt. Im Bereich links neben dem Code lassen sich Breakpoints setzen. Führt man dann das Script im Debug-Modus (starten mit dem Button mit dem Käfer drauf) aus, dann stoppt die Ausführung am Haltepunkt und mit Hilfe der View *Variablen* lassen sich die Inhalte der Variablen untersuchen. Die üblichen Debugging-Kommandos wie *Step Into*, *Step Over* stehen natürlich auch zur Verfügung. Thonny ist eine gute Alternative zu IDLE. An ausgewachsene kommerzielle Produkte wie PyCharm kommt die kleine IDE nicht heran, das ist aber auch nicht das Ziel.

## Thonny & Raspberry Pi Pico

Gut gelungen ist die Integration mit dem Raspberry Pi Pico. Das ist kein Wunder, die Macher von Thonny arbeiten mit der Raspberry Pi Foundation zusammen. Nach dem Start von Thonny lässt sich in der rechten unteren Ecke der Python-Interpreter auswählen (dort wo die Python-Version angezeigt wird). Wenn ein Pico mit einem USB-Kabel verbunden ist, findet man hier die die Option *MicroPython (Raspberry Pi Pico)*. Der in Thonny eingegebene Code wird dann direkt auf dem Pico ausgeführt.
