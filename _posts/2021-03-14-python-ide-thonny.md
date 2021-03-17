---
layout: default
title: "Die Python IDE Thonny"
image: /static/python-ide-thonny/thonny-logo.png
category: tools
tags: ide, micropython
vgwort:
---

**Thonny, die Python IDE for Beginners**, ist eine kompakte Python-IDE, die sich hervorragend zum Lernen der Sprache, aber auch für das Programmieren von ESP-Boards oder den  Raspberry Pi Pico eignet.

Um mit MicroPython auf einem ESP-Board oder dem neuen Raspberry Pi Pico zu kommunizieren kann man REPL nutzen. Die Shell nimmt einzelne Benutzereingaben auf und gibt das Ergebnis an den Benutzer zurück. Das funktioniert, ist aber nicht sonderlich komfortabel. Eine Alternative ist die kleine IDE [Thonny](https://thonny.org), die nur etwas über 80 MB Platz auf der Platte belegt. Im Dwonload enthalten ist der aktuelle Python-Interpreter in der Version 3.7.9, so dass für den Start nichts weiter benötigt wird.

Der folgende Screenshot zeigt die IDE nach dem Start:

![Thonny, eine kleine IDE für MicroPython.](/static/python-ide-thonny/thonny.png)

Wie man erkennen kann beschränkt sich die IDE auf das Wesentliche. Im oberen Textfeld lässt sich Programmcode eingeben. Dieser kann nach dem Speichern mit dem grünen Pfeil ausgeführt werden. Die Ausgaben erscheinen dann in der Konsole im unteren Bereich.

Thonny ist mit den gängigen IDE-Features ausgestattet. Die Syntax des Codes wird durch Highlighting in verschiedenen Farben hervorgehoben. Funktionen werden beim Tippen durch Auto-Completion vervollstämndigt. Im Bereich links neben dem Code lassen sich Haltepunkte setzen. Führt man dann das Script im Debug-Modus (der Button mit dem Käfer drauf) aus, so stoppt die Ausführung und mit Hilfe der View Variablen lassen sich die Inhalte der Variablen untersuchen. Die üblichen Debugging-Kommandos wie Step Into, Step Over stehen natürlich auch zur Verfügung. Thonny ist eine gute Alternative zu IDLE. An ausgewachsene kommerzielle Produkte wie PyCharm kommt die kleine IDE nicht heran, das ist aber auch nicht das Ziel.




Gut gelungen ist die Inztegration mit XXX.  Nach dem Start von Thonny lässt sich in der rechten unteren Ecke der Python-Interpreter auswählen.

 Zum Ausführen des Codes auf dem Pico wählt man hier die Option *MicroPython (Raspberry Pi Pico)* aus. Danach kann man beispielsweise den LED-Code von oben in das obere Textfeld eingeben und mit Run (das Icon mit dem grünen Pfeil) direkt auf dem Pico ausführen.
