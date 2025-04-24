# TaskFire  
Ein To-do-Tool, mit dem du mehrere Boards erstellen kannst. Jedes Board kann Unter-Boards mit eigenen Aufgaben und Kategorien haben. Wenn eine Aufgabe ausgelöst wird, „steigt“ sie bis zum Master-Board auf. Alles wird lokal auf deiner Festplatte gespeichert.

[Readme English](https://github.com/FCUnlimited/TaskFire/blob/main/readmeEN.md)
---

## Die Hauptansicht  
**Gesamtübersicht**  
![grafik](https://github.com/user-attachments/assets/499ae332-4547-44e6-af34-65b1a16c9b42)

---

### Boards  
![grafik](https://github.com/user-attachments/assets/01d2432c-43ce-4522-a0f6-20f9335ee7f9)

#### Menü  
Oben siehst du ein Menü, mit dem du zwischen folgenden Ansichten wechseln kannst:
- Board-Ansicht  
- Einstellungen  

#### Board-Panel  
Direkt darunter sind die Boards aufgelistet – in diesem Beispiel aus zwei unterschiedlichen, lokal gespeicherten Datenbanken.  
Aufgaben, die auf einem Unter-Board „Feuer fangen“, steigen bis zum übergeordneten Board auf, das sie löschen kann.  
Wenn eine Aufgabe auslöst, zeigt das Board eine blaue Zahl an, die angibt, wie viele neue Aufgaben aktiv sind.

#### Board-Menü  
Der linke Button öffnet den Board-Editor, in dem du Kategorien und weitere Dinge hinzufügen kannst.  
Unter dem Board-Panel kannst du ein Board zu einer Datenbank deiner Wahl hinzufügen.  
Jeder Button zeigt einen Tooltip, wenn du mit der Maus darüberfährst.

---

### Tag-Editor  
![grafik](https://github.com/user-attachments/assets/f3ce61a9-bd75-4a86-9d64-107d27bb0545)

#### Unteraufgaben  
Direkt unter dem Titel kannst du Unteraufgaben hinzufügen.  
Abgeschlossene Unteraufgaben werden automatisch ausgeblendet.  
Wenn du am Anfang einer Unteraufgabe `#rd`, `#bu`, `#ye` oder `#gn` schreibst, wird sie entsprechend eingefärbt.

#### Tags  
Tag-Kategorien kannst du im Tag-Editor definieren.  
Die Tag-Kategorie bestimmt die Farbe des Tags.  
![grafik](https://github.com/user-attachments/assets/01bd8b69-7aa2-46ca-873f-5b09c1d8e90c)  
Es werden auch Tags vorgeschlagen, die in anderen Aufgaben bereits verwendet wurden.  
Wenn ein Tag nicht mehr verwendet wird, verschwindet er automatisch aus der Liste.

#### Priorität  
Die Priorität bestimmt die Position in der Aufgabenliste und die Farbe des Rahmens.

#### Alarmzeit  
![grafik](https://github.com/user-attachments/assets/983560c0-832b-4520-9f38-8ff7091ab022)  
Hier kannst du festlegen, wann eine Aufgabe „Feuer fängt“.  
Wenn das passiert und die Aufgabe im Master-Board erscheint, kannst du einfach mehr Zeit hinzufügen und sie zurück zum ursprünglichen Board schicken.  
Außerdem erscheint ein Benachrichtigungssymbol in der Taskleiste, das dir zeigt, wie viele neue Aufgaben seit dem letzten Check aktiv wurden.

#### Notizen  
Ein einfaches Notizfeld und darunter ein Link-Bereich.  
Wenn du einen Screenshot machst, eine URL oder Datei kopierst – gib einfach einen Namen ein und drücke Enter. Es wird automatisch gespeichert.  
Ich nutze z. B. ein Makro in Outlook, um einen Link zu einer Mail zu generieren.

#### Links  
Unter dem Notizfeld befindet sich eine Liste mit Links.  
Du kannst einfach irgendeine URL oder sogar einen Screenshot einfügen, einen Namen schreiben – und voilà: ein Link.

---

### Aufgabenliste  
![grafik](https://github.com/user-attachments/assets/9a7a189c-f7a0-40d7-a343-296147a35909)  
Hier siehst du die Aufgaben, die zu diesem Board gehören oder von einem Unter-Board hochgekommen sind.  
- Das durchgestrichene Alarmsymbol zeigt an, dass kein Alarm gesetzt ist – die Aufgabe wird dich also nicht erinnern.  
- Die Flamme zeigt, ob die Aufgabe aktiv ist. Wenn ja, wird sie rot dargestellt.  
- Es kann auch eine blaue Sirene geben, die sichtbar wird, wenn die Aufgabe gerade neu erschienen ist und du sie noch nicht angeklickt hast.
- Oben rechts ist eine Lupe worüber sich die Suche aktivieren lässt für das jeweilige Board und Unterboards.

---

## Weitere coole Features

- Deine Daten bleiben deine Daten – kein Server, kein Risiko  
- Automatische Update-Funktion  
- Synchronisation zwischen mehreren Geräten über deine bevorzugte Dateifreigabe-Software wie Dropbox, SharePoint oder mein Favorit: **Syncthing**  
- Erstellt mit der Power von **AvaloniaUI** – eine Mobile-App ist also nur eine Frage der Zeit  

---

## Danke an

- [AvaloniaUI](https://avaloniaui.net/)  
- [ReactiveUI](https://www.reactiveui.net/)  
- [Projektanker/Icons](https://github.com/Projektanker/Icons.Avalonia)  
- [LiteDB](https://www.litedb.org/)  
- [Velopack](https://velopack.io/)  

---

Wenn du willst, kann ich dir daraus auch eine hübsche README.md machen oder das in eine Avalonia-Hilfe-Seite packen. Sag einfach Bescheid!