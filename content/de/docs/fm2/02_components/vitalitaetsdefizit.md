---
title: "Vitalitätsdefizitlayer"
weight: 200
description: >-
     Der Vitalitätsdefizitlayer der FieldMApp ermöglicht es, die Vitatliät eines Feldes zu betrachten.
---

# Hintergrund

Ein Vitalitätsdefizit-Layer ist ein fernerkundungsbasierter Datenlayer, der in der FieldMApp als zusätzliche Informations- und Orientierungshilfe dargestellt werden kann. Er ermöglicht es, für vergangenen Jahre, die Vitalität des Bestandes auf dem betrachteten Feld mit dem durchschnittlichen Zustand anderer Felder der gleichen Kulturart im selben Naturraum zu vergleichen. Der Layer basiert auf multispektralen Satellitendaten. Es handelt sich um einen pixelbasierten Datensatz mit 10m Auflösung, so dass Unterschiede innerhalb eines Feldes sichtbar werden können. 

## Daten und Methodik

### Satellitendaten

Die Vitalitätsdefizit-Layer basieren auf Multispektraldaten der Erdbeobachtungsmission Sentinel-2. Diese Mission beinhaltet aktuell zwei identische Satelliten, Sentinel-2A und Sentinel-2B, die in einer sonnensynchronen Umlaufbahn operieren. Das auf den Satelliten befindliche MultiSpectral Imager (MSI) liefert hochauflösende multispektrale Bilder in 13 Wellenlängenbereichen. Die Bilddaten enthalten wichtige Informationen zum Pflanzenzustand und können somit beim Monitoring der Vitalität von Pflanzenbeständen, bei Vegetationskartierungen und ähnlichen Anwendungen unterstützen. Die Bilddaten werden mit einer Wiederholungsrate von etwa 5 Tagen aufgenommen. Im Falle von Bewölkung kann die Landoberfläche allerdings nicht beobachtet werden, so dass hier zeitliche Lücken von mehr als 5 Tagen entstehen können.

### Erzeugung von Vegetationsindex-Zeitreihen

Für die Erzeugung der Vitalitätsdefizit-Layer werden die Sentinel-Daten zunächst mit dem Sen2Cor Prozessor atmosphärisch korrigiert, die Wolkenmaskierung erfolgt mithilfe des Scene-Classification-Layers (SCL). Es wird ein Datenstapel der Sentinel-2 Aufnahmen erstellt und Wolkenlücken werden linear interpoliert. Die Zeitreihen von März bis Oktober werden schließlich mit dem Savitzky-Golay-Filter geglättet. Anschließend werden für 5-Tages-Schritte zwei Vegetationsindizes berechnet, welche mit der Dichte, Grünheit und Vitalität von Vegetationsbeständen korrelieren: der Normalized Difference Vegetation Index (NDVI) und der Enhanced Vegetation Index (EVI).

![Screenshot Karte](/graphs/vit_ndvi_1.png)
*Abbildung 1: Kartenausschnitt für Felder bei Demmin für einen NDVI Layer am 28.04.2024*

![Berechnung NDVI EVI](/graphs/ndvi_calculation.png)

*Abbildung 2: Berechnung des `NDVI` und `EVI`*


### Berechnung der durchschnittlichen Vitalität und der Vitalitätsdefizit-Layer

Geodaten zur landwirtschaftlichen Nutzung - aus Daten des IACS (Integrated Administration and Control System) oder aus satellitenbasierten Feldfruchtkartierungen - werden zu 17 Feldfruchtklassen aggregiert. Diese Klassen umfassen Winterweizen, Wintergerste, Winterroggen, sonstige Wintergetreide, Sommerweizen, Sommerroggen, Sommerhafer, Mais, Leguminosen, Kartoffeln, Zuckerrübe, Winterraps, Klee/Luzerne, Ackergras, Dauergrünland, Wein und Obstbäume, wobei in jeder Klasse zwischen konventionellem und biologischem Anbau unterschieden wird. Im Anschluss werden innerhalb der Naturräume (Bundesamt für Naturschutz) pro Feldfrucht der Mittelwert und die Standardabweichung der beiden Vegetationsindizes für jeden 5-Tages-Schritt berechnet. Schließlich werden von den aufbereiteten 5-tägigen Vegetationsindex-Zeitreihen die für den gegebenen Naturraum, die gegebene Feldfrucht und den gegebenen Zeitschritt passenden Mittelwerte abgezogen. Der resultierende Datensatz wird als Vitalitätsdefizit-Layer bezeichnet. 

