---
title: "Vitalitätsdefizitlayer"
weight: 200
description: >-
     Satellitenbildprodukt zur Beurteilung der aktuellen Pflanzenentwicklung auf Feldern
---

## Hintergrund

Ein Vitalitätsdefizit-Layer ist ein fernerkundungsbasierter Datenlayer, der in der FieldMApp als zusätzliche Informations- und Orientierungshilfe dargestellt werden kann. Der Vitalitätsdefizit-Layer ermöglicht es, für vergangene Jahre, die Vitalität des Bestandes auf dem betrachteten Feld mit dem durchschnittlichen Zustand anderer Felder der gleichen Kulturart im selben Naturraum zu vergleichen. Der Layer basiert auf multispektralen Satellitendaten. Es handelt sich um einen pixelbasierten Datensatz mit 10m Auflösung, so dass Unterschiede innerhalb eines Feldes sichtbar werden können. 

## Daten und Methodik

### Satellitendaten

Die Vitalitätsdefizit-Layer basieren auf Multispektraldaten der Erdbeobachtungsmission Sentinel-2. Diese Mission beinhaltet aktuell zwei identische Satelliten, Sentinel-2A und Sentinel-2B, die in einer sonnensynchronen Umlaufbahn operieren. Das auf den Satelliten befindliche Multi-Spectral-Instrument (MSI) liefert hochauflösende multispektrale Bilder in 13 Wellenlängenbereichen. Die Bilddaten enthalten wichtige Informationen zum Pflanzenzustand und können somit beim Monitoring der Vitalität von Pflanzenbeständen, bei Vegetationskartierungen und ähnlichen Anwendungen unterstützen. Die Bilddaten werden mit einer Wiederholungsrate von etwa 5 Tagen aufgenommen. Im Falle von Bewölkung kann die Landoberfläche allerdings nicht beobachtet werden, so dass hier zeitliche Lücken von mehr als 5 Tagen entstehen können.

### Erzeugung von Vegetationsindex-Zeitreihen

Für die Erzeugung der Vitalitätsdefizit-Layer werden die Sentinel-Daten zunächst mit dem Sen2Cor Prozessor (Main-Knor et al. 2017) atmosphärisch korrigiert. Die Wolkenmaskierung erfolgt mithilfe des Scene-Classification-Layers (SCL, Main-Knor et al. 2017). Es wird ein Datenstapel der Sentinel-2 Aufnahmen erstellt und Wolkenlücken werden linear interpoliert. Die Zeitreihen von März bis Oktober werden schließlich mit dem Savitzky-Golay-Filter (Savitzky & Golay 1964) geglättet. Anschließend werden für 5-Tages-Schritte zwei Vegetationsindizes berechnet, welche mit der Dichte, Grünheit und Vitalität von Vegetationsbeständen korrelieren: der Normalized Difference Vegetation Index (NDVI; Abb. 1) und der Enhanced Vegetation Index (EVI). Diese werden wie folgt berechnet:

![Berechnung NDVI EVI](/graphs/ndvi_calculation.png)

Dabei steht ROT und NIR für die ermittelte Reflektanz der Wellenlängenbereiche, die Rot beziehungsweise nahes Infrarot abdecken.

![Screenshot Karte](/graphs/vit_ndvi_1.png)
*Abbildung 1: Kartenausschnitt für Felder bei Demmin für einen NDVI Layer am 28.04.2024*

### Berechnung der durchschnittlichen Vitalität und der Vitalitätsdefizit-Layer

Geodaten zur landwirtschaftlichen Nutzung - aus Daten des IACS (Integrated Administration and Control System) oder aus satellitenbasierten Feldfruchtkartierungen - werden zu 17 Feldfruchtklassen aggregiert. Diese Klassen umfassen Winterweizen, Wintergerste, Winterroggen, sonstige Wintergetreide, Sommerweizen, Sommerroggen, Sommerhafer, Mais, Leguminosen, Kartoffeln, Zuckerrübe, Winterraps, Klee/Luzerne, Ackergras, Dauergrünland, Wein und Obstbäume, wobei in jeder Klasse zwischen konventionellem und biologischem Anbau unterschieden wird. Im Anschluss werden innerhalb der Naturräume (BfN 2011) pro Feldfrucht der Mittelwert und die Standardabweichung der beiden Vegetationsindizes für jeden 5-Tages-Schritt berechnet. Schließlich werden von den aufbereiteten 5-tägigen Vegetationsindex-Zeitreihen die für den gegebenen Naturraum, die gegebene Feldfrucht und den gegebenen Zeitschritt passenden Mittelwerte abgezogen. Der resultierende Datensatz wird als Vitalitätsdefizit-Layer bezeichnet. 

