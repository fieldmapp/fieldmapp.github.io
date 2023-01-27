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
Die Funktionen, welche die Bedienoberfläche (vgl. Abb. 4) bereithält, ermöglichen:
* die Auswahl von bis zu drei Zonen links (Abb. 4-A) und rechts (Abb. 4-B) der Fahrspur. Für eine einzelne Zone oder mehrere Zonen gleichzeitig, kann:
* der Anfang einer Minderertragsfläche durch Antippen der bzw. Wischen über die entsprechende(n) Zonennummer(n) bei A1 bzw. B1 (siehe Abb. 4) festgelegt werden,
* das Tastenfeld zur Eingabe der Ertragsminderung und der Ursache durch Antippen der bzw. Wischen über die entsprechende(n) Zonennummer(n) bei A2 bzw. B2 (siehe Abb. 4) aktiviert werden,
* das Ende einer Minderertragsfläche durch Antippen der bzw. Wischen über die entsprechende(n) Zonennummer(n) bei A3 bzw. B3 (siehe Abb. 4) festgelegt werden.

* die Erfassung der Intensität der (zu erwartenden) Ertragsminderung (Abb. 4-C), und
* die Erfassung der Ursache(n), welche die (zu erwartende) Ertragsminderung hervorrufen (Abb. 4-D).

![](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_fig04_de.svg)
_**Abb. 4:** Aufbau der Bedienoberfläche des Anwendungsfalls „Minderertragsflächenkartierung“: Die Hälften der Bearbeitungsbreite links und rechts der Fahrspur werden durch Bereiche A und B repräsentiert. Im dargestellten Beispiel sind beide Bereich in jeweils drei Zonen (Zone 1-3 im Bereich A und Zone 4-6 im Bereich B) unterteilt. Durch Auswahl der Zonen können die Intensität (C) und die Ursachen (D) der (zu erwartenden) Ertragsminderung erfasst werden._

### Handhabung
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

### Leitfaden zur bewährten Datenerfassung
 * Für ein Feld sollte die Erfassung der Minderertragsflächen mehrmals unabhängig voneinander erfolgen. Auf diese Weise soll sichergestellt werden, dass
   * … alle potentiellen Minderertragsstandorte erfasst werden, auch wenn deren Ausprägung nur unter unterschiedlichen Witterungsbedingungen entsteht.
   * … die größtmögliche Ausdehnung der potentiellen Minderertragsfläche kartiert wird sowie die üblicherweise auftretende Varianz in der Ausdehnung.
   * … anhand der Analyse der Häufigkeitsverteilung einer erfassten Eigenschaft (wie z.B. der Minderertragsursache) eventuell erfolgte Fehlangaben ausgeschlossen werden können.<br>

 * Sollte lokal eine exakte Erfassung der Problemstandorte während einer Befahrung nicht möglich sein, z.B. auf Grund einer hohen standörtlichen Heterogenität, empfehlen wir die Erfassung auf den Teil der Problemstandorte zu beschränken, die bei erhalt der Qualität leistbar ist. Die verbleibenden Problemstandorte können bei späteren Befahrungen ergänzt werden.


### Liste erfasster Kenngrößen
| Kenngröße      | Kürzel          | Definition      | Auswahloptionen |
| -------------- | --------------- | --------------- | --------------- |
| Zeit | UtcDateTime | Datum und Uhrzeit (bezogen auf die koordinierte Weltzeit (UTC – Universal Time Coordinated)) der Eingabe durch den Nutzer |  |
| Ortskoordinaten | UtcDateTime | Koordinaten des Ortes der Eingabe durch den Nutzer im Rohdatenformat RTCM 3.3|  |
| Zonennummer | LaneIndex | Nummer des Streifens (= Zone) links oder rechts der Fahrspur, für den die Dateneingabe durch den Nutzer erfolgt | „1“, „2“, „3“, „4“, „5“, „6“ |
| Beginn Minderertragszone | Action | Markiert den Beginn einer Minderertragsfläche, innerhalb einer Zone. | „Start“ |
| Ende Minderertragszone | Action | Markiert das Ende einer Minderertragsfläche, innerhalb einer Zone. | „Stop“ |
| Ursache | Action cause | Grund, der das beobachtete verminderte Pflanzenwachstum und somit den (zu erwartenden) Minderertrag hervorruft. | „Sandlinse“, „Verdichtung“, Vorgewende“, „Kuppe“, Hang“, „Waldrand“, „Trockenstress“, „Nassstelle“, „Mäusefraß/Wildschaden“ |
| Ertragsminderung | Action damage | Aktuell zu beobachtender Grad der Beeinträchtigung des Pflanzenwachstums und des deshalb (zu erwartenden) Minderertrags | „gering“, „mittel“, „hoch“ |


