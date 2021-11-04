
---
title: "Module - Profiling: Entwickler"
weight: 100
description: >-
     Informationen über die Software-Umsetzung des Profilings.
---

## Übersicht

TODO: Wie ist das Modul aufgebaut? Wie kann man es erweitern?

## Struktur der Modul-Navigation

Das Profiling-Modul nutzt den Navigations-Stack um die einzelnen Seiten anzuzeigen. Angezeigt wird immer nur die oberste Seite. Dabei liegt die Hauptseite des Moduls die ganze Zeit am Boden vom Stack und wird nie entfernt. Sobald eine Kategorie ausgewählt wird, wird eine Seite mit einem Lade-Icon auf den Stack geladen. Erst darauf dann die entsprechende Frage-/Auswertungsseite. Beim Schließen der Frage-/Auswertungsseite muss die Seite mit dem Lade-Icon auch entfernt werden damit man wieder das Hauptmenü sieht.

### Generelle Modul-Struktur

Die gesamte organisatorische Struktur liegt in der Klasse `SurveyManager`. Dies umfasst:
- das Erzeugen und Anzeigen neuer Frageseiten (bzw Pushen in den Navigations-Stack)
- das Erzeugen der Auswertungsobjekte
- das Erzeugen und Anzeigen neuer Auswertungsseiten
- das Aufrufen der Funktionen zum Speichern und Laden von Fragen und Antworten (die Funktionen werden bereitgestellt durch `DatabankCommunication`)

![Diagram_2019-10-14_10-08-33](uploads/7fe769beacf52a44573ecb6b03fcc0f3/Diagram_2019-10-14_10-08-33.png)


## Einfügen einer neuen Fragenkategorie

### 1. Erstellung einer Frage-Klasse

Angenommen unsere neue einzufügende Kategorie heißt "FruitChecker". Die Funktionalität dieser Kategorie ist für die Erklärung nachgeordnet. Sie dient hier nur als Namensplatzhalter, um zu verdeutlichen wie man Dinge benennen könnte/sollte.

Es muss sich Gedanken gemacht werden, welche Attribute die Frage und die passende Antwort brauchen, um abgespeichert zu werden. Dann erstellt man eine neue Klasse im Namespace "MobileDataCollection.Survey.Models" `QuestionFruitCheckePager.cs`, welche die Klasse für die Fragen darstellt. Benennungsschema und Namespace sind hier wichtig, da die zugehörigen Klassen einer Fragekategorie mit Reflection gesucht werden. Sie erbt Methoden und Eigenschaften von der Klasse BindableObject. Außerdem muss sie das Interface IQuestionContent implementieren. Das bedeutet sie muss sowohl `int InternId`, welches als Primärschlüssel dient, und `int Difficulty`, welches die Schwierigkeit der Frage angibt, implementieren. Andere benötigte Attribute können dann auch in QuestionFruitCheckerPage definiert werden. Man kann sich hier an den schon erstellten Klassen `QuestionDoubleSliderPage.cs`, `QuestionImageCheckerPage.cs`, `QuestionStadiumPage.cs` und `QuestionIntrospectionPage.cs` orientieren.

### 2. Erstellung einer Antwort-Klasse

Man muss eine Klasse für die Antworten erstellen, was in unserem Beispiel `AnswerFruitCheckerPage.cs` im Namespace "MobileDataCollection.Survey.Models" entspricht. Diese Klasse erbt BindableObject und das Interface IUserAnswer. Das heißt, es muss `int InternId` implementiert werden, der hier auch als Primärschlüssel dient, um die Antwort einer Frage zuzuordnen. Es muss auch eine Methode `float EvalulateScore(IUserAnswer)` implementiert werden. Diese gibt den Wert (zwischen 0 und 100) zurück, wie gut diese Frage beantwortet wurde. Dann benötigt die Klasse noch die erwarteten Antworten. Man kann sich hier an den schon erstellten Klassen `AnswerDoubleSliderPage.cs`, `AnswerImageCheckerPage.cs`, `AnswerStadiumPage.cs` und `AnswerIntrospectionpage.cs` orientieren.

### 3. Erstellung eines Layouts

Wenn ein neues Layout für diese Kategorie geschrieben werden soll, dann wird dieses wird als XAML "FruitCheckerPage.xaml" im Namespace "MobileDataCollection.Survey.Views" gespeichert. Für die Gestaltung sind keine Grenzen gesetzt. Es muss darauf geachtet werden, dass die App hauptsächlich von Durchschnittsbenutzern genutzt wird und man deshalb das Design sowie Interaktionen simple und intuitiv gestaltet.
Auch sollten die Button WeiterButton, AbbrechenButton und BackButton im Layout enthalten sein, um über die verschiedenen Kategorien ein einheitliches Design zu behalten.

Diese XAML Datei hat eine zugehörige Klasse in diesem Fall "FruitCheckerPage.xaml.cs". Sie steuert was in dem Layout angezeigt wird und was passiert, wenn man auf Button oder Bilder klickt. Diese Klasse erbt ContentPage und das Interface ISurveyPage.
Der Konstruktor der Klasse benötigt die Parameter `QuestionFruitCheckerPage question`, `int answersGiven` und `int answersNeeded`. Die Reihenfolge der Parameter ist hier wichtig, da Instanzen der Klassen wieder über Reflection erstellt werden. Die Methoden `OnWeiterButtonClicked`, `OnAbbrechenButtonClicked` und `OnBackButtonPressed` können aus beispielsweise `DoubleSliderPage.xaml.cs` kopiert und müssen dann noch auf die Kategorie angepasst werden. Auch können die Attribute `QuestionItem`, `AnswerItem` und `Header` kopiert und müssen dann noch auf "QuestionFruitCheckerPage" angepasst werden. Insgesamt kann man sich bei der Implementierung der Klasse sehr an den Klassen `DoubleSliderPage.xam.cs`, `ImageCheckerPage.xaml.cs`, `StadiumPage.xaml.cs` und `IntrospectionPage.xaml.cs` orientieren.

### 4. Erstellung eines SurveyMenuItem

Damit man die Fragen später auch auswählen kann, muss ein SurveyMenuItem des Objektes erstellt werden. Es wird später in der MainPage in einer Liste angezeigt. Das Objekt speichert eine interne Id der Kategorie (im Beispiel von oben "FruitChecker"), den anzuzeigenden Namen der Kategorie, wie viele Fragen in der Kategorie zu beantworten sind, die maximale Anzahl an Fragen, die Anzahl an beantworteten Fragen, eine Liste mit Ids der Selbsteinschätzungsfragen für diese Kategorie, der Antwortserie (wie viele Antworten in Folge richtig bzw. falsch waren) und die aktuelle Schwierigkeitsstufe. Damit so ein Objekt erstellt wird, muss es in der JSON-Datei "surveys" in "MobileDataCollection.Survey/Android/Assets" aufgelistet sein.

### 5. Speichern und Laden der Fragen und Antworten

Die Klassen werden automatisch deserialisiert und serialisiert. Attribute die dabei ignoriert werden sollen, müssen mit dem `JsonIgnore` Attribut ausgestattet werden. Dann muss zudem noch in der Methode `CreateCSV`eine Schleife eingefügt werden, die alle Antworten im CSV Format speichert.