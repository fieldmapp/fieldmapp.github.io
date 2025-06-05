---
title: "Externe Sensoren der FieldMApp"
weight: 200
description: >-
     Verwendung eines externen GNSS Empfängers.
---

# DGNSS
> **Hinweis**  
> DGNSS (*Differentielles* GNSS) ist eine Technologie, um eine höhere Positionsgenauigkeit zu erzielen. Dabei werden zusätzlich zu den GNSS-Signalen (*GNSS* Global Navigation Satellite System, ist ein Sammelbegriff für Satellitennavigationssysteme) noch differenzielle Korrekturdaten über das Internet empfangen. Bei der in der FieldMApp verwendeten **RTK** Korrektur erfolgt die Anwendung der Korrekturdaten in Echtzeit.

Es ist empfohlen, einen externen GNSS Empfänger mit externen Korrekturdaten zu verwenden um eine höhere Positionsgenauigkeit zu erzielen. Derzeit ist ein über USB verbundener **u-blox F9P** Empfänger unterstützt. Es kann derzeit **ausschließlich auf Android-Geräten** eingesetzt werden.

Im Folgenden werden die benötigten Schritte beschrieben.

## Empfänger verbinden
Der externe Empfänger muss mit einem USB-C zu USB-A Adapterkabel mit dem Tablet verbunden werden. Die Antenne muss mus mit dem Empfänger verbunden werden und mit freier Sicht auf den Himmel platziert werden.

## Android Aufforderung zustimmen
Bei Verbinden des Empfängers erscheint eine Aufforderung auf dem Bildschirm.
![Herstellen einer USB-Verbindung](/screenshots/screenshot_usb_verbindung.jpg)
*Aufforderung welcher bei Verbinden des GNSS-Empfängers erscheint*

## Internet Verbindung herstellen
Um die NTRIP Korrekturdaten zu empfangen muss eine Internetverbindung auf dem Tablet verfügbar sein.

## Auswählen der NTRIP Korrekturdaten
Es muss die korrekte Quelle für NTRIP-Korrekturdaten ausgewählt werden. Dazu das Bedienelement für die Positionsbestimmung ausklappen. Unter NTRIP-Korrektur muss das derzeitige Bundesland gewählt werden. Für einige Bundesländer werden personalisierte Zugangsdaten benötigt, welche durch Klick auf den Button nebem dem Namen des Bundeslandes eingegeben werden können. Für Bundesländer in denen der Zugang frei verfügbar ist, wie etwa Thüringen reicht ein Auswählen aus.

## Aktivieren
Durch Umlegen des Schalters `RTK aktivieren` wird die Verwendung des externen DGNSS-Exmpfängers aktiviert. Es kann nun etwa eine Minute dauern bis eine Positionsbestimmung möglich ist. Es ist durch erneutes Bedienen des Schalters jederzeit ein Wechsel zum internen Empfänger möglich.

> **Hinweis**  
> Die Qualitätsanzeige der Positionsbestimmung sollte von Rot (`NONE`) auf schließlich Blau (`FLOAT`) oder besser Grün (`FIX`) umschwenken um, was eine zuverlässige Positionsbestimmung signalisiert.

## Statusinformationen
In dem Bedienelement zur Positionsbestimmung können verschiedene Statusinformationen über die Verbindung angezeigt werden.

![Statusinformationen der RTK Verbindung](/screenshots/screenshot_rtk_aktiv.jpg)

*Statusinformationen der RTK Verbindung* 

## Unterstützte Hardware
### Empfänger
 - [u-blox F9P USB-Modul](https://gnss.store/zed-f9p-gnss-modules/126-elt0110.html)
### Antenne
 - [u-blox ANN-MB Series](https://www.u-blox.com/en/product/ann-mb-series)