## Interpretation der Vitalitätsdefizit-Layer

Abbildung 2 zeigt den Vitalitätsdefizitlayer für den 28.04.2024 für Felder bei Demmin im Naturraum *Nordostmecklenburgischen Tiefland*. In den blassgelb eingefärbten Kartenbereichen entspricht die Vitalität des Bestandes zu diesem Zeitpunkt in etwa dem Durchschnitt aller Felder in diesem Naturraum – die Werte sind dabei auf die jeweilige Feldfrucht angepasst. Dort, wo Bereiche des Feldes Orange- und Rottöne aufweisen (z.B. für das Rapsfeld in der Kartenmitte) ist die Vitalität geringer und dort, wo Grün- und Blautöne zu sehen sind (z.B. im Winterweizenfeld darunter) ist die Vitalität höher als dies im Mittel für alle anderen Raps- bzw. Winterweizen-Felder des Naturraums beobachtet wurde. Besonders rote Bereiche können auf Minderertragsflächen (eingekreist in Abb. 2) hindeuten. Im Unterschied zu der einfachen Darstellung des Vegetationsindizes (vgl. Abb. 1) erhält man mit den Vitalitätsdefizitlayern eine zusätzliche Information über die Pflanzenvitalität durch den räumlichen Vergleich. Über einen zweiten Kanal im Vitalitätsdefizitlayer kann man über die feldfruchtspezifische Standardabweichung (vgl. Abb. 3) die Farbskalierung und -darstellung anpassen (z.B. durch z-Standardisierung). Somit bleiben die Vitalitätsdefizite auch für unterschiedliche Feldfrüchte vergleichbar. 

![Screenshot Karte](/graphs/vit_ndvi_2.png)
*Abbildung 2: Kartenausschnitt für Felder bei Demmin für einen Vitalitätsdefizitlayer am 28.04.2024. Schwarze Bereiche sind nicht-landwirtschaftlich genutzte Flächen (OSM 2025)*

![Screenshot Karte](/graphs/vit_ndvi_3.png)
*Abbildung 3: Kartenausschnitt für Felder bei Demmin für die feldfruchtspezifische Standardabweichung des NDVI am 28.04.2024. Schwarze Bereiche sind nicht-landwirtschaftlich genutzte Flächen (OSM 2025).*

**Autoren & Entwickler**

   * Konzept: Ursula Gessner und Patrick Klotz

   * Dokumentation im Wiki: Ursula Gessner

   * Code-Entwicklung: Patrick Klotz

**Referenzen**
Bundesamt für Naturschutz (BfN) (Hrsg.) (2011): Naturräume und Großlandschaften Deutschlands. <https://www.bfn.de/daten-und-fakten/biogeografische-regionen-und-naturraeumliche-haupteinheiten-deutschlands> (Stand: 2011) (Zugriff: 2025-02-21).

Main-Knorn M., B.Pflug, J. Louis, V. Debaecker, U. Müller-Wilm, F. Gascon (2017): Sen2Cor for Sentinel-2. – Proceedings SPIE 10427, Image and Signal Processing for Remote Sensing XXIII, 1042704 (4 October 2017). DOI: [10.1117/12.2278218](https://doi.org/10.1117/12.2278218).

OpenStreetMap contributors (OSM) (2025): OpenStreetMap. OpenStreetMap Foundation. <openstreetmap.org> (Stand: 2025-02-21) (Zugriff: 2025-02-21).

Savitzky, A. & M. J. E. Golay (1964): Smoothing and Differentiation of Data by Simplified Least Squares Procedures.  – Analytic Chemistry 36 (8), 1627–1639. DOI: [10.1021/ac60214a047](https://doi.org/10.1021/ac60214a047).

**Zitationsvorschlag**
Gessner, U. & P. Klotz (2025): FieldMApp. Komponenten der FieldMApp. Vitalitätsdefizitlayer. <https://fieldmapp.github.io/docs/fm2/02_components/vitalitaetsdefizit/> (Stand: 2025-06-02) (Zugriff: YYYY-MM-DD).