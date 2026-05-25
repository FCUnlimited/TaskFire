# TaskFire Benutzerhandbuch

Dieses Handbuch beschreibt die wichtigsten Arbeitsablaeufe in TaskFire: Boards anlegen, Aufgaben erfassen, Erinnerungen nutzen, Tags und Checkpoints verwenden und Daten lokal synchronisieren.

## 1. Grundidee

TaskFire ist ein lokales Aufgabenwerkzeug mit mehreren Boards. Ein Board kann Unter-Boards enthalten. Aufgaben gehoeren zuerst zu einem Ursprungs-Board. Wenn eine Aufgabe faellig wird oder manuell auf "Feuer" gesetzt wird, erscheint sie auch auf dem uebergeordneten Board, damit sie dort sichtbar wird.

Typischer Ablauf:

1. Du sammelst Aufgaben auf thematischen Boards, zum Beispiel `Office`, `Privat` oder `Projekt X`.
2. Du gibst Aufgaben bei Bedarf eine Erinnerungszeit.
3. Faellige Aufgaben steigen im Board-Baum nach oben und werden als aktive Aufgaben sichtbar.
4. Du bearbeitest die Aufgabe, verschiebst die Erinnerung oder sendest sie zurueck in eine passende Kategorie.

Alle Daten liegen lokal auf deinem Geraet. TaskFire kann mehrere lokale Datenbanken einbinden, zum Beispiel in einem Sync-Ordner von Syncthing, Dropbox oder SharePoint.

## 2. Hauptansicht

Die Hauptansicht besteht aus mehreren Bereichen:

- **Boards**: links die Board-Struktur mit Haupt- und Unter-Boards.
- **Tasks**: die Aufgabenliste des aktuell gewaehlten Boards.
- **Editor**: erscheint, wenn eine Aufgabe ausgewaehlt wird.
- **Tags**: Ansicht fuer Checkpoints und Aufgaben nach Tag-Kategorien.
- **Board Editor**: Verwaltung von Boards und Kategorien.
- **Tag Editor**: Verwaltung der Tag-Kategorien.
- **Settings**: lokale Einstellungen und Datenbankpfade.

Welche Bereiche sichtbar sind, haengt von der ausgewaehlten Ansicht und der aktuellen Auswahl ab.

## 3. Boards verwenden

Boards strukturieren deine Aufgaben. Ein Haupt-Board kann Unter-Boards haben. Aufgaben auf Unter-Boards koennen bei Faelligkeit auf uebergeordnete Boards "hochfeuern".

### Board auswaehlen

Klicke links in der Board-Liste auf ein Board. Die Aufgabenliste zeigt dann:

- Aufgaben, die direkt zu diesem Board gehoeren.
- Aufgaben aus Unter-Boards, wenn sie auf Feuer sind.
- Aufgaben passend zum aktiven Kategorie-Filter.

Eine blaue Zahl neben einem Board zeigt an, wie viele neue faellige Aufgaben dort angekommen sind.

### Kategorien auf Boards

Jedes Board hat Kategorien. Kategorien dienen als einfache Spalten oder Arbeitsbereiche innerhalb eines Boards, zum Beispiel:

- `Backlog`
- `Heute`
- `Warten`
- `Erledigen`

In der Aufgabenliste erscheinen die Kategorien als Filterbuttons. Ein Klick aktiviert eine Kategorie, ein weiterer Klick deaktiviert den Filter wieder. Die rote Zahl an einer Kategorie zeigt Aufgaben ohne gesetzte Erinnerung in dieser Kategorie an.

### Board Editor

Im Bereich **Board Editor** kannst du Boards bearbeiten. Dort lassen sich unter anderem:

- Name und Beschreibung eines Boards aendern.
- Kategorien hinzufuegen.
- Kategorien entfernen, solange keine Aufgabe mehr in dieser Kategorie liegt.
- Die Reihenfolge von Boards per Drag-and-drop anpassen.
- Boards als Haupt- oder Unter-Board organisieren.

Eine Kategorie kann nicht geloescht werden, wenn noch mindestens eine Aufgabe darin liegt oder wenn sie als Rueckkehr-/Loeschkategorie des Boards verwendet wird.

## 4. Aufgaben anlegen

1. Waehle links ein Board aus.
2. Schreibe oben in das Feld **New Task** den Titel der Aufgabe.
3. Bestaetige die Eingabe, um die Aufgabe anzulegen.

Wenn gerade ein Kategorie-Filter aktiv ist, wird die neue Aufgabe dieser Kategorie zugeordnet. Andernfalls landet sie in der Standardkategorie des Boards.

Nach dem Anlegen wird die Aufgabe ausgewaehlt und im Editor geoeffnet.

## 5. Aufgabenliste lesen

Eine Aufgabe in der Liste zeigt mehrere Informationen:

