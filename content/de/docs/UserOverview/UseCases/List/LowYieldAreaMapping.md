---
title: "Nutzerübersicht - Minderertragsflächenkartierung"
linkTitle: "Minderertragsflächenkartierung"
weight: 100
---

## Allgemeines
### Ziel
Landwirten soll eine weitgehend automatisierte Erzeugung digitaler Minderertragskarten (auf Basis von Shapefiles) zu ihren Anbauflächen ermöglicht werden sowie eine automatisierte Bereitstellung von Handlungsempfehlungen zu deren Bewirtschaftung. Zur Erreichung dieser Ziele werden aus Satellitenbildern und meteorologischen Daten automatisch Informationen extrahiert (wie z.B. die Größe von Minderertragsarealen) und mit dem Wissen von Landwirten um örtliche Gegebenheiten (wie etwa die Ursache für den Minderertrag) verknüpft. Der hier beschriebene Anwendungsfall ermöglicht es, die dafür von Landwirten benötigten Informationen zu Eigenschaften von Minderertragsarealen auf pflanzenbaulich genutzten Flächen digital zu erfassen. Damit Landwirten durch die Erfassung der Informationen kein zusätzlicher Zeitaufwand entsteht, wird diese von der Landmaschine aus, während der Bewirtschaftung der zu kartierenden Felder, vorgenommen (vgl. Abb. 1).

![](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_fig01.jpg)

_**Abb. 1:** Zonenweise Erfassung ausgewählter Eigenschaften von Minderertragsarealen während der Bewirtschaftung pflanzenbaulich genutzter Flächen. (Photo: M. Enderling, Bearbeitung: S.C. Truckenbrodt)_

### Adressierte Nutzergruppe
* Landwirtinnen und Landwirte
* Fahrerinnen und Fahrer von Landmaschinen (z.B. Schlepper, Traktor, selbstfahrende Spritze, Mähdrescher, Kartoffelvollernter)

### Einsatzort
* Pflanzenbaulich genutzte Flächen (z.B. Acker, Schlag)

### Ausgabegrößen
* Shapefiles, die rechteckige Polygone enthalten, welche bei mit der kleinstmöglichen Ausdehnung Problemstandorte, hier potentielle Minderertragsflächen, einrahmen.

