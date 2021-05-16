---
layout: default
title:  Python mit Anaconda
image: /static/anaconda/anaconda-navigator.JPG
date:   2020-05-13
category: tools
kw: python anaconda
---

Python ist die Sprache der Wahl für Projekte im Umfeld von Machine Learning und Data Science. Verschiedene Versionen der Sprache selbst, aber vor allen Dingen tausende in diesem Kontext benötigten Pakete und Bibliotheken sind schwer zu kontrollieren. Zum Glück steht mit **[Anaconda](https://www.anaconda.com/)** ein Werkzeug zur Verfügung, das hilft den Überblick zu behalten und das Projekt zu verwalten.

*Anaconda* bezeichnet sich selbst als Data Science-Plattform, ist also eine Python-Distribution mit Fokus auf vorhersagende Analyse und wissenschaftliche Berechnungen.

Enthalten sind unter anderem:

- der Conda Package Manager mit dem zugehörigen Repository
- die Programmiersprachen Python und R
- ein Cloud Repository zum Teilen von eigenen Projekten
- ein Manager für virtuelle Umgebungen
- Jupyter Notebooks und andere Entwicklungsumgebungen wie Spyder oder RStudio
- der Anaconda Navigator

Die *Individual Edition* der aktuellen Version Anaconda 3 ist kostenlos erhältlich und richtet sich an Solo-Entwickler. Für Teams oder Unternehmen stehen umfangreichere, aber kostenpflichtige Editionen bereit.

## Installation von Anaconda
Anaconda ist für Windows, Mac OS und Linux jeweils für Python 2.7 und Python 3.7 verfügbar. Die ARM-Architektur wird leider noch nicht unterstützt, es gibt also keine offizielle Version für den Raspberry Pi. Mit Miniconda (Link) steht aber eine abgespeckte Variante zur Verfügung. Der graphische Installer ist 460 MB groß, die Installation beinhaltet keine großen Hürden.

## Anaconda Navigator
Nach der Installation lässt sich der *Anaconda Navigator* starten, der den Überblick über alle Anwendungen, Pakete und Umgebungen bietet. Auf der linken Seite findet sich ein Menü, dessen erster Punkt "Home" lautet. Hier lassen sich weitere Anwendungen wie das bekannte Jupyter Notebook oder die IDE Spyder installieren oder bereits installierte Anwendungen starten.

<img src="/static/anaconda/anaconda-navigator.JPG" alt="Anaconda Navigator" class="img-fluid">

## Conda
Conda ist ein Paketmanager ähnlich Pip, geht aber über dessen Leistungsumfang hinaus. Pip ist explizit für Python-Pakete gedacht, mit Conda dagegen lassen sich auch C-Bibliotheken oder R-Pakete verwalten. Das Werkzeug ist von der Kommandozeile aus erreichbar. Um beispielsweise TensorFlow in der CPU-Variante zu installieren, sind die folgenden Eingaben erforderlich:

    conda create -n tf tensorflow
    conda activate tf

Conda lädt und installiert dann die erforderlichen Pakete.


## Virtuelle Umgebungen
In Python-Projekten arbeitet man bevorzugt in isolierten virtuellen Umgebungen. Sie erlauben die Abhängigkeiten in Form von Paketen und Modulen verschiedener Projekte auseinanderzuhalten. Im Prinzip ist das eine Verzeichnisstruktur wo genau die passende Python-Version und erforderliche Pakete für das jeweilige Projekt enthalten sind. Die zuvor für TensorFlow angelegte und aktivierte Umgebung namens *tf* ist nun im Anaconda Navigator unter *Environments* zu finden. Nach der Auswahl des Umgebungsnamens werden auf der rechten Seite die enthaltenen Pakete mit ihren jeweiligen Versionen aufgelistet.
