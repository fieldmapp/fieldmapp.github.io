---
title: "Anwendungsgebiete für die FieldMApp"
weight: 3
description: >-
     Übersicht der FieldMApp Anwendungsgebiete.
---

{{% pageinfo %}}
Die Dokumentation ist noch im Aufbau.
{{% /pageinfo %}}

## **Anwendungsfall:** Datenbasierte Entscheidungsunterstützung 
### Minderertragsflächen mit historischen Wetter- und Fernerkundungsprodukten abgleichen

Dieser Anwendungsfall zeigt die Integration verschiedener Datenprodukte im [Map-Module](../../02_components/02_map.md), sowie im [Reporting-Module](../../02_components/06_extensions/reporting) der FieldMApp. Diese Integration ermöglicht eine fundierte, datenbasierte Entscheidungsunterstützung direkt innerhalb der App – beispielsweise durch die Analyse von Temperatur- und Niederschlagsverläufen während der Vegetationsperiode oder durch einen Überblick über die Entwicklung der Pflanzenvitalität zur Bewertung bereits durchgeführter Maßnahmen.

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/use_case1.mp4" type="video/mp4">
</video>

> **Verwendete Layer**
> - `Alt-Tellin` mit dem [Feldaufnahme-Module](../../02_components/03_recording/) aufgenommene Minderertragsflächen
> - `Sentinel 2 EVI` Rasterdatenzeitreihe des Ehanced vegetation index auf Basis von Sentinel 2 Aufnahmen
> - `DWD Bodenfeuchtekarte` [Rasterdatenzeitreihe](https://www.dwd.de/DE/fachnutzer/landwirtschaft/appl/bf_view/_node.html) (täglich) der Bodenfeuchte, bereitgestellt durch den deutschen Wetterdienst
> - `OSM` OpenStreetMap basierte Hintergrundkarte

> **Verwendete Erweiterung**  
> -  [**Reporting**](../../02_components/06_extensions/reporting) Kartenerweiterung für monatliche Reports mit Wetter und Fernerkundungsparametern 

## **Anwendungsfall:** Minderertragsfläche aufnehmen und bearbeiten

Dieser Anwendungsfall zeigt, wie sich mit der FieldMApp Minderertragsflächen auf einem Feld schnell und präzise erfassen lassen. Die kartierten Flächen können direkt in der App bearbeitet und anschließend exportiert werden – etwa für die Weiterverarbeitung in QGIS. So fügt sich die App nahtlos in bestehende Datenanalyse-Workflows ein und beschleunigt die Feldauswertung.

