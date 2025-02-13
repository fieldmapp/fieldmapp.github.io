
---
title: "Module - Profiling: Projektmanager"
linkTitle: "Profiling"
weight: 100
description: >-
     Informationen zur Nutzung des Profiling und den damit gewonnen Daten.
---

## Übersicht

TODO: Was kann das Modul leisten? Welche Daten werden gewonnen? Was ist dazu notwendig?

## Einfügen neuer Fragen

Die Fragen sind in den txt Dateien unter MobileDataCollection.Survey.Android Assets gespeichert. (TODO: Korrigieren sobald "modularize" abgeschlossen ist)

Es gibt einige Attribute, die für alle Fragen gleich sind. Zudem gibt es Konventionen für die Nutzung von Strings.
Jeder Fragentyp hat das Attribut `InternId`. Dieses dient als Primärschlüssel mit dem man die Frage eindeutig identifizieren kann. Dieses sollte also immer eineindeutig für eine gespeicherte Frage vergeben werden. Zudem enthält jeder Typ (bis auf Introspection) das Attribut `Difficulty`. Dies ist eine Zahl von 1, für leicht, bis 3, für schwer, welche den Schwierigkeitsgrad der Frage angibt. Der Fragetext ist im Attribut `QuestionText` gespeichert und auch in jedem Fragetyp vorhanden.

Die Fragen sind im JSON-Format in der Datei "questions" abgelegt. Zeilenumbrüche und Leerzeichen können also zur Formatierung (außerhalb von Strings) beliebig eingesetzt werden. Zudem unterstützt die von uns genutzte JSON-Bibliothek (Newtonsoft JSON) sowohl einzeilige als auch mehrzeilige Kommentare im C#-Stil.

Damit Bilder richtig geladen werden können, müssen diese mit Visual Studio in die Ordner Resources/drawable-mdpi für "niedrig" auflösende Bilder und in Resources/drawable-xhdpi für "hoch" auflösende Bilder abgelegt werden. Der Name der beiden Bilder muss gleich sein, damit das System erkennt, dass es sich um den gleichen Inhalt unterschiedlicher Auflösung handelt. Es wird dann automatisch in Abhängigkeit der Display-Größe das passende Bild angezeigt. Der Namen der Bilder muss immer mit dem jeweiligen Format enden z.B. "Bild.png". Nach dem Hinzufügen neuer Bilder muss die App neu erstellt (kompiliert) werden, damit die neuen Bilder übertragen werden. Dasselbe gilt für neu hinzugefügte Fragen.

### 1. Fragen für den DoubleSlider Typ

Der DoubleSlider Typ beinhaltet ein Bild und zwei Slider auf denen man jeweils einen Wert von 0 bis 100 angeben kann. Die Frage lautet immer: "Schätzen Sie den Grad der Bedeckung des Bodens durch Pflanzen (A) und den Anteil grüner Pflanzenbestandteile (B) ein."

Ein QuestionDoubleSlider Objekt benötigt die Attribute `int InternId`, `string QuestionText`, `int Difficulty`, `string PictureAddress`, `int AnswerA`, `int AnswerB`, um erstellt zu werden. Das Attribut `QuestionText` enthält die anzuzeigende Frage. Diese kann beliebig gewählt werden. `AnswerA` und `AnswerB` stehen jeweils für die korrekten Antworten; für die Frage der Bodenbedeckung durch Pflanzen (A) und den Anteil grüner Pflanzenbestandteile (B) wird ein Wert von 0 bis 100 gesetzt. Der String `PictureAdress` enthält den Namen des Bildes, das für diese Frage angezeigt werden soll.

Um eine neue Frage einzufügen, öffnet man "questions", geht zum Eintrag "DoubleSlider", kopiert einen bestehenden Eintrag und fügt die neuen Werte ein.

### 2. Fragen für den ImageChecker Typ

Der ImageChecker Typ beinhaltet 4 Bilder, die einzeln ausgewählt werden können. Die Fragen dazu lauten z.B.: "Wo sehen sie die Feldfruchtsorte Weizen abgebildet?"

Ein QuestionImageChecker Objekt benötigt die Attribute `int Internid`, `string QuestionText`, `int Difficulty`, `int Image1Correct`, `int Image2Correct`, `int Image3Correct`, `int Image4Correct`, `string Image1Source`, `string Image2Source`, `string Image3Source`, `string Image4Source`, um erstellt zu werden. Das Attribut `QuestionText` enthält die anzuzeigende Frage. Diese kann beliebig gewählt werden. Die Attribute `Image1Correct`, `Image2Correct`, `Image3Correct` und `Image4Correct` geben an, welches Bild korrekt ist. Es können auch mehrere korrekt sein. Diese haben dann den Wert 1. Die falschen Bilder haben den Wert 0. Die Attribute `Image1Source`, `Image2Source`, `Image3Source` und `Image4Source` geben den Namen der einzelnen Bilder an.

Um eine neue Frage einzufügen, öffnet man "questions", geht zum Eintrag "ImageChecker", kopiert einen bestehenden Eintrag und fügt die neuen Werte ein.

### 3. Fragen für den Stadium Typ

Der Stadium Typ beinhaltet ein Bild und 2 Listen, in denen man zum einem das Wuchsstadium der Pflanze und zum anderem die Art der Pflanze anklicken kann. Die Fragen dazu lauten z.B.: "Ordnen Sie dem Bild eine Feldfruchtsorte und das/die Entwicklungstadium/-stadien zu."

Ein QuestionStadium Objekt benötigt die Attribute `int InternId`, `string QuestionText`, `int Difficulty`, `string Image`, `List<StadiumSubItem> Stadiums`, `List<Plant> Plants`, `int CorrectAnswerStadium`, `string CorrectAnswerFruitType`. Die Liste `Stadiums` enthält mehrere StadiumSubItem Elemente. Die Elemente werden als JSON-Liste abgebildet. Das Gleiche gilt für die Liste `Plants`.
Das Attribut `CorrectAnswerStadium` ist eine Zahl von 1 bis 9 und gibt damit an, welches Element aus der List `Stadiums` das richtige Element ist. Die Elemente haben ihren Index (beginnend mit 0) als Zahl. Das Attribut `CorrectAnswerFruitType` ist ein String der Länge 1 und gibt an welches Element aus der Liste `Plants` das richtige Element ist.

Um eine neue Frage einzufügen, öffnet man "questions", geht zum Eintrag "Stadium", kopiert einen bestehenden Eintrag und fügt die neuen Werte ein.

### 4. Fragen für den Introspection Typ

Diese Fragen stellen eine Besonderheit dar, da es sich hier um die Selbsteinschätzung handelt. Daher haben die Fragen keine Bilder oder Schwierigkeiten, sondern nur einen Text und eine Auswahlmöglichkeit von 1 bis 5.

Ein QuestionIntrospection Objekt benötigt die Attribute `int InternId`, `string QuestionText`. Der `QuestionText` gibt dabei die Behauptung zur Selbsteinschätzung an z.B.: "Ich kann die Sorte von Feldfrüchten zuverlässig erkennen".

Um eine neue Frage einzufügen, öffnet man "questions", geht zum Eintrag "Introspection", kopiert einen bestehenden Eintrag und fügt die neuen Werte ein.