
---
title: "Module - Projekte: Projektmanager"
weight: 100
description: >-
     Informationen zur Nutzung der Projekte und den damit gewonnen Daten.
---

## Übersicht

TODO: Was kann das Modul leisten? Welche Daten werden gewonnen? Was ist dazu notwendig?

## Projekt-Format

Projekt-Dateien sind ein ZIP-Archiv und enthalten eine `Project.json`-Datei und mehrere `.odkbuild`-Dateien.

Jede `.odkbuild`-Datei wird in der App in eine Fragebogenseite übersetzt. Dort werden diese alphabetisch angeordnet. Z.B. erscheinen Seiten die mit `a` beginnen vor Seiten die mit `b` beginnen. Deswegen wird empfohlen die Dateinamen mit einer Zahl zu beginnen: `01ErsteSeite.odbuild`, `02ZweiteSeite.odkbuild` ...

Die `Project.json` folgt dem folgenden Muster:

```
{
  "Project": {
    "0": "Projektname auf Deutsch",
    "1": "Project in English"
  },
  "Author": {
    "0": "Autor-Bezeichnung auf Deutsch",
    "1": "Author in English"
  },
  "Description": {
    "0": "Beschreibung auf Deutsch",
    "1": "Description in English"
  },
  "Secret": null,
  "Languages": {
    "0": "German",
    "1": "English"
  },
  "ProfilingId": "uniqueProfilingId"
}
```

`"Project"`, `"Author"`, `"Description"` und `"Languages"` sind Listen, bei denen der jeweils der gleiche Index für die selbe Sprache steht. Diese wird in `"Languages"` festgelegt.  `"ProfilingId"` identifiziert das für dieses Projekt notwendige Profiling (siehe [Profiling](Modules/Profiling)).


## Unterstützte Teile des ODK-Standards

### Algemeine Felder

Sprachen werden unterstützt, jedoch muss die `"Languages"`-Liste in jeder `.odkbuild`-Datei genau der in der  `Projects.json`-Datei entsprechen.

| Feldname | Unterstützung |
| ------ | ------ |
| Data Name | :heavy_check_mark: |
| Label | :heavy_check_mark: |
| Hints | :heavy_check_mark: (komplett) In der App abrufbar über "Hinweis"-Knopf |
| Default Value | :x: |
| Read Only | :x: |
| Required | :heavy_check_mark: |
| Invalid Text | :x: |
| Show question if | :heavy_check_mark: (Einschränkungen siehe "Formeln" weiter unten) |
| Constraint | :question: (Darf keine Referenzen auf andere Elemente, sondern nur auf sich selbst via der "."-Notation haben. Weitere einschränkungen siehe "Formeln" weiter unten) |
| Constraint Invalid Text | :x: |
| Calculate | :x: |

### Text-Felder

| Feldname | Unterstützung |
| ------ | ------ |
| Length | :heavy_check_mark: (komplett) |

### Numeric-Felder

| Feldname | Unterstützung |
| ------ | ------ |
| Valid Range | :heavy_check_mark: (komplett) |
| Style | :x: |
| Kind | :x: |

### Date/Time-Felder

| Feldname | Unterstützung |
| ------ | ------ |
| Range | :heavy_check_mark: (komplett) |
| Kind | :question: Nur "Full Date" und "Full Date and Time" |


### Time-Felder 

:x: (Time-Element wird nicht unterstützt)

### Location-Felder

| Feldname | Unterstützung |
| ------ | ------ |
| Kind | :x: |
| Style | :x: |

### Media-Felder

Hierzu wird in der App die Kamera geöffnet, damit man ein neues Foto machen kann.

| Feldname | Unterstützung |
| ------ | ------ |
| Kind | :x: |

### Barcode-Felder

:x: (Barcode-Element wird nicht unterstützt)

### Choose One-Felder

| Feldname | Unterstützung |
| ------ | ------ |
| Options | :question: ("Underlying Value" muss dem 0-basierten Listen-Index entsprechen. Muss also bei 0 starten und immer um 1 erhöht werden) |
| Cascading | :x: |
| Follow-up Question | :x: |
| Style | :x: |

### Select Multiple-Felder

:x: (Select Multiple-Element wird nicht unterstützt)

### Metadata-Felder

:x: (Metadata-Element wird nicht unterstützt)

### Metadata-Felder

:x: (Metadata-Element wird nicht unterstützt)

### Group-Felder

:x: (Group-Element wird nicht unterstützt)

## Formeln

Siehe [ODK Dokumentation zu Formeln](https://docs.getodk.org/form-logic/). Wir nutzen NCalc um Formeln auszuwerten. Nach jeder Änderung werden alle unterstützten Formelfelder ("Constraint" und "Show question if") neu berechnet. 

Unterstützte Formelelemente (siehe "OdkBooleanExpresion" Klasse):
- Zahlen
- div und mod
- true, false und logische Verknüpfungen in Wortform ("and") und Symbolform ("&&")
- sin, cos, tan
- asin, acos, atan
- abs
- log, log10
- sqrt
- round und int
- pow, exp und exp10
- boolean-from-string
- random
- pi
- now

## Erweiterungen

Über die von ODK definierten Elemente unterstützen wir weitere Elemente an. Um diese zu nutzen muss man ein Text-Element zum Formular hinzufügen und in den ODK-Namen (`"Label"`) jeder Sprache den Elemententyp schreiben. Beispiel siehe "Kompass".

### Kompass

Elementyp: `compass`

Beispiel-Label-Eintrag: `"Ausrichtung der Pflanzenreihen{compass}"`. Der angezeigte Elementenname enthält `{compass}` dann nicht.

Wert wird als Zahl zwischen 0 und 360 angezeigt und gespeichert.

## Existierende Projekte

| Projekt | Projektdatei-Download |
| ------ | ------ |
| FieldCampagne | [FieldCampagneProject.zip](uploads/45e465e26cdb2df3fd835d2c258ac982/FieldCampagneProject.zip) (Stand: 09.03.2021) |