# Adresssuche

### _QGIS-Plugin zur Suche von Adressen_

Fragen, Anmerkungen, Fehlermeldungen, etc. bitte gerne per E-Mail an [thomas.knaeuper@stud.hs-bochum.de] mitteilen.

<!-- <img src="./screenshots/flurstuecksfinder.gif"> -->

## Inhalt
- [Hinweise](#hinweise)
- [Features](#features)
- [Installation](#installation)
- [Verwendung](#verwendung)
  - [Reiter Daten](#reiter-daten)
  - [Reiter Suche](#reiter-suche)

- [Daten](#daten)
  - [Verwendete WFS-Dienste](#verwendete-wfs-dienste)
  - [Katasterämter, Gemarkungen und Fluren](#katasterämter-gemarkungen-und-fluren)
  - [Lizenz der Daten](#lizenz-der-daten)


## Hinweise
Die Adresssuche ist für die Suche im Hauskoordinatenformat vorgesehen.  
Auf der Webseite der [AdV] wird dieses genauer erläutert.


## Features
- Suche von Adressen über:
    - Straße
    - Hausnummer
    - Adresszusatz
    - Postleitzahl
    - Ort

## Installation

Das Plugin ist im offiziellen [QGIS-Plugin-Repository] enthalten und kann in QGIS über *Erweiterungen -> Erweiterungen verwalten und installieren* installiert und auch bei Verfügbarkeit einer neuen Version aktualisiert werden.


## Verwendung

### Reiter Einstellungen

<img src="./screenshots/reiter_einstellungen.png" width="300">

Hier kann der Katasteramtsbezirk (z.B. Stadt, Kreis, Städteregion) im Bereich "Einstellungen" ausgewählt werden.

- **NRW:**<br>
  Auswahl des Kastasteramtsbezirks über das Dropdown-Menü, Flurstückssuche auf Basis des NRW-WFS-Dienstes.<br><br>
  Anmerkung: Das Werkzeug [Flurstück mit Klick auf die Karte finden](#flurstück-mit-klick-auf-die-karte-finden) funktioniert landesweit auch ohne explizite Auswahl eines Katasteramtsbezirks.

- **Kreis Viersen, Kleve, Wesel und Stadt Krefeld:**<br>
  Flurstückssuche auf Basis des enstprechenden KRZN-WFS-Dienstes (wochenaktuell).

Die Option "Flurstück highlighten" markiert das Flurstück. Die Markierung wird so lange angezeigt bis das Plugin geschlossen oder ein neues Flurstück gesucht wird. Wird die Option deaktiviert, so wird nur der Umring des Flurstücks kurz blinkend hervorgehoben.

### Reiter Flurstück suchen


<img src="./screenshots/reiter_flurstueck_suchen.png" width="300">

Im Reiter „Flurstück suchen“ gibt es mehrere Möglichkeiten, um nach einem Flurstück zu suchen:

1. Über die Dropdown-Menüs Gemarkung, Gemarkungsschlüssel, Flurnummer und Flurstücksnummer
2. Direkte Suche über das verkürzte Kennzeichen Gemarkung-Flur-Flurstück (z.B. `3230-1-1`)
3. Über die ALKIS-ID (z.B. `DENW33AL00009NPL`)
4. Über das Flurstückskennzeichen, z.B. `05320308900675______` (20 Zeichen)

Bei Variante 1 stehen nur Elemente zur Auswahl, die auf dem WFS-Server für den jeweiligen Kastasteramtsbezirks vorhanden sind.
Variante 2, 3 und 4 ermöglichen die direkte Suche über ein Kennzeichen oder eine ALKIS-ID. Die Suche kann hier mit einem Klick auf das Lupen-Symbol oder mit der ENTER/Return-Taste ausgeführt werden. Ist _NRW_ im Reiter Einstellungen ausgewählt, wird mit einer ID NRW-weit gesucht.

Sobald ein gültiges Flurstück ausgewählt oder gesucht wurde, werden die Knöpfe freigeschaltet und das ausgewählte Flurstück im Kartenfenster angesteuert.

#### Funktionsknöpfe
| Funktionsknopf | Funktion |
|--|--|
| <img src="./icons/web.png" width="40">  | Das Globus-Symbol öffnet [TIM-online] (bei Verwendung des NRW-WFS) bzw. das [Geoportal Niederrhein] (bei Verwendung des KRZN-WFS für Kreis Viersen, Kleve, Wesel oder Stadt Krefeld) an der Position des gewählten Flurstücks. |
| <img src="./icons/ideditor.png" width="40">  | Das iD-Symbol stellt eine Verbindung zum OpenStreetMap [iD]-Editor her. Zur Bearbeitung ist ein kostenloses  [OpenStreetMap-Benutzerkonto] erforderlich.|
| <img src="./icons/josm.png" width="40">  | Das Karten-Symbol stellt eine Verbindung zu [JOSM] (Java OpenStreetMap Editor) her.<br>Diese Funktion sollte nur genutzt werden, wenn JOSM auf dem Endgerät in einem der beiden folgenden Verzeichnisse installiert ist:<br>`C:\Program Files (x86)\JOSM` oder<br>`C:\Users\[Windows-User]\AppData\Local\JOSM`.<br>Zur Bearbeitung ist ein kostenloses [OpenStreetMap-Benutzerkonto] erforderlich.|
| <img src="./icons/add.png" width="40">  | Durch einen Klick auf das Plus-Symbol kann das Polygon des Flurstücks dem Kartenbild hinzugefügt werden. |
| <img src="./icons/remove.png" width="40">  |  Durch das Minus-Symbol wird das mit Klick auf das Plus-Symbol hinzugefügte Flurstück wieder entfernt. |



## Daten




[thomas.knaeuper@stud.hs-bochum.de]: <mailto:thomas.knaeuper@stud.hs-bochum.de?subject=Adresssuche%20Plugin>
[Adv]:<a href="https://www.adv-online.de/AdV-Produkte/Standards-und-Produktblaetter/ZSHH/" target="_blank">Hello, world!</a>
[QGIS-Plugin-Repository]: <https://github.com/thmskn/address_search>