- **Titel**: Name der Aufgabe.
- **Rahmenfarbe**: Prioritaet der Aufgabe.
- **Kategorie**: aktuelle Board-Kategorie der Aufgabe.
- **Tags**: farbige Kennzeichnungen aus Checkpoints.
- **Flamme**: Aufgabe ist aktiv beziehungsweise "auf Feuer".
- **Durchgestrichener Alarm**: es ist keine Erinnerung gesetzt.
- **Blaue Alarmleuchte**: die Aufgabe ist neu faellig geworden und wurde seitdem noch nicht geoeffnet.
- **Sync-Warnung**: es gibt eine Konflikt- oder Abweichungsversion aus der Synchronisation.

Mit dem Flammen-Button kannst du den Feuer-Status einer Aufgabe manuell umschalten.

## 6. Aufgabe bearbeiten

Waehle eine Aufgabe in der Aufgabenliste aus. Der Editor oeffnet sich mit den wichtigsten Feldern:

- **Titel**: Name der Aufgabe.
- **Checkpoints**: einzelne Arbeitsschritte oder Tags.
- **Prioritaet**: `None`, `Low`, `Middle`, `High`.
- **Erinnerung**: Datum und Uhrzeit, zu der die Aufgabe faellig wird.
- **Kategorie**: Kategorie innerhalb des aktuellen Boards.
- **Notizen**: freies Textfeld.
- **Links**: Dateien, URLs oder aus der Zwischenablage gespeicherte Anlagen.

Unten im Editor findest du Aktionen zum Schliessen, Verschieben und Loeschen der Aufgabe.

### Prioritaet setzen

Die Prioritaet beeinflusst die Sortierung in der Aufgabenliste. Hoehere Prioritaeten erscheinen weiter oben. Die Prioritaet wird ausserdem ueber die Rahmenfarbe sichtbar.

### Aufgabe verschieben

Mit dem Verschieben-Button kannst du eine Aufgabe auf ein anderes Board verschieben. Wenn das Ziel-Board in einer anderen Datenbank liegt, wird die Aufgabe in diese Datenbank uebernommen.

### Aufgabe loeschen

Der Loesch-Button entfernt die Aufgabe aus dem aktuellen Board. Je nach Datenstand kann sie als geloescht markiert beziehungsweise aus der lokalen Datenbank entfernt werden.

## 7. Erinnerungen und "Feuer"

TaskFire benutzt Erinnerungen, um Aufgaben zur richtigen Zeit sichtbar zu machen.

### Erinnerung setzen

Im Editor kannst du ein Datum und eine Uhrzeit setzen. Zusaetzlich gibt es Schnellbuttons:

- **Now**: setzt die Erinnerung auf heute um 08:00 Uhr.
- **+4h**: verschiebt die Erinnerung um 4 Stunden.
- **+1d**: verschiebt die Erinnerung um 1 Tag.
- **+1w**: verschiebt die Erinnerung um 1 Woche.
- **+1M**: verschiebt die Erinnerung um 1 Monat.

Wenn die Erinnerungszeit erreicht ist, wird die Aufgabe auf Feuer gesetzt und erscheint auf dem uebergeordneten Board. Der Taskleistenzaehler zeigt neue faellige Aufgaben an.

### Aufgabe zuruecksenden

Wenn eine Aufgabe aus einem Unter-Board auf einem uebergeordneten Board erscheint, zeigt der Editor passende Rueckkehr-Kategorien an. Mit einem Klick sendest du die Aufgabe zurueck in die Ursprungskategorie und loeschst den Feuer-Status.

Das ist praktisch fuer Aufgaben, die du spaeter wieder sehen moechtest: Erinnerung verlaengern, passende Kategorie waehlen, zurueckschicken.

## 8. Checkpoints und Tags

Checkpoints sind einzelne Punkte innerhalb einer Aufgabe. Sie koennen normale Unteraufgaben sein oder als Tags dienen.

### Checkpoint anlegen

1. Oeffne eine Aufgabe.
2. Fuege im Checkpoint-Bereich einen neuen Punkt hinzu.
3. Schreibe den Text.
4. Bestaetige mit Enter oder beende die Bearbeitung mit Escape.

Abgehakte Checkpoints werden standardmaessig ausgeblendet. Mit dem Checkpoint-Button **ShowAll** kannst du erledigte Punkte wieder einblenden, wenn erledigte Checkpoints vorhanden sind.

### Tags ueber Checkpoints

Ein Checkpoint wird zum Tag, wenn er mit dem Prefix einer Tag-Kategorie beginnt. Beispiele:

- `#rd Wichtig`
- `#bu Kunde A`
- `#ye Rueckfrage`
- `#gn Privat`

Der Prefix wird im **Tag Editor** definiert. Die Tag-Kategorie bestimmt die Farbe. Wenn nach dem Tag noch Text folgt, bleibt dieser als Checkpoint-Text sichtbar. Wenn nur das Tag selbst eingetragen wird, wird es als reines Tag angezeigt.

Tags werden automatisch aus den vorhandenen Aufgaben gesammelt. Wenn kein aktiver Checkpoint ein Tag mehr verwendet, verschwindet es aus der Vorschlags- beziehungsweise Tag-Liste.

