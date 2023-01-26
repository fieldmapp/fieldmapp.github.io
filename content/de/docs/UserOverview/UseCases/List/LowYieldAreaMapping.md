---
title: "Nutzerübersicht - Minderertragsflächenkartierung"
linkTitle: "Minderertragsflächenkartierung"
weight: 100
---

# Ziel
Landwirten soll eine weitgehend automatisierte Erzeugung digitaler Minderertragskarten (Shapefiles) zu ihren Anbauflächen ermöglicht werden sowie eine automatisierte Bereitstellung von Handlungsempfehlungen zu deren Bewirtschaftung. Zur Erreichung dieser Ziele werden aus Satellitenbildern und meteorologischen Daten automatisch Informationen extrahiert (wie z.B. die Größe von Minderertragsarealen und der Niederschlags- und Temperaturverlauf) und mit dem Wissen von Landwirten um örtliche Gegebenheiten (wie etwa die Ursache für den Minderertrag) verknüpft. Der hier beschriebene Anwendungsfall ermöglicht es, die dafür vom Landwirt benötigten Informationen zu Eigenschaften von Minderertragsarealen auf pflanzenbaulich genutzten Flächen digital zu erfassen. Damit dem Landwirt für die Erfassung der Informationen kein zusätzlicher Zeitaufwand entsteht, wird diese von der Landmaschine aus, während der Bewirtschaftung der zu kartierenden Felder, vorgenommen (vgl. Abb. 1).

![](/screenshots/fig/UseCases/LowYieldAreas/LowYieldAreaMapping_fig01.jpg)

_**Abb. 1:** Zonenweise Erfassung ausgewählter Eigenschaften von Minderertragsarealen währen der Bewirtschaftung von pflanzenbaulich genutzten Flächen. (Photo: M. Enderling, Bearbeitung: S.C. Truckenbrodt)_

# Adressierte Nutzergruppe

* Landwirtinnen und Landwirte
* Fahrerinnen und Fahrer von Landmaschinen (z.B. Schlepper, Traktoren, selbstfahrende Spritze, Mähdrescher, Kartoffelvollernter)

# Einsatzort

* Pflanzenbaulich genutzte Flächen (z.B. Acker, Schlag)

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

**2. _OPTIONAL:_ Festlegen der Konfiguration der Benutzeroberfläche** <details><summary>[Mehr ...]</summary>
 
(A)	Bereits vorhandene Konfiguration anpassen
  i.	auf der Startseite des Anwendungsfalls `Minderertragskartierung` den Namen einer vordefinierten Konfiguration (z.B. Standard) durch Antippen aus der Liste ausgewählt 
  ii.	den Button `KONFIGURATION ANPASSEN` antippen, sodass die Konfigurationsansicht geöffnet wird (weiteres Vorgehen siehe 2-b-ii)
  
{{< alert title="Hinweis" >}}Durch das Anpassen einer Konfiguration wird die gespeicherte Ausgangskonfiguration überschrieben, auch wenn diese einen neuen Konfigurationsnamen erhält.{{< /alert >}}

(B)	Neue Konfiguration erstellen
  i.	Den Button `NEUE KONFIGURATION ERSTELLEN` antippen, sodass die Konfigurationsansicht geöffnet wird.
  ii.	Anpassung des Konfigurationsnamens
      In die Zeile hinter „Konfigurationsname“ tippen und mit dem sich öffnenden Tastenfeld den Namen eintragen, unter dem die Konfiguration gespeichert werden soll.
  iii.	Festlegen der Bearbeitungsbreite
        In die Zeile hinter „Bearbeitungsbreite (in Metern)“ tippen und mit dem sich öffnenden Ziffernblock die Bearbeitungsbreite in Metern eingeben, für welche die Kartierung erfolgen soll.
  iv.	Festlegen der kartierbaren Minderertragsursachen
      Nacheinander jedes der zur Verfügung stehenden Felder unter „Auswahl Minderertragsursache“ Antippen und festlegen, ob dieses zu einem Button mit einer Minderertragsursache werden soll. 
    1. _Falls ja:_ Aus der erscheinenden Liste (Abb. 2-B) eine Minderertragsursache (Abb. 2-B2) durch Antippen auswählen oder durch Antippen von `Neu erstellen` (Abb. 2-B3), das Fenster öffnen, über das eine neue, die Liste ergänzende Ursache eingeben und durch Tippen auf `OK` hinzugefügt werden kann (Abb. 2-C).
    2.	_Falls nein:_ Aus der erscheinenden Liste `Schaltfläche verstecken` durch Antippen auswählen.
  v.	Festlegen der Zonenanzahl
      Unter „Anzahl der Zonen“ kann die Anzahl der Zonen, welche symmetrisch jeweils auf die halbe Bearbeitungsbreite rechts bzw. links der Fahrspur verteilt werden soll, durch den Schieberegler festgelegt werden.
  vi.	Durch Antippen von `Speichern` wird die Konfiguration unter dem angegebene Konfigurationsnamen gespeichert.
{{< alert title="Hinweis" >}}Durch erneutes Ausführen einzelner Konfigurationsschritte können Korrekturen vorgenommen werden.{{< /alert >}}</summary>

**2. Konfiguration der Bedienoberfläche auswählen** <details><summary>[Mehr ...]</summary>
(C)	...indem der Name einer vordefinierten Konfiguration (z.B. Standard) durch Antippen aus der Liste ausgewählt und durch berühren des Buttons „AUSGEWÄHLTE KONFIGURATION BENUTZEN“ geöffnet wird.</details>


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

# Autoren Wiki

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Entwickler Code

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Zitationsvorschlag

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.

# Lizenz

Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