### Entwickler- und Projektmanagerübersicht
* Sie sind Entwickler/-in und möchten den Anwendungsfall weiterentwickeln oder adaptieren? <br>
  Dann geht es [hier](https://fieldmapp.github.io/docs/modules/drivingview/developers/) entlang zu weiteren Informationen.
* Sie sind Projektmanager und möchten mehr Informationen zur Nutzung der Fahrtansicht und den damit gewonnen Daten? <br>
  Dann können Sie sich [hier](https://fieldmapp.github.io/docs/modules/drivingview/projectmanagers/) dazu informieren.


## Hinweise zur Nutzung
### Einsatzszenario
ToDo

### Aufbau der Bedienoberflächen
ToDo

### Handhabung
ToDo

### Leitfaden zur bewährten Datenerfassung
ToDo

### Liste erfasster Kenngrößen
ToDo

### Unsicherheits- und Genauigkeitsangaben 
ToDo


## Hard- und Software-Ausstattung
### Rückgriff auf interne und externe Messgeräte
#### Liste erforderliche Sensoren
Interne Sensoren
| Sensorname | Zweck | Ersetzbar | Nutzungsempfehlung |
| -------------- | --------------- | --------------- | --------------- |
| GPS | Ermöglicht die Erfassung der Position bei der der Eingabe der Daten. | Ja <br> (Alternative: externes dGNSS) | wenig empfehlenswert |


#### Liste optional einsetzbarer Sensoren
Interne Sensoren
| Sensorname | Zweck | Nutzungsempfehlung |
| -------------- | --------------- | --------------- |
| Mikrophon | Ermöglicht die Nutzung der Spracherkennung und damit die Steuerung der Anwendung mittels Sprachbefehlen | sehr empfehlenswert |

Externe Sensoren
| Sensorname | Zweck | Nutzungsempfehlung |
| -------------- | --------------- | --------------- |
| Differentielles Global Navigation Satellite System ([dGNSS](https://fieldmapp.github.io/docs/useroverview/sensors/external/dgnss/)) | Ermöglicht die zentimetergenaue Erfassung der Position bei der Dateneingabe. Aufgrund der höheren Präzession des dGNSS-Sensor im Vergleich zum Geräteinternen GPS-Sensor, kann durch dessen Nutzung zu einer Verringerung des Gesamtfehlers bei der Datenaufnahme beigetragen werden. |sehr empfehlenswert |


### Veröffentlichte Software-Versionen
| Versionsnummer | Letzte Änderung | Downloadlink Anwendungsfall                    | Was wurde gegenüber vorheriger Version geändert |
| -------------- | --------------- | ---------------------------------------------- | ----------------------------------------------- |
| 0.1            | 01.02.2023      | [Link zu Version 0.1](https://www.example.org) | Wiki-Beitrag ergänzt                            |
| 0.0            | 23.02.2022      | [Link zu Version 0.0](https://www.example.org) | Wiki-Beitrag online gestellt                    |



## Weiterführende Informationen
### Posterbeiträge
* Truckenbrodt, S.C., M. Enderling, C. Pathe, E. Borg, C. Schmullius & F. Klan (2021): **Die FieldMApp – eine vielseitig einsetzbare Softwarelösung zur Datenaufnahme mit mobilen Endgeräten.** – 1. AgriSens FELDTAG „Einsatz von Fernerkundungstechnologien in der Landwirtschaft“, 4. November 2021, Kruckow, Deutschland (Poster). <br>
_[[pdf](https://elib.dlr.de/146508/1/AgriSensFeldtag21_AF2_Poster_FieldMApp_Aufbau_final.pdf)]_

### Vorträge
* Truckenbrodt, S.C., M. Enderling, E. Borg & F. Klan (2021): **AgriSens - DEMMIN 4.0 Anwendungsfall 2: Nachhaltige Bewirtschaftung.** – 1. AgriSens FELDTAG „Einsatz von Fernerkundungstechnologien in der Landwirtschaft“, 4. November 2021, Kruckow, Deutschland (Vortrag). <br>
_[[pdf](https://elib.dlr.de/146506/1/Truckenbrodt_etal_2021_FieldMApp.pdf)]_

### Publikationen
* Truckenbrodt, S.C., M. Enderling, E. Borg, C. Schmullius & F. Klan (2023): ** Benefits and Challenges of Participatory Design in Agriculture: The Example of the FieldMApp.** - Proceedings of Science 407, Austrian Citizen Science Conference 2022 (ACSC2022), 28.-30.06.2022, Dornbirn, Österreich. <br>
_[[pdf](https://doi.org/10.22323/1.407.0012)]_


## Autoren & Entwickler
### Konzeption
* Sina C. Truckenbrodt
* Friederike Klan
* Maximilian Enderling
* Erik Borg

### Dokumentation im Wiki
* Sina C. Truckenbrodt
* Maximilian Enderling

### Code Entwicklung
* Maximilian Enderling

## Zitationsvorschlag
Truckenbrodt, S.C., M. Enderling, E. Borg & F. Klan (2022): FieldMApp Nutzerübersicht. Anwendungsfall Minderertragsflächenkartierung. <https://fieldmapp.github.io/docs/useroverview/usecases/list/lowyieldareamapping/> (Stand: 2023-01-26) (Zugriff: YYYY-MM-DD).


## Lizenz
ToDo





_______________________
TODO:
# Einsatzszenario

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Liste erfassbarer Variablen

## Liste der Variablen

- Lorem ipsum
- dolor sit amet

## Variablen Definition und Kürzel

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

## Best-Practice-Guidline für Variablenerfassung

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Kopplung mit Profiling?

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Aufbau Benutzeroberfläche des Proflings

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Aufbau Nutzeroberfläche für den Anwendungsfall

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Beschreibung Handhabung/Workflow
**1. Anwendungsfall `Minderertragskartierung` im Menü der FieldMApp anwählen**


**2. Festlegen der Konfiguration der Benutzeroberfläche** (OPTIONAL)
<details><summary>2.1. Bereits vorhandene Konfiguration anpassen</summary>
 
 * auf der Startseite des Anwendungsfalls `Minderertragskartierung` den Namen einer vordefinierten Konfiguration (z.B. Standard) durch Antippen aus der Liste ausgewählt 
 * den Button `KONFIGURATION ANPASSEN` antippen, sodass die Konfigurationsansicht geöffnet wird (weiteres Vorgehen siehe 2-b-ii)
 
{{% pageinfo %}}
Durch das Anpassen einer Konfiguration wird die gespeicherte Ausgangskonfiguration überschrieben, auch wenn diese einen neuen Konfigurationsnamen erhält.
{{% /pageinfo %}}
</details>
 

<details><summary>2.2	Neue Konfiguration erstellen</summary>
 
 * Den Button `NEUE KONFIGURATION ERSTELLEN` antippen, sodass die Konfigurationsansicht geöffnet wird.
 * Anpassung des Konfigurationsnamens <br>
 In die Zeile hinter „Konfigurationsname“ tippen und mit dem sich öffnenden Tastenfeld den Namen eintragen, unter dem die Konfiguration gespeichert werden soll.
 * Festlegen der Bearbeitungsbreite <br>
 In die Zeile hinter „Bearbeitungsbreite (in Metern)“ tippen und mit dem sich öffnenden Ziffernblock die Bearbeitungsbreite in Metern eingeben, für welche die Kartierung erfolgen soll.
 * Festlegen der kartierbaren Minderertragsursachen <br>
 Nacheinander jedes der zur Verfügung stehenden Felder unter „Auswahl Minderertragsursache“ Antippen und festlegen, ob dieses zu einem Button mit einer Minderertragsursache werden soll.
   * _Falls ja:_ Aus der erscheinenden Liste (Abb. 2-B) eine Minderertragsursache (Abb. 2-B2) durch Antippen auswählen oder durch Antippen von `Neu erstellen` (Abb. 2-B3), das Fenster öffnen, über das eine neue, die Liste ergänzende Ursache eingeben und durch Tippen auf `OK` hinzugefügt werden kann (Abb. 2-C).
   * _Falls nein:_ Aus der erscheinenden Liste `Schaltfläche verstecken` durch Antippen auswählen.
 * Festlegen der Zonenanzahl <br>
 Unter „Anzahl der Zonen“ kann die Anzahl der Zonen, welche symmetrisch jeweils auf die halbe Bearbeitungsbreite rechts bzw. links der Fahrspur verteilt werden soll, durch den Schieberegler festgelegt werden.
 * Durch Antippen von `Speichern` wird die Konfiguration unter dem angegebene Konfigurationsnamen gespeichert. 
 
{{% pageinfo %}}
Durch erneutes Ausführen einzelner Konfigurationsschritte können Korrekturen vorgenommen werden.
{{% /pageinfo %}}
</details><br>


**3. Konfiguration der Bedienoberfläche auswählen** 
<details><summary>3.1 Auswahl</summary>
 
 * Die Auswahl erfolgt indem der Name einer vordefinierten Konfiguration (z.B. Standard) durch Antippen aus der Liste ausgewählt und durch berühren des Buttons „AUSGEWÄHLTE KONFIGURATION BENUTZEN“ geöffnet wird.
</details><br>


**4. Datenaufnahme mit der Fahrtansicht** 
<details><summary>4.1 Markieren des Anfangs einer Minderertragsfläche</summary>
 
 * Lorem ipsum dolor
 * Lorem ipsum dolor
</details>

<details><summary>4.2 Eingabe der Eigenschaften von Minderertragsflächen</summary>
 
 * Lorem ipsum dolor
 * Lorem ipsum dolor
</details>

<details><summary>4.3 Markieren des Endes einer Minderertragsfläche</summary>
 
 * Lorem ipsum dolor
 * Lorem ipsum dolor
</details>

<details><summary>4.4 Korrektur bei Falscheingaben</summary>
 
 * Lorem ipsum dolor
 * Lorem ipsum dolor
</details>
<br>


# Rückgriff auf interne und externe Messgeräte

## Liste erforderliche Sensoren

Jeweils mit Kennzeichnung, ob dieser Sensor intern/extern ist
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

## Liste optional einsetzbarer Sensoren

Jeweils mit Kennzeichnung, ob dieser Sensor intern/extern ist
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Versionen des Anwendungsfall

| Versionsnummer | Letzte Änderung | Downloadlink Profiling | Downloadlink Anwendungsfall | Was wurde gegenüber vorheriger Version geändert |
| -------------- | --------------- | ---------------------- | --------------------------- | ----------------------------------------------- |
| 1.0            | Lorem           |https://www.example.org | https://www.example.org     | Lorem ipsum dolor sit amet                      |

# Weiterführende Informationen

Links zu Anwendungsfallspezifischen Publikationen

# Link zur zugehörigen Entwickler- und Projektmanagerübersicht

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Autoren & Entwickler
## Konzeption
* Sina C. Truckenbrodt
* Friederike Klan
* Maximilian Enderling
* Erik Borg

## Dokumentation im Wiki
* Sina C. Truckenbrodt
* Maximilian Enderling

## Code Entwicklung
* Maximilian Enderling

## Zitationsvorschlag
Truckenbrodt, S.C., M. Enderling, E. Borg & F. Klan (2022): FieldMApp Nutzerübersicht. Anwendungsfall Minderertragsflächenkartierung. <https://fieldmapp.github.io/docs/useroverview/usecases/list/lowyieldareamapping/> (Stand: 2023-01-26) (Zugriff: YYYY-MM-DD).

# Lizenz

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