## Interpretation der Vitalitätsdefizit-Layer

Abbildung 2 zeigt den Vitalitätsdefizitlayer für den 28.04.2024 für Felder bei Demmin im Naturraum *Nordostmecklenburgischen Tiefland*. In den blassgelb eingefärbten Kartenbereichen entspricht die Vitalität des Bestandes zu diesem Zeitpunkt in etwa dem Durchschnitt aller Felder in diesem Naturraum – die Werte sind dabei auf die jeweilige Feldfrucht angepasst. Dort, wo Bereiche des Feldes Orange- und Rottöne aufweisen (z.B. im Rapsfeld in der Kartenmitte) ist die Vitalität des Raps geringer und dort, wo Grün- und Blautöne zu sehen sind (z.B. im Winterweizenfeld darunter) ist die Vitalität höher als dies im Mittel für alle anderen Raps bzw. Winterweizen-Felder des Naturraums beobachtet wurde. Besonders rote Bereiche können sich auf Minderertragsflächen (eingekreist in Abbildung 3) zeigen, wie z.B. auf Sandlinsen. Im Unterschied zu der einfachen Darstellung des Vegetationsindizes (vgl. Abbildung 1) erhält man mit den Vitalitätsdefizitlayern eine zusätzliche Information über die Pflanzenvitalität durch den räumlichen Vergleich. Über einen zweiten Kanal im Vitalitätsdefizitlayer kann man über die feldfruchtspezifische Standardabweichung (vgl. Abbildung 4) die Farbskalierung und -darstellung anpassen (z.B. durch z-Standardisierung). Somit bleiben die Vitalitätsdefizite auch für unterschiedliche Feldfrüchte vergleichbar. 

![Screenshot Karte](/graphs/vit_ndvi_2.png)
*Abbildung 3: Kartenausschnitt für Felder bei Demmin für einen Vitalitätsdefizitlayer am 28.04.2024. Schwarze Bereiche sind nicht-landwirtschaftlich genutzte Flächen (OpenStreetMap 2025)*

![Screenshot Karte](/graphs/vit_ndvi_3.png)
*Abbildung 4: Kartenausschnitt für Felder bei Demmin für die feldfruchtspezifische Standardabweichung des NDVI am 28.04.2024. Schwarze Bereiche sind nicht-landwirtschaftlich genutzte Flächen (OpenStreetMap 2025).*

**Autoren & Entwickler**

   * Konzept: Ursula Gessner und Patrick Klotz

   * Dokumentation im Wiki: Ursula Gessner

   * Code-Entwicklung: Patrick Klotz

**Zitationsvorschlag**


BUNDESAMT FÜR NATURSCHUTZ (Hrsg.) (2008): Daten zur Natur 2008. – Münster (Landwirtschaftsverlag): 10-11.SSYMANK, A. (1994): Neue Anforderungen im europäischen Naturschutz: Das Schutzgebietssystem Natura 2000 und die FFH-Richtlinie der EU. – Natur und Lan-schaft 69 (Heft 9): 395-406.

Magdalena Main-Knorn, Bringfried Pflug, Jerome Louis, Vincent Debaecker, Uwe Müller-Wilm, Ferran Gascon, "Sen2Cor for Sentinel-2," Proc. SPIE 10427, Image and Signal Processing for Remote Sensing XXIII, 1042704 (4 October 2017);[ https://doi.org/10.1117/12.2278218](https://doi.org/10.1117/12.2278218)

OpenStreetMap contributors (2025). *OpenStreetMap*. OpenStreetMap Foundation. Available as open data under the Open Data Commons Open Database License (ODbL) at [openstreetmap.org](http://openstreetmap.org/)

Savitzky, Abraham.; Golay, M. J. E. (1964): Smoothing and Differentiation of Data by Simplified Least Squares Procedures. In: Anal. Chem. 36 (8), S. 1627–1639. DOI: 10.1021/ac60214a047.

