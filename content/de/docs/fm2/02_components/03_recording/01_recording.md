---
title: "Eine Minderertragsfläche kartieren"
weight: 1
description: >-
     Benutzerdokumentation für das Kartieren von Minderertragsflächen.
---

- Es sollen digitale Karten von Minderertragsflächen und deren Ursachen erstellt werden
- Ich fahre über das Feld und markiere Beginn und Ende von Minderertragsflächen links und rechts meiner Fahrspur
- Ich gebe Ursache und Stärke der Minderertragsfläche an
- Ich kann die gesammelten Daten exportieren

> **Hinweis**  
> Für eine verbesserte Genauigkeit, ist es empfohlen einen [externen GNSS-Empfänger mit DGPS zu verwenden]({{< ref "docs/fm2/02_components/05_sensors/02_external.md" >}}). Für mehr Informationen zur erzielbaren Genauigkeit: [Unsicherheits- und Genauigkeitsangaben]({{< ref "docs/fm2/02_components/03_recording/03_recording_accuracy.md" >}})

## Das Minderertragsflächenmodul in der FieldMApp auswählen
Durch einen Klick auf den Button `Neue Aufnahme starten!` kann eine neue Feldaufnahme gestartet werden.

## Die Aufnahmeoptionen anpassen
### Neue Feldaufnahme
#### Name der Aufnahme
Name der Feldaufnahme unter der die vorgenommenen Einstellungen sowie die spätere Aufnahme gespeichert werden und bei Bedarf wieder abgerufen werden können.
#### Autor
Name der kartierenden Person.
#### Gesamtbreite (m)
Eingabe der gesamten Bearbeitungsbreite in Metern.
#### Anzahl der Zonen (einseitig)
Die Arbeitsbreite links und rechts der Fahrspur wird in gleich große Zonen unterteilt, um eine strukturierte Kartierung zu ermöglichen. Dabei kann jede Seite in 1 bis 5 Zonen aufgeteilt werden. Die Anzahl der Zonen bestimmt die Breite der einzelnen Streifen. Zum Beispiel ergibt eine Gesamtbreite von 30 m bei 3 Zonen pro Seite insgesamt 6 Streifen mit einer Breite von jeweils 5 m.

#### Abstand zur Aufnahme
Distanz zwischen Fahrer und GNSS-Antenne in Metern.
- Positive Zahl: Die Antenne ist vor dem Fahrer???
- Negative Zahl: Die Antenne ist hinter dem Fahrer.

![Optionen](/graphs/arbeitsbreite.jpg)
Foto: Maximilian Enderling, Bearbeitung: Tim Surber *Diese Grafik zeigt die Bedeutung der Option `Gesamtbreite`, einen positiven `Abstand zur Aufnahme` und eine `Anzahl der Zonen(einseitig)` von zwei*

#### Auswahl von Minderertragsursachen
Es kann eine voreingestellte Auswahl an Minderertragsursachen ausgewählt werden, oder eine neue Liste erstellt werden. Durch einen Klick auf das „+“ kann ein Name für die Sammlung von Gründen vergeben werden und die Gründe (durch Kommas getrennt) eingetragen werden.  

### Abschließen der Aufnahmeoptioneneingabe
Um die Eingaben zu bestätigen, muss das Speicherysmbol in der unteren rechten Ecke angeklickt werden. Dies startet die Feldaufnahme. Mit einem Klick auf das Symbol mit dem Kreuz hingegen wird das Erstellen einer neuen Feldaufnahme abgebrochen.

### Vorhandene Feldaufnahme als Vorlage verwenden
Bei einer wiederholten Kartierung kann Zeit gespart werden, in dem auf der rechten Seite eine zuvor erstellte Feldaufnahme als Vorlage verwendet wird. Es werden die Aufnahmeoptionen der Vorlage übernommen in die Optionsfelder übernommen.  In der Konfigurationsansicht erscheinen die Eingaben der vorherigen Feldaufnahme, wobei der Name der Feldaufnahme neu vergeben werden muss.

## Während der Aufnahme
Minderertragsflächen werden durch eine oder mehrere Zonen begrenzt. Zonen unterteilen die Breite der Fahrspur. Einer Zone muss ein Grund mit zugehöriger Intensität zugewiesen werden.

> **Hinweis**  
> Beachten Sie auch den [Leitfaden zur bewährten Datenerfassung]({{< ref "docs/fm2/02_components/03_recording/02_recording_tips.md" >}})


### Beginn von Minderertragsflächen
Der Anfang einer Minderertragsfläche in einer Zone oder mehreren Zonen wird durch nach unten Wischen über die betreffende(n) Nummer(n) der Zone(n) festgelegt (Abb. 5). Die Möglichkeit zur Eingabe des Grundes und verbundenen Intensität wird damit automatisch freigeschaltet (Abb. 6). Aktivierte Zonen sind in einer hellgrünen Farbe hinterlegt.

### Eigenschaften der Minderertragsflächen
#### Grund
Durch klicken auf die entsprechende Ursache und Schweregrad können diese Informationen der zuletzt aktivierten Zone, welche in einem helleren grün hinterlegt ist, hinzugefügt werden. Nach erfolgreicher Eingabe erscheint eine schwarze Umrandung des zuletzt hinzugefügten Grundes, sowie ein schwarzer Haken beim entsprechenden Schweregrad

> **Hinweis**  
> Alternativ können Grund und Intensität auch zu allen weiteren aktiven oder nicht aktivierten Zonen per Drag and Drop gezogen werden. 


#### Intensität
Für jeden Grund stehen drei Intensitäten zur Verfügung. Der sandige Farbton bedeutet geringe Intensität, der orange Farbton mittlere Intensität und der rote Farbton hohe Intensität.

### Ende von Minderertragsflächen
Das Ende einer Minderertragsfläche wird durch ein Hochwischen über die entsprechende Zonennummer oder durch ein Doppeltipp auf die entsprechende Zonennummer erreicht.

> **Hinweis**  
> Der Beginn und das Ende der Zone sollte möglichst genau in dem Moment markiert wrden, in dem der Fahrer die Begrenzungen der Minderertragsfläche überfährt.

### Darstellungsoptionen
Durch klicken auf den Button mit dem Kartensymbol in der rechten oder linken Ecke eine Karte angezeigt werden, welche die aktuelle Position und die bereits erfassten Flächen anzeigt. Die Größe der Karte kann durch bewegen des Anfassers angepasst.

> **Hinweis**  
> Durch Verändern der Position und Größe kann die Aufnahme für eine optimierte Einhandbedienung des Tablets angepasst werden.


## Beenden der Feldaufnahme

### Speichern
Ein Tippen auf den Speicherbutton unten links beendet und speichert die Aufnahme.
### Verwerfen
Das rote Kreuz neben dem Speicherbutton dient zum Abbrechen und Löschen der Aufnahme. In diesem Fall wird kein Ergebnis erstellt, und alle aufgenommenen potenziellen Minderertragsflächen werden nicht verworfen.

{{% pageinfo %}}
Die Dokumentation ist noch im Aufbau.
{{% /pageinfo %}}
