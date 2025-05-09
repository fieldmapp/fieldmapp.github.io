---
title: "Map"
weight: 2
description: >-
     Die Karten und GIS Funktionalitäten der FieldMApp.
---

{{% pageinfo %}}
Die Dokumentation is  t noch im Aufbau.
{{% /pageinfo %}}

> Das Map-Modul ist die geografische Informationssystem (GIS)-Komponente der FieldMApp und bietet leistungsstarke Werkzeuge zur Visualisierung, Bearbeitung und Erstellung räumlicher Daten im Feld. Mit einer intuitiven, für mobile Geräte optimierten Benutzeroberfläche ermöglicht dieses Modul Anwendern, mit verschiedenen Geodatenformaten zu arbeiten, ihre Position zu verfolgen und räumliche Analyseaufgaben direkt auf ihrem mobilen Gerät durchzuführen.

> **Hauptfunktionen**
> - [Multi-Layer-Visualisierung](#geodaten-visualiseren) - Darstellung verschiedener Datenformate wie Tile-Layer (OSM), Webdienste (WMS) und Vektordaten (GeoJSON)
> - [Interaktive Bearbeitungswerkzeuge](#geodaten-bearbeiten) - Erstellung und Modifikation räumlicher Features mittels einfacher Berührungsgesten
> - [Echtzeit-Positionsverfolgung](#positionanzeigen-und--folgen) - Anzeige des aktuellen Standorts mit Genauigkeitsinformationen und automatischer Bewegungsverfolgung
> - [Ortssuche](#ortssuche) - Finden von Orten und Adressen über OpenStreetMap-basierte Suchfunktionalität
> - [Zeitgesteuerte Layer](#3-niederschlagsradar-hinzufügen-dwd-wms) - Arbeit mit zeitlichen Daten wie Wetterradar mit intuitiver Zeitsteuerung

> Ob Sie Felddaten sammeln, in unbekanntem Gelände navigieren oder räumliche Muster vor Ort analysieren – das Map-Modul bietet alle wesentlichen GIS-Funktionen, optimiert für die mobile Feldarbeit.

> **Map-Erweiterungen:**
> - [**Reporting**](../06_extensions/reporting) Kartenerweiterung für monatliche Reports mit Wetter und Fernerkundungsparametern 

## Geodaten visualiseren

Dieses Tutorial zeigt, wie Geodaten in das GIS-Modul der mobilen Anwendung geladen und visualisiert werden können. Im Beispiel werden drei Layer eingebunden:

- OpenStreetMap (OSM) – als Hintergrundkarte zur Orientierung.
- DWD-Niederschlagsradar (WMS) – aktuelle Wetterdaten mit Zeitsteuerung.
- Elbeeinzugsgebiet (GeoJSON) – thematischer Vektorlayer mit Metadaten.

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/fm_gis_module.mp4" type="video/mp4">
</video>


#### **Schritt-für-Schritt-Anleitung**

##### 1. Start des GIS-Moduls
- Öffne die App und navigiere zum GIS-Modul > Navigationsleiste *Karte*.
- Du siehst eine leere Karte mit Werkzeugleiste.

##### 2. Hintergrundkarte laden: OpenStreetMap (Tilelayer)
- Tippe auf das **Layer hinzufügen** (Symbol: Stapel).
- Wähle aus der Liste **OpenStreetMap**.
- Die Hintergrundkarte erscheint zur besseren räumlichen Orientierung.

##### 3. Niederschlagsradar hinzufügen (DWD, WMS)
- Erneut das **Layer hinzufügen** öffnen.
- Wähle aus der Liste **DWD Niederschlagsradar**.
- Im Menü des Layers erscheint die Option für **Zeitsteuerung**, mit dem du verschiedene Zeitpunkte auswählen kannst.

##### 4. GeoJSON laden: Elbeeinzugsgebiet
- Erneut das **Layer hinzufügen** öffnen.
- Wähle aus der Liste  `elbe_basin.geojson`
- Die Geometrien werden dargestellt
- Durch Antippen einzelner Flächen erhältst du die zugehörigen Metadaten (z. B. Name, Fläche, ID).

##### 5. Interaktive Funktionen nutzen
- Zoomen, Verschieben, Layer-Reihenfolge ändern.
- Informationen zu Layern anzeigen lassen.
- Layer (de)aktivieren über die Sidebar.


<hr>

## Geodaten bearbeiten

Dieses Tutorial zeigt die Bearbeitung eines Vektordatensatzes, hierfür Laden wir den `elbe_basin.geojson` Datensatz und bearbeiten diesen Mithilfe des OpenStreetMap Hintergrund-Layers.

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/fm_gis_module_edt.mp4" type="video/mp4">
</video>


#### **Schritt-für-Schritt-Anleitung**

##### 1. Laden des GeoJSON-Datensatzes und des Hintergrundlayers
-  siehe Anleitung [*Geodaten visualiseren*](#4-geojson-laden-elbeeinzugsgebiet)

##### 2. Bearbeitungsmodus starten
- Tippe auf das Feature (z. B. Polygon), das du bearbeiten möchtest, um es **zu selektieren**.
- **Halte das selektierte Feature gedrückt (Long Press)**, um den Bearbeitungsmodus zu starten.
- Die Geometrie wird jetzt editierbar (z. B. Eckpunkte verschieben).

##### 3. Änderungen vornehmen
- Verschiebe Eckpunkte oder forme die Geometrie wie gewünscht um.
- Bestätige die Änderungen durch einen Klick auf **„Speichern“** oder das entsprechende Symbol in der Werkzeugleiste (rechts)


<hr>

## Neue Geodaten erstellen

Dieses Tutorial zeigt das Hinzufügen eines Features zu einem existierenden Vektordatensatz, hierfür Laden wir den `elbe_basin.geojson` Datensatz und erstellen eine neue Polyline.


<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/fm_gis_new_feature.mp4" type="video/mp4">
</video>


#### **Schritt-für-Schritt-Anleitung**

##### 1. Laden des GeoJSON-Datensatzes und des Hintergrundlayers
-  siehe Anleitung [*Geodaten visualiseren*](#4-geojson-laden-elbeeinzugsgebiet)

##### 2. Bearbeitungsmodus starten
- gewünschte Geometrieart in der Werkzeugleiste (rechts) auswählen mögliche Wahl zwischen Polyline, Polygon oder Punkt

##### 3. Änderungen vornehmen
- Verschiebe Eckpunkte oder forme die Geometrie wie gewünscht um.
- Bestätige die Änderungen durch einen Klick auf **„Speichern“** oder das entsprechende Symbol in der Werkzeugleiste (rechts)
- gewünschten Layer in welchem das neue Feature gespeichert werden soll auswählen


<hr>

## Positionanzeigen und -folgen

In dieser Anleitung zeigen wir, wie du deine aktuelle GPS-Position im GIS-Modul anzeigen und der Bewegung automatisch folgen lassen kannst. Dies ist besonders hilfreich bei Navigation, Geländeaufnahmen oder Außeneinsätzen.


<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/gis_follow_pos.mp4" type="video/mp4">
</video>

#### **Schritt-für-Schritt-Anleitung**


##### 1. Anzeige der aktuellen Position aktivieren
- Tippe auf das **GNSS-Symbol** (Fadenkreuz mit Punkt) in der Kartenansicht.
- Deine aktuelle Position wird auf der Karte als blauer Pfeil angezeigt.
- Der aktuelle GNSS-Genauigkeit wird in der Info-Box unterhalb des Buttons dargestellt und als Fehlerkreis in der Karte

##### 2. Follow-Me-Modus aktivieren
- Tippe auf das GNSS-Symbol, um den **Follow-Me-Modus** zu aktivieren.
- Die Karte zentriert sich automatisch auf deine Position und folgt deinen Bewegungen.

> 🔁 Der Modus bleibt aktiv, bis du den GNSS-Fokus deaktivierst.

##### 3. Follow-Me-Modus aktivieren
- Tippe auf das GPS-Verlauf-Symbol (Kreissymbol) um die Ansicht der letzten 100 GNSS Positionen darzustellen.

##### 4. GPS deaktivieren (optional)
- Durch weiteres Tippen auf das GPS-Symbol kannst du den Follow-Me-Modus beenden.
- Die Karte bleibt dann an der letzten Position stehen.


<hr>

## Ortssuche

In diesem Beispiel wird die OSM basierte Ortssuche gezeigt.

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/gis_search.mp4" type="video/mp4">
</video>


#### **Schritt-für-Schritt-Anleitung**

##### 1. Zugriff auf das Suchfeld
- Tippe auf das **Suchsymbol** 🔍 oder das Eingabefeld am oberen Bildschirmrand.
- Das Suchfeld öffnet sich und wartet auf deine Eingabe.

##### 2. Ort oder Adresse eingeben
- Gib den gesuchten Begriff ein, z. B.:
  - `Jena`
  - `München, Marienplatz`
  - `Jena DLR`
- Während der Eingabe werden **Vorschläge basierend auf OpenStreetMap-Daten** angezeigt.

##### 3. Treffer auswählen
- Wähle den passenden Eintrag aus der Liste.
- Die Karte zoomt automatisch zum entsprechenden Ort.
- Ein Marker kennzeichnet die Zielposition.
