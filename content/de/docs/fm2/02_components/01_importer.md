---
title: "Importer"
weight: 1
description: >-
     Importieren von externen Vektor- und Rasterdaten.
---

{{% pageinfo %}}
Die Dokumentation ist noch im Aufbau.
{{% /pageinfo %}}


> Das Import-Modul ermöglicht den Import von Vektor- und Rasterdaten in die FieldMApp. Einmal importiert, stehen die Daten allen Modulen der FieldMApp zur weiteren Verarbeitung zur Verfügung – zum Beispiel der [Karte](../02_map) zur Visualisierung und Bearbeitung.

## Datentypen

> Derzeit unterstützt das Import-Modul den Import von Vektordaten im Format `GeoJSON` im Koordinatensystem WGS84. Außerdem können Rasterdaten über OGC-konforme WMS- und Tile-Services eingebunden werden. Weitere Formate sind für zukünftige Versionen geplant.


### GeoJSON Importieren

Dieses Tutorial zeigt, wie eine externe `GeoJSON`-Datei (`elbe_basin.geojson`) in die FieldMApp importiert und im Karten-Module visualisiert wird. 

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/add_geojson.mp4" type="video/mp4">
</video>

#### **Schritt-für-Schritt-Anleitung**

##### 1. GeoJSON-Datei auswählen
Tippe auf die Schaltfläche **+** (rechts unten). Es öffnet sich ein Auswahlfenster, hier **Geojson** auswählen. Im Dateiexplorer  zur gewünschten `.geojson`-Datei navigieren und auswählen.

##### 2. Datei wird importiert
Nach der Auswahl wird die Datei automatisch in die Anwendung geladen und steht den Modulen der FieldMApp zur Verfügung.

##### 3. Karte öffnen und Layer prüfen
Wechsle zum Modul [**„Karte“**](../02_map#geodaten-visualiseren), um den importierten Layer zu visualisieren. Er sollte nun als eigenständiger Layer erscheinen und kann dort angezeigt, bearbeitet oder analysiert werden. 

<hr>

### WMS Dienst einbinden

Dieses Tutorial zeigt, wie ein externe [WMS-Dienst](https://gdz.bkg.bund.de/index.php/default/wms-basemapde-schummerung-wms-basemapde-schummerung.html) in die FieldMApp importiert und im Karten-Module visualisiert wird. 
 

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/add_wms.mp4" type="video/mp4">
</video>

#### **Schritt-für-Schritt-Anleitung**

##### 1. WMS als Quelle wählen
Tippe auf die Schaltfläche **+** (rechts unten). Es öffnet sich ein Auswahlfenster, hier **WMS/WMTS/XYZ** auswählen. 

##### 2. WMS-URL einfügen
Gib die URL des gewünschten WMS-Dienstes in das dafür vorgesehene Feld ein. Achte darauf, dass es sich um einen OGC-konformen Dienst handelt, sowie einen Name für den WMS-Layer.

##### 3. Layer und Zusatzinformation
Gib den gewünschten Layer ein, welcher eingebunden werden soll. Eine Mehrfachnennung ist möglich als Komma-separiert Liste. Weiterhin wird die Version des WMS benötigt, üblicherweise `1.3.0`. Optional können verfügbare Styles definiert werden. Untersützt der Layer Transparenz kann diese durch den Schieberegeler aktiviert werden.

##### 4. In der Karte prüfen
Öffne das Modul [**„Karte“**](../02_map#geodaten-visualiseren), um die eingebundenen WMS-Layer anzuzeigen. 

<hr>

### Tile-Service einbinden

Dieses Tutorial zeigt, wie ein externe [Tile-Service](https://github.com/CartoDB/basemap-styles) in die FieldMApp importiert und im Karten-Module visualisiert wird. 
 

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/add_tilelayer.mp4" type="video/mp4">
</video>


#### **Schritt-für-Schritt-Anleitung**

##### 1. Tile-Service als Quelle wählen
Tippe auf die Schaltfläche **+** (rechts unten). Es öffnet sich ein Auswahlfenster, hier **WMS/WMTS/XYZ** auswählen. Im neuen Pop-up-Fenster den Schieberegeler **TMS** aktivieren.

##### 2. Service-URL einfügen
Gib die URL des gewünschten Tile-Service in das dafür vorgesehene Feld ein, sowie einen Name für den Tile-Layer.

##### 3. Zusatzinformation
Weiterhin kann im Feld `Service Attributation` der Urheber des Dienstes hinterlegt werden. Durch das Feld `MapKey-URL` kann eine externe Legendengrafik geladen werden.

##### 4. In der Karte prüfen
Öffne das Modul [**„Karte“**](../02_map#geodaten-visualiseren), um die eingebundenen Tile-Layer anzuzeigen. 

<hr>

### Importierte Daten entfernen

Dieses Tutorial zeigt, wie die zuvor importierte `GeoJSON`-Datei (`elbe_basin.geojson`) aus der FieldMApp entfernt wird.

<video width="640" height="480" controls>
  <source src="https://github.com/fieldmapp/fieldmapp.github.io/raw/refs/heads/master/assets/video/delete_data.mp4" type="video/mp4">
</video>

#### **Schritt-für-Schritt-Anleitung**

##### 1. GeoJSON-Datei auswählen
Finde die zu löschende Datei/Quelle aus der Liste importierter Datenquellen im Importer-Module

##### 2. Quelle entfernen
Durch einen **long-press** auf die ausgewählte Quelle öffnet sich ein Lösch-Dialogfenster, in diesem muss die zu löschende Quelle bestätigt werden, wird dies bestätigt wird die Datenquelle entfernt. 
