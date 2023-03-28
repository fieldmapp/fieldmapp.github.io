
---
title: "Entwicklerübersicht"
weight: 300
description: >-
     Alles Relevante für die Weiterentwicklung der FieldMApp.
---

# Übersicht

TODO: Warum sollte man die FieldMApp nutzen? In wie fern erleichtert es die Entwicklung eigener (aufbauender) Datenaufnahme-Apps? Auf welchen Systemen wird die FieldMApp unterstützt?

## Aufsetzen der Entwicklungsumgebung

Das Projekt nutzt Visual Studio Community 2019 als Entwicklungsumgebung. Dabei muss für Xamarin.Forms bei der Installation (oder nachträglich mit dem Visual Studio Installer) das Paket "Mobile Entwicklung mit .NET" ausgewählt worden sein.

## Allgemeines

Die FieldMApp ist modular aufgebaut. Für Module stehen verschiedene verschiedene Funktionalitäten bereit, darunter:
- Nutzerverwaltung
- Zugriff auf grundlegende Smartphone-Sensorik
- App-Navigation
- Datenbankzugriff

Diese werden durch eine Schnittstelle im Basismodul "DlrDataApp.Modules.SharedModule" verfügbar gemacht und können von allen anderen Modulen genutzt werden.

# Module

TODO: Abhängigkeitsdiagramm

| Modulartikel | Kurzbeschreibung |
| ------ | ----- |
| [Profiling](Profiling) | Evaluieren der Nutzerkompetenz durch mehrere Fragen und anschließender Selbsteinschätzung |
| [Projekte](Projects) | Importieren und Ausfüllen von [ODK](https://getodk.org/) Formularen |
|  [Fahrtansicht](DrivingView) | Nutzergesteuerte Kartierung von besonderen Gebieten auf landwirtschaftlich genutzten Feldern |