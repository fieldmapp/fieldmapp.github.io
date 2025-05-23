---
title: "Map-Erweiterung: Reporting"
weight: 100
description: >-
     Reporting der FieldMApp
     .
---

{{% pageinfo %}}
Die Dokumentation ist noch im Aufbau.
{{% /pageinfo %}}


## Felddaten Reporting


> Das Reporting-Modul befindet sich aktuell in der prototypischen Entwicklung. Ziel ist es, für registrierte landwirtschaftliche Flächen regelmäßige Berichte bereitzustellen, um datenbasierte, fundierte Entscheidungen zur Bewirtschaftung treffen zu können. Es kombiniert **Wetterdaten** und **Fernerkundungsprodukte** in einem kompakten Überblick und schafft damit die Grundlage für **datengetriebene Entscheidungsprozesse in der Landwirtschaft**.

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/fm-reporting.mp4" type="video/mp4">
</video>

### Funktionen im Überblick

##### 1. Auswahl registrierter Flächen
- Auf der Startseite des Moduls erscheinen alle registrierten Flächen (z. B. Felder, Schläge).
- Wähle eine Fläche durch Antippen aus der Liste aus.

##### 2. Ansehen des aktuellen Berichts
- Ein aktueller Bericht enthält zeitlich aufbereitete Daten zu:
  - 🌡️ **Wetterdaten**:
    - Temperaturverlauf (Tagesmittel)
    -  tägliche Niederschlagsmenge (in mm)
  - 🌿 **Fernerkundungsdaten**:
    - **NDVI** (Normalized Difference Vegetation Index): Gibt Auskunft über die Vitalität der Vegetation.
    - **Vitalitätsdifferenz**: Zeigt die Veränderung im Vegetationszustand im Vergleich zu einer Vorperiode.

##### 3. Interpretation der Daten
- Die **Wetterdaten** helfen dabei, Stressfaktoren wie Hitze oder Trockenperioden zu erkennen.
- Die **Fernerkundungsdaten** unterstützen bei der Einschätzung des Pflanzenwachstums, etwa bei Verzögerung der Entwicklung oder möglichem Schädlings-/Krankheitsdruck.
    
<br>

>##### Hinweise zur Nutzung
> - Aktuell ist das Modul im Testbetrieb – Berichte werden ggf. nicht regelmäßig automatisch erstellt.
> - Die angezeigten Werte basieren auf öffentlich zugänglichen Wetterdaten (DWD) und Satellitenbildern (Sentinel-2).
> - Umfang und Parameter im Bericht werden zukünftig konfigurierbar sein
