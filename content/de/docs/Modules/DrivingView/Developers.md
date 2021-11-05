
---
title: "Module - Fahrtansicht: Entwickler"
linkTitle: "Entwickler"
weight: 100
description: >-
     Informationen über die Software-Umsetzung der Fartansicht.
---

## Übersicht

TODO: Wie ist das Modul aufgebaut? Wie kann man es erweitern?

## Zustände

Die Zustände jeder Zone lassen sich in folgendem Diagramm darstellen:
![drivingView2_1_](uploads/200cc46837b3e9dc6ebf1101fe1fe1e4/drivingView2_1_.png)

Die Schadensdetail-Button (Ursache & Stärke des Minderertrags) werden von allen Zonen geteilt verwendet. Alle anderen Buttons ("Anfang", "Stop", Spurauswahl) sind für jede Zone einzeln vorhanden.

## Spracheingabe

Bei der Spracheingabe wird folgende formale Grammatik erlaubt (angegeben in [EBNF](https://de.wikipedia.org/wiki/Erweiterte_Backus-Naur-Form)):

```
Programm = "abbrechen" | ZonenStart | ZonenEnde | ZonenTypisierung;
ZonenStart = "start", SpurenAufzählung;
ZonenEnde = "stop", SpurenAufzählung;
ZonenTypisierung = ( ZonenTypisierung1 | ZonenTypisierung2 | ZonenTypisierung3 | ZonenTypisierung4 ), [ "stop" ];
ZonenTypisierung1 = SpurenAufzählung, ZonenAngabe;
ZonenTypisierung2 = ZonenAngabe, SpurenAufzählung;
ZonenTypisierung3 = MinderertragsUrsache, ZonenAngabe, MinderertragsTyp;
ZonenTypisierung4 = MinderertragsTyp, ZonenAngabe, MinderertragsUrsache;
ZonenAngabe = ( ( MinderertragsUrsache, MinderertragsTyp ) | ( MinderertragsTyp, MinderertragsUrsache) | MinderertragsUrsache | MinderertragsTyp );
MinderertragsUrsache = "hang" | "nass" | "nässe" | "maus" | "wild" | "lehm" | "sand" | "kuppe" | "ton" | "verdichtung" | "wende";
MinderertragsTyp = "gering" | "mittel" | "hoch";
SpurenAufzählung = [ "zone" ], SpurenAufzählungTeil, { SpurenAufzählungTeil };
SpurenAufzählungTeil = "spur" | ( ( "links" | "rechts" ), SpurBezeichnung, { SpurBezeichnung } );
SpurBezeichnung =  "eins" | "zwei" | "drei";
```