### Unsicherheits- und Genauigkeitsangaben 
ToDo


## Hard- und Software-Ausstattung
### Rückgriff auf interne und externe Messgeräte
#### Liste erforderliche Sensoren
Interne Sensoren
| Sensorname     | Zweck                                                                | Ersetzbar                             | Nutzungsempfehlung |
| -------------- | -------------------------------------------------------------------- | ------------------------------------- | -------------------- |
| GPS            | Ermöglicht die Erfassung der Position bei der Eingabe der Daten. | Ja <br> (Alternative: externes dGNSS) | wenig empfehlenswert |


#### Liste optional einsetzbarer Sensoren
Interne Sensoren
| Sensorname     | Zweck                                                                                                   | Nutzungsempfehlung  |
| -------------- | ------------------------------------------------------------------------------------------------------- | ------------------- |
| Mikrophon      | Ermöglicht die Nutzung der Spracherkennung und damit <br>die Steuerung der Anwendung mittels Sprachbefehlen | sehr empfehlenswert |


Externe Sensoren
| Sensorname     | Zweck           | Nutzungsempfehlung |
| -------------- | --------------- | ------------------ |
| Differentielles Global Navigation Satellite System ([dGNSS](https://fieldmapp.github.io/docs/useroverview/sensors/external/dgnss/)) | Ermöglicht die zentimetergenaue Erfassung der Position bei der Dateneingabe. Aufgrund der höheren Präzession des dGNSS-Sensor im Vergleich zum Geräteinternen GPS-Sensor, kann durch dessen Nutzung zu einer Verringerung des Gesamtfehlers bei der Datenaufnahme beigetragen werden. |sehr empfehlenswert |


### Veröffentlichte Software-Versionen
| Versionsnummer | Letzte Änderung | Downloadlink Anwendungsfall                    | Was wurde gegenüber vorheriger Version geändert |
| -------------- | --------------- | ---------------------------------------------- | ----------------------------------------------- |
| 0.1            | 27.01.2023      | [Link zu Version 0.1](https://www.example.org) | Wiki-Beitrag ergänzt                            |
| 0.0            | 23.02.2022      | [Link zu Version 0.0](https://www.example.org) | Wiki-Beitrag online gestellt                    |



## Weiterführende Informationen
### Posterbeiträge
* Truckenbrodt, S.C., M. Enderling, C. Pathe, E. Borg, C. Schmullius & F. Klan (2021): **Die FieldMApp – eine vielseitig einsetzbare Softwarelösung zur Datenaufnahme mit mobilen Endgeräten.** – 1. AgriSens FELDTAG „Einsatz von Fernerkundungstechnologien in der Landwirtschaft“, 4. November 2021, Kruckow, Deutschland (Poster). <br>
_[[pdf](https://elib.dlr.de/146508/1/AgriSensFeldtag21_AF2_Poster_FieldMApp_Aufbau_final.pdf)]_

### Vorträge
* Truckenbrodt, S.C., M. Enderling, E. Borg & F. Klan (2021): **AgriSens - DEMMIN 4.0 Anwendungsfall 2: Nachhaltige Bewirtschaftung.** – 1. AgriSens FELDTAG „Einsatz von Fernerkundungstechnologien in der Landwirtschaft“, 4. November 2021, Kruckow, Deutschland (Vortrag). <br>
_[[pdf](https://elib.dlr.de/146506/1/Truckenbrodt_etal_2021_FieldMApp.pdf)]_

### Publikationen
* Truckenbrodt, S.C., M. Enderling, E. Borg, C. Schmullius & F. Klan (2023): **Benefits and Challenges of Participatory Design in Agriculture: The Example of the FieldMApp.** - Proceedings of Science 407, Austrian Citizen Science Conference 2022 (ACSC2022), 28.-30.06.2022, Dornbirn, Österreich. <br>
_[[pdf](https://pos.sissa.it/407/012/pdf)]_

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




# Versionen des Anwendungsfall

| Versionsnummer | Letzte Änderung | Downloadlink Profiling | Downloadlink Anwendungsfall | Was wurde gegenüber vorheriger Version geändert |
| -------------- | --------------- | ---------------------- | --------------------------- | ----------------------------------------------- |
| 1.0            | Lorem           |https://www.example.org | https://www.example.org     | Lorem ipsum dolor sit amet                      |

