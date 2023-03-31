
---
title: "Entwickler: CheatSheet"
linkTitle: "CheatSheet"
weight: 10000
description: >-
     Schnellhilfe für Entwickler.
---

# APK erstellen

Anleitung für Visual Studio Community 2022 (englisch)
1. Sicherstellen, dass "Release" (und nicht "Debug") bei "Solution Configurations" (in 2. Reihe von oben, direkt unter "File, Edit, View, ...") ausgewählt ist
2. Im "Solution Explorer" Rechtsklick auf das Projekt "DLR_Data_App.Android" -> "Set as Startup Project"
3. Wieder Rechtsklick auf "DLR_Data_App.Android" -> "Archive..."
4. Nun wird die aktuelle Version der Android App archiviert. Ggf muss man hier in der Liste nochmal nach oben scrollen um das aktuellste Archiv zu sehen
5. Das aktuellste Archiv mit Linksklick auswählen, dann unten links im Fenster auf "Distribute..." -> "Ad Hoc"
6. Nun muss eine Identität zum signieren der APK ausgewählt werden. Wenn noch keine erstellt wurde, kann man das hier mit dem "+" machen
7. Dann unten rechts auf "Save as...". Nun öffnet sich ein Explorer in dem man auswählen kann wo die APK gespeichert werden soll.
8. Mit "Speichern" wird die APK am angegebenen Ort gespeichert. An dieser Stelle muss man noch das Passwort für die Signierungsidentität eingeben.

Zu beliebigen Schritten kann das Archivieren "Value cannot be Zero" auftauchen. In dem Fall zuerst einfach nochmal das Archivieren von vorn starten.

# Bestehende Module zur Android App hinzufügen

Anleitung für Visual Studio Community 2022 (englisch)
1. Im "Solution Explorer" das Projekt "DLR_Data_App.Android" aufklappen.
2. Unter "DLR_Data_App.Android" rechtsklick auf "References" -> "Add References"
3. Der "Reference Manager" öffnet sich. Hier links in "Projects" wechseln, wenn es sich nicht automatisch ausgewählt hat.
4. Immer ausgewählt sollten sein: "DLR_Data_App", "DlrDataApp.Modules.Base.Android", "DlrDataApp.Modules.Base.Shared"
5. Je nachdem welche Module verfügbar sein sollen, kann man hier beliebig auswählen: (wenn ein Projekt eines Moduls ausgewählt ist, müssen es alle sein)
     - Profiling: DlrDataApp.Modules.Profiling.Android, DlrDataApp.Modules.Profiling.Shared
     - Projekte (bzw ODK Formulare): DlrDataApp.Modules.OdkProjects.Android, DlrDataApp.Modules.OdkProjects.Shared; **Außerdem**: das "Profiling" Modul
     - Spracherkennung: DlrDataApp.Modules.SpeechRecognition.Android, DlrDataApp.Modules.SpeechRecognition.Shared
     - Fahrtansicht (bzw Feldkartierer): DlrDataApp.Modules.FieldCartographer.Android, DlrDataApp.Modules.FieldCartographer.Shared; **Außerdem**: das "Spracherkennungs" Modul

# Modulstruktur, Shared Methods, Navigation

Siehe Nextcloud Documentation/fieldmapp1modulexplanation.pdf
