---
title: "Nutzerübersicht - Minderertragsflächenkartierung"
linkTitle: "Minderertragsflächenkartierung"
weight: 100
---

## Allgemeines
### Ziel
Landwirten soll eine weitgehend automatisierte Erzeugung digitaler Karten von potentiellen Minderertragsstandorten (auf Basis von Shapefiles) zu ihren Anbauflächen ermöglicht werden, sowie eine automatisierte Bereitstellung von Handlungsempfehlungen zu deren Bewirtschaftung. Zur Erreichung dieser Ziele werden aus Satellitenbildern und meteorologischen Daten automatisch Informationen extrahiert (wie z.B. die Größe von Minderertragsarealen) und mit dem Wissen von Landwirten um örtliche Gegebenheiten (wie etwa die Ursache für den Minderertrag) verknüpft. Der hier beschriebene Anwendungsfall ermöglicht es, die dafür von Landwirten benötigten Informationen zu Eigenschaften von Minderertragsarealen auf pflanzenbaulich genutzten Flächen digital zu erfassen. Damit Landwirten durch die Erfassung der Informationen kein zusätzlicher Zeitaufwand entsteht, wird diese von der Landmaschine aus, während der Bewirtschaftung der zu kartierenden Felder, vorgenommen (vgl. Abb. 1).

![](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_fig01.jpg)

_**Abb. 1:** Zonenweise Erfassung ausgewählter Eigenschaften von Minderertragsarealen während der Bewirtschaftung pflanzenbaulich genutzter Flächen. (Photo: M. Enderling, Bearbeitung: S.C. Truckenbrodt)_

### Adressierte Nutzergruppe
* Landwirtinnen und Landwirte
* Fahrerinnen und Fahrer von Landmaschinen (z.B. Schlepper, Traktor, selbstfahrende Spritze, Mähdrescher, Kartoffelvollernter)

### Einsatzort
* Pflanzenbaulich genutzte Flächen (z.B. Acker, Schlag)

### Ausgabegrößen
* Shapefiles, die Polygone (Vielecke) enthalten, welche die kleinstmögliche Ausdehnung von Problemstandorten, hier potentiellen Minderertragsflächen, kennzeichnen. Die Polygone werden von einem Rechteck oder mehreren aneinandergrenzenden oder sich überlappenden Rechtecken gebildet.

### Entwickler- und Projektmanagerübersicht
* Sie sind Entwickler/-in und möchten den Anwendungsfall weiterentwickeln oder adaptieren? <br>
  Dann geht es [hier](https://fieldmapp.github.io/docs/modules/drivingview/developers/) zu weiteren Informationen.
* Sie sind Projektmanager und möchten mehr Informationen zur Nutzung der Fahrtansicht und den damit gewonnen Daten? <br>
  Dann können Sie sich [hier](https://fieldmapp.github.io/docs/modules/drivingview/projectmanagers/) dazu informieren.


## Hinweise zur Nutzung
### Einsatzszenario
Der Anwendungsfall Minderertragsflächenkartierung dient der digitalen Erfassung ausgewählter Eigenschaften innerhalb von Äckern gelegener flächenhafter Problemstandorte – hier potentieller Minderertragsflächen. Der Anwendungsfall ist so konzipiert, dass dieser von Landmaschinenfahrenden während der Bewirtschaftung von Ackerflächen eingesetzt werden kann. Zur Erfassung der Lage der potentiellen Minderertragsflächen werden die Bereiche links und rechts der Fahrspur in Zonen unterteilt (z. B. 2 x 3 Zonen in Abb. 1). Zusammengenommen entsprechen die parallel zur Fahrspur verlaufenden Zonen der Bearbeitungsbreite. Taucht in einer der Zonen auf Höhe des Bewirtschaftenden ein Problemstandort auf, wird für diese Zone mit Hilfe der FieldMApp die Datenaufnahme, durch die Lokalisierung des Anfangspunktes, gestartet (siehe Video 1). In dem Moment, in dem das Ende des Problemstandorts in dieser Zone passiert wird, wird das Zonenende und damit indirekt die Ausdehnung des Problemstandorts innerhalb dieser Zone erfasst (siehe Video 1). 

[![Aktivierung und Deaktivierung von Zonen mit der FieldMApp](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_video01_de.jpg)](https://youtu.be/h3IqRWEvcCc-Y?t=0s "Aktivierung und Deaktivierung von Zonen mit der FieldMApp")

_**Video 1:** Erfassung der Ausdehnung von Minderertragsflächen (links: hellgrüne Objekte) mit der FieldMApp-Fahrtansicht (rechts) durch die Aktivierung und Deaktivierung der betreffenden Zonen, durch Antippen der entsprechenden Zonennummern neben "Start" bzw. "Stop". Die dabei entstehenden hellblauen Boxen stellen das Kartierungsergebnis dar. (Animation: M. Enderling, Graphikelemente S.C. Truckenbrodt)_

Nach dem Start der Lokalisierung eines Problemstandorts in einer Zone ist die Erhebung von dessen Eigenschaften möglich, solange in dieser Zone nicht mit der Erhebung eines neuen Problemstandorts begonnen wurde. Nach und nach wird so ein umfassendes Bild zur Lage der Problemstandorte geschaffen (siehe Abb. 2).

Da sich der Arbeitsaufwand bei jeder Bewirtschaftung (in Abhängigkeit von der durchgeführten Maßnahme, dem phänologischen Stadium, den Witterungsbedingungen, der Arbeitsbreite, der Minderertragsflächendichte usw.) unterscheiden kann, besteht die Möglichkeit, die Bedienoberfläche zur Datenaufnahme individuell zu konfigurieren. Parameter, die dadurch angepasst werden können, sind:

* die Bearbeitungsbreite, auf die sich die Datenaufnahme bezieht, 
* die Anzahl der Zonen, in die diese Breite unterteilt wird, und
* die Anzahl der Minderertragsursachen, die in der aktuellen Situation ausgeprägt sind und somit kartiert werden können.

Unabhängig von der gewählten Konfiguration ist bei jeder Kartierung eine möglichst exakte Erfassung der Minderertragsflächen und deren Eigenschaften anzustreben. Sollte die Arbeitsbelastung oder die Dichte der Minderertragsflächen zu einer zeitweisen Überlastung des Fahrers/der Fahrerin führen, wird empfohlen, die Kartierung auf wenige Flächen zu reduzieren bzw. diese zeitweise auszusetzen. Da die Kartierung von Minderertragsflächen in einem Feld wiederholt (während verschiedener Bearbeitungsschritte) erfolgen soll, ist davon auszugehen, dass eventuell entstandene Datenlücken mit der Zeit geschlossen werden. Darüber hinaus ermöglicht die mehrfache Kartierung der gleichen Minderertragsflächen eine Abschätzung der Genauigkeit für die Ergebniskarte.

Die Ergebniskarte bzw. das Ergebnis-Shapefile wird nach Abschluss der Datenerfassung automatisch erzeugt. Dabei werden aneinandergrenzende kartierte Areale mit gleichen Eigenschaften vereinigt, sodass daraus Polygone hervorgehen. Letztlich sollte jeder Problemstandort durch ein Polygon repräsentiert sein (Abb. 3). Polygone, die einem Thema, wie z.B. potentiellen Minderertragsflächen, zuzuordnen sind, werden in einem Shapefile zusammengefasst. Dieses kann zur Bewirtschaftungsplanung oder als Orientierungshilfe, z.B. für neue Mitarbeiter/-innen, genutzt werden.


![](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_fig02.png)

_**Abb. 2:** Eingrenzung der Minderertragsareale, die innerhalb von jeweils drei Zonen links und rechts der Fahrspur liegen, durch Boxen. Gruppierte gleichfarbige Boxen, die links und rechts einer Fahrspur liegen, wurden während der Befahrung dieser aufgenommen. (Photo: B. Weier, Bearbeitung: S.C. Truckenbrodt)_


![](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_fig03_de.svg)

_**Abb. 3:** Darstellung des Ergebnis-Shapefiles, das aus einer Kartierung von potentiellen Minderertragsflächen mit Hilfe der FieldMApp abgeleitet wurde. Die zugrunde liegende FieldMApp-Kartierung ist in Abbildung 2 dargestellt._


### Aufbau der Bedienoberflächen

**Bedienoberfläche zur Konfiguration der Fahrtansicht**

Die Konfigurationsansicht (Abb. 4-A), mit deren Hilfe die Bedienoberfläche zur Datenaufnahme den individuellen Anforderungen entsprechend ausgestaltet bzw. angepasst werden kann, ist über den Button `NEUE KONFIGURATION ERSTELLEN` bzw. `KONFIGURATION ANPASSEN` zu erreichen. 
Folgende Anpassungen werden durch die Konfigurationsansicht ermöglicht:

* Vergabe bzw. Anpassung eines Konfigurationsnamens (Abb. 4-A1), unter dem die vorgenommenen Einstellungen gespeichert (Abb. 4-A5) und bei Bedarf wieder abgerufen werden können.
* Die Eingabe der Bearbeitungsbreite (Abb. 4-A2), als die Breite, auf die sich die Datenaufnahme bei der Befahrung einer Fahrspur bezieht. Die Angabe erfolgt in Metern und ist erforderlich, um die Ergebnisdateien erzeugen zu können.
* Die Auswahl von bis zu neun Minderertragsursachen, die in der aktuellen Situation erkenn- und somit kartierbar sind (Abb. 4-A3). Die Anordnung der Ursachen auf den dafür zur Verfügung stehenden Buttons kann individuell festgelegt werden. Durch Antippen eines Buttons erscheint eine Auswahlliste (Abb. 4-B):
   * Soll der Button während der Kartierung nicht angezeigt werden, wählt man `Schaltfläche verstecken` aus (Abb. 4-B1). 
   * Soll der Button hingegen mit einer Ursache belegt werden, kann auf eine Liste vordefinierter Minderertragsursachen zurückgegriffen werden (Abb. 4-B2). 
   * Nicht aufgelistete Ursachen können ergänzt werden, indem `Neu erstellen` (Abb. 4-B3) angetippt und die Ursache (Abb. 4-C1) sowie zugehörige Schlüsselwörter für die Spracherkennung (Abb. 4-C2) in den sich nacheinander öffnenden Fenstern eingegeben werden.
* Die Festlegung der Anzahl von Zonen (Abb. 4-A4) gleicher Breite, in welche die halbe Bearbeitungsbreite (Abb. 4-A2) links und rechts der Fahrspur jeweils unterteilt werden soll. Die Seiten können in ein bis drei Zonen unterteilt werden.

![](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_fig04_de.svg)

_**Abb. 4:** Aufbau des (A) Menüs zur individuellen Konfiguration der Bedienoberfläche der FieldMApp-Fahrtansicht und des zugehörigen (B) Sub-Menüs zur Festlegung der Ursachen, die zur Ausbildung des zu erfassenden Problemstandortes geführt haben. Das Sub-Menü umfasst neben (B2), einer Auswahlliste, auch die Möglichkeit zur (B3, C) Eingabe weiterer Ursachen._
<br>

**Bedienoberfläche zur Datenaufnahme (Fahrtansicht)**

Die Bedienoberfläche zur Datenaufnahme kann nach Auswahl einer Konfiguration mit `AUSGEWÄHLTE KONFIGURATION BENUTZEN` geöffnet werden. Die Funktionen, welche die Bedienoberfläche zur Datenaufnahme (vgl. Abb. 5) bereithält, ermöglichen:

* die Auswahl von bis zu drei Zonen links (Abb. 5-A) und rechts (Abb. 5-B) der Fahrspur. Für eine einzelne Zone, oder mehrere Zonen gleichzeitig, kann:
   * der Anfang einer Minderertragsfläche durch Antippen der bzw. Wischen über die entsprechende(n) Zonennummer(n) bei A1 bzw. B1 (siehe Abb. 5) festgelegt werden,
   * das Tastenfeld zur Eingabe der Ertragsminderung und der Ursache durch Antippen der bzw. Wischen über die entsprechende(n) Zonennummer(n) bei A2 bzw. B2 (siehe Abb. 5) aktiviert werden,
   * das Ende einer Minderertragsfläche durch Antippen der bzw. Wischen über die entsprechende(n) Zonennummer(n) bei A3 bzw. B3 (siehe Abb. 5) festgelegt werden.

* die Erfassung der Intensität der (zu erwartenden) Ertragsminderung (Abb. 5-C) und
* die Erfassung der Ursache(n), welche die (zu erwartende) Ertragsminderung hervorrufen (Abb. 5-D).

![](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_fig05_de.svg)

_**Abb. 5:** Aufbau der Bedienoberfläche des Anwendungsfalls „Minderertragsflächenkartierung“: Die Hälften der Bearbeitungsbreite links und rechts der Fahrspur werden durch Bereiche A und B repräsentiert. Im dargestellten Beispiel sind beide Bereiche in jeweils drei Zonen (Zone 1-3 im Bereich A und Zone 4-6 im Bereich B) unterteilt. Durch Auswahl der Zonen können die Intensität (C) und die Ursachen (D) der (zu erwartenden) Ertragsminderung erfasst werden._



### Handhabung
**1. Anwendungsfall `Minderertragskartierung` im Menü der FieldMApp anwählen**


**2. Festlegen der Konfiguration der Benutzeroberfläche** (OPTIONAL)
<details><summary>2.1. Bereits vorhandene Konfiguration anpassen</summary>
 
* Auf der Startseite des Anwendungsfalls `Minderertragskartierung` den Namen einer vordefinierten Konfiguration (z.B. Standard) durch Antippen aus der Liste ausgewählen
* Durch Antippen des Buttons `KONFIGURATION ANPASSEN` wird die Konfigurationsansicht geöffnet (weiteres Vorgehen siehe 2.2 zweiter Spiegelstrich)
 
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
* Durch Antippen von `Speichern` wird die Konfiguration unter dem angegebenen Konfigurationsnamen gespeichert. 
 
{{% pageinfo %}}
Durch erneutes Ausführen einzelner Konfigurationsschritte können Korrekturen vorgenommen werden.
{{% /pageinfo %}}
</details><br>


**3. Konfiguration der Bedienoberfläche auswählen** 
<details><summary>3.1 Auswahl</summary>
 
* Die Auswahl erfolgt, indem der Name einer vordefinierten Konfiguration (z.B. Standard) durch Antippen aus der Liste ausgewählt und durch Berühren von `AUSGEWÄHLTE KONFIGURATION BENUTZEN` geöffnet wird.
</details><br>


**4. Datenaufnahme mit der Fahrtansicht** 

{{% pageinfo %}}
Buttons der Fahrtansicht, mit deren Hilfe in der aktuellen Situation Daten erhoben werden können, haben eine grüne Hintergrundfarbe. Mit Buttons ohne grünen Hintergrund können keine Daten erhoben werden. Die Hintergrundfarbe wechselt, je nachdem, welche Eingaben im Vorfeld erfolgt sind.
{{% /pageinfo %}}

<details><summary>4.1 Markieren des Anfangs einer Minderertragsfläche</summary>
 
* Der Anfang einer Minderertragsfläche in einer Zone oder mehreren Zonen wird durch Antippen oder Wischen über die betreffende(n) Nummer(n) der Zone(n) auf Höhe des Dreiecks mit dem Schriftzug „Start“ (Abb. 5-A1, 5-B1) festgelegt. Die Möglichkeit zur Eingabe von Eigenschaften zu dem zu kartierenden Objekt wird damit automatisch freigeschaltet.
</details>

<details><summary>4.2 Eingabe der Eigenschaften von Minderertragsflächen</summary>
 
* Durch Antippen der oder Wischen über die Nummer(n) der Zone(n) in der Mitte der Fahrtansicht (Abb. 5-A2, 5-B2) werden für diese die Eigenschaftsbuttons mit Zentrum der Fahrtansicht (Abb. 5-C, 5-D) aktiviert. Die adressierten Zonen werden durch einen gelben Hintergrund hervorgehoben.
* Durch Antippen eines aktivierten Eigenschaftsbuttons wird den adressierten Zonen die ausgewählte Eigenschaft zugewiesen. Der Hintergrund der adressierten Zone(n) erscheint auf Höhe der gewählten Eigenschaften daraufhin grün.
* Objekten können weitere Eigenschaften zugewiesen werden, indem die ersten beiden Schritte unter 4.2 wiederholt werden. Wurden alle Eigenschaften für das kartierte Objekt in einer Zone erfasst, erscheint der Hintergrund der gesamten Zone grün.
* Bereits erfasste Eigenschaften eines Objektes in einer Zone/mehreren Zonen können korrigiert werden, in dem die ersten beiden Schritte unter 4.2 wiederholt werden, solange noch nicht mit der Kartierung eines neuen Objektes in der/den betreffenden Zone(n) begonnen wurde.
</details>

<details><summary>4.3 Markieren des Endes einer Minderertragsfläche</summary>
 
* Das Ende einer Minderertragsfläche in einer Zone oder mehreren Zonen wird durch Antippen oder Wischen über die betreffende(n) Nummer(n) der Zone(n) auf Höhe des Dreiecks mit dem Schriftzug „Stop“ (Abb. 5-A3, 5-B3) festgelegt. 
</details>

<details><summary>4.4 Korrektur bei Falscheingaben</summary>
 
* Durch Antippen von `Abbrechen` werden für alle Zonen die Eingaben gelöscht, die bis zum letzten Start eines Objektes zurückreichen.
</details>
<br>

### Leitfaden zur bewährten Datenerfassung
* Für ein Feld sollte die Erfassung der Minderertragsflächen mehrmals unabhängig voneinander erfolgen. Auf diese Weise soll sichergestellt werden, dass

   * … alle potentiellen Minderertragsstandorte erfasst werden, auch wenn deren Ausprägung nur unter unterschiedlichen Witterungsbedingungen entsteht.
   * … die größtmögliche Ausdehnung der potentiellen Minderertragsfläche kartiert wird sowie die üblicherweise auftretende Varianz in der Ausdehnung.
   * … anhand der Analyse der Häufigkeitsverteilung einer erfassten Eigenschaft (wie z.B. der Minderertragsursache) eventuell erfolgte Fehlangaben ausgeschlossen werden können.<br>

* Sollte lokal eine exakte Erfassung der Problemstandorte während einer Befahrung nicht möglich sein, z.B. auf Grund einer hohen standörtlichen Heterogenität, empfehlen wir die Erfassung auf den Teil der Problemstandorte zu beschränken, die bei Erhalt der Qualität leistbar ist. Die verbleibenden Problemstandorte können bei späteren Befahrungen ergänzt werden.


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
Im Rahmen einer Untersuchung wurden 150 Minderertragsflächen von 5 verschiedenen Personen mit Hilfe des Tastenfelds der FieldMApp-Fahrtansicht erfasst (Stichprobenumfang N = 750). Das Fahrzeug, in dem sich die kartierenden Personen während der Datenerhebung befanden, wurde mit einer konstanten Geschwindigkeit von 15 km/h bewegt. Die Minderertragsflächen waren bei der Untersuchung so verteilt, dass ein sehr breites Spektrum von Eingabebefehlen abgedeckt wurde. Die Eingabebefehle reichten von 

* einer separiert in einer Zone liegenden Minderertragsfläche, über 
* direkt aneinander grenzende Minderertragsflächen unterschiedlicher Ursachen, die sich jeweils über mehrere Zonen erstreckten, bis hin zu 
* direkt aneinander grenzende Minderertragsflächen unterschiedlicher Ursachen, die sich jeweils über mehrere Zonen erstreckten und auf gleicher Höhe liegend links und rechts der Fahrspur unterschiedliche Ursachen aufwiesen.

Eine parallele Bedienung von anderen Steuerelementen am Fahrzeug erfolgte nicht. Unter diesen Gegebenheiten wurden folgende zu erwartenden minimalen Unsicherheiten bzw. maximalen Genauigkeiten abgeschätzt:

| Kenngröße | Abgeschätzter Wert               |
| --------- | --------------------------------:|
| Zu erwartende Ausfallrate an Angaben (bezogen auf N)                                                                           |    0,9% |
| Anteil korrekter Eingabebefehle (bezogen auf N)                                                                                |   96,1% |
| Anteil korrekt eingegebener Zonennummern (bezogen auf N)                                                                       |   98,7% |
| Anteil korrekt eingegebener Minderertragsursachen (bezogen auf N)                                                              |   96,5% |
| Median des richtungsabhängigen Versatzes zwischen dem Anfang der Minderertragsfläche und dem Start der Datenerfassung          |  +4.9 m |
| Mittelwert des richtungsabhängigen Versatzes zwischen dem Anfang der Minderertragsfläche und dem Start der Datenerfassung      |  +6,9 m |
| Standardabweichung als Streumaß für den Versatz zwischen dem Anfang der Minderertragsfläche und dem Start der Datenerfassung | 11,25 m |


## Hard- und Software-Ausstattung
### Rückgriff auf interne und externe Messgeräte
#### Liste erforderliche Sensoren
Interne Sensoren
| Sensorname     | Zweck                                                                | Ersetzbar                             | Nutzungsempfehlung |
| -------------- | -------------------------------------------------------------------- | ------------------------------------- | -------------------- |
| GPS            | Ermöglicht die Erfassung der Position bei der Eingabe der Daten. | Ja <br> (Alternative: externes dGNSS) | GPS wenig empfehlenswert |


#### Liste optional einsetzbarer Sensoren
Interne Sensoren
| Sensorname     | Zweck                                                                                                   | Nutzungsempfehlung  |
| -------------- | ------------------------------------------------------------------------------------------------------- | ------------------- |
| Mikrophon      | Ermöglicht die Nutzung der Spracherkennung und damit <br>die Steuerung der Anwendung mittels Sprachbefehlen | sehr empfehlenswert |


Externe Sensoren
| Sensorname     | Zweck           | Nutzungsempfehlung |
| -------------- | --------------- | ------------------ |
| Differentielles Global Navigation Satellite System ([dGNSS](https://fieldmapp.github.io/docs/useroverview/sensors/external/dgnss/)) | Ermöglicht die zentimetergenaue Erfassung der Position bei der Dateneingabe. Aufgrund der höheren Präzision des dGNSS-Sensors im Vergleich zum geräteinternen GPS-Sensor kann durch dessen Nutzung zu einer Verringerung des Gesamtfehlers bei der Datenaufnahme beigetragen werden. |sehr empfehlenswert |


### Veröffentlichte Software-Versionen
| Versionsnummer | Letzte Änderung | Downloadlink Anwendungsfall                    | Was wurde gegenüber vorheriger Version geändert |
| -------------- | --------------- | ---------------------------------------------- | ----------------------------------------------- |
| 1.0            | 30.01.2023      | [Link zu Version 0.1](https://www.example.org) | Wiki-Beitrag ergänzt                            |
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
Truckenbrodt, S.C., M. Enderling, E. Borg & F. Klan (2022): FieldMApp Nutzerübersicht. Anwendungsfall Minderertragsflächenkartierung. &lt;https://fieldmapp.github.io/docs/useroverview/usecases/list/lowyieldareamapping/&gt; (Stand: 2023-01-31) (Zugriff: YYYY-MM-DD).