### Tag Editor

Im Bereich **Tag Editor** verwaltest du Tag-Kategorien pro Datenbank:

- Name der Kategorie.
- Prefix, der im Checkpoint erkannt wird.
- Farbe des Tags.
- Reihenfolge der Kategorien.

Tags gelten innerhalb der Datenbank, in der die Aufgabe gespeichert ist.

## 9. Tag-Ansicht

Die Ansicht **Tags** zeigt Datenbanken, Tag-Kategorien und darunter die verwendeten Tags. Wenn du eine Kategorie oder ein einzelnes Tag auswaehlst, zeigt TaskFire die passenden offenen Checkpoints beziehungsweise Aufgaben.

Diese Ansicht ist hilfreich, wenn du nicht nach Board, sondern nach Thema arbeiten willst, zum Beispiel nach Kunde, Kontext oder Projektphase.

## 10. Suche

In der Aufgabenliste befindet sich rechts oben ein Lupen-Button.

Wenn die Suche aktiv ist:

- Das Eingabefeld wechselt von **New Task** zu **Search**.
- TaskFire sucht im aktuellen Board und in Unter-Boards.
- Gesucht wird im Aufgabentitel, in Notizen und in Checkpoints.

Wenn die Suche deaktiviert ist, dient das Feld wieder zum Erstellen neuer Aufgaben.

## 11. Links und Anlagen

Im Editor gibt es unter den Notizen ein Feld fuer Links und Anlagen.

So legst du einen Link oder eine Anlage an:

1. Kopiere eine URL, einen Dateipfad, eine Datei oder einen Screenshot in die Zwischenablage.
2. Schreibe im Link-Feld einen Namen.
3. Bestaetige mit Enter.

TaskFire speichert den Inhalt aus der Zwischenablage als Link oder Datei. Dateien werden in einem `Attachments`-Ordner neben der jeweiligen Datenbank abgelegt. Ein Klick auf den Link oeffnet die gespeicherte Adresse oder Datei mit dem Betriebssystem.

## 12. Synchronisation und Datenhaltung

TaskFire speichert Daten lokal in LiteDB-Datenbanken. Beim ersten Start wird eine Standarddatenbank angelegt. Weitere Datenbanken koennen in den Einstellungen eingebunden werden.

Fuer die Synchronisation zwischen Geraeten empfiehlt sich ein lokaler Sync-Ordner, zum Beispiel:

- Syncthing
- Dropbox
- SharePoint
- OneDrive

TaskFire prueft die Daten regelmaessig und synchronisiert eingebundene Datenbanken. Wenn mehrere Geraete dieselbe Aufgabe veraendern, kann eine Sync-Warnung erscheinen. Im Editor kannst du dann eine Version auswaehlen und als korrekte Version uebernehmen.

Hinweis: Vermeide es, dieselbe Aufgabe gleichzeitig auf mehreren Geraeten zu bearbeiten. Das reduziert Konflikte deutlich.

## 13. Einstellungen

Im Bereich **Settings** findest du lokale Einstellungen, unter anderem:

- eingebundene Datenbankpfade.
- geraetespezifische Einstellungen.
- Breite des Editors.
- weitere Anwendungseinstellungen aus dem FCTools/Avalonia-Framework.

Aenderungen an Aufgaben, Boards, Kategorien und Tags werden automatisch gespeichert.

## 14. Praktische Arbeitsweise

Eine einfache Routine sieht so aus:

1. Sammle neue Aufgaben im passenden Board.
2. Setze eine Kategorie und bei Bedarf eine Prioritaet.
3. Zerlege groessere Aufgaben in Checkpoints.
4. Setze Tags fuer Kontext, Kunde oder Thema.
5. Gib Aufgaben eine Erinnerung, wenn sie spaeter wieder auftauchen sollen.
6. Arbeite im Haupt-Board die neu angekommenen Aufgaben ab.
7. Verlaengere, verschiebe oder sende Aufgaben zurueck, wenn sie noch nicht dran sind.

So bleibt das Haupt-Board schlank, waehrend Unter-Boards als Speicher fuer spaetere oder kontextbezogene Aufgaben dienen.

## 15. Begriffsklaerung

| Begriff | Bedeutung |
| --- | --- |
| Board | Bereich oder Liste fuer Aufgaben |
| Unter-Board | Board unterhalb eines anderen Boards |
| Aufgabe / Todo | Konkreter Eintrag, der bearbeitet werden soll |
| Kategorie | Filter oder Arbeitsbereich innerhalb eines Boards |
| Checkpoint | Unteraufgabe oder einzelner Arbeitsschritt |
| Tag | Checkpoint mit erkanntem Prefix und Farbe |
| Feuer / On Fire | Aufgabe ist aktiv/faellig und wird nach oben sichtbar |
| Just Arrived | Aufgabe ist neu faellig geworden und wurde noch nicht geoeffnet |
| Datenbank | Lokale Datei, in der Boards, Aufgaben und Tags gespeichert werden |

