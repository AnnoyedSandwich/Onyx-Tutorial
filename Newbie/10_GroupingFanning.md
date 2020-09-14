---

---

# Grouping Tools und Fan/Fx

Das Grouping Tool ist eine einfache und effiziente Möglichkeit seine ausgewählten Fixtures in Untergruppen zu unterteilen. Das ermöglicht (auch in Verbindung mit Fan/FX) sehr interessante Stage Looks die nicht viel zeit in Anspruch nehmen. 

MIt den `Next`/`Last` Tasten auf dem CommandPad kann man schnell zwischen den Fixture Untergeuppen wechseln. Zur Erinnerung, Aktive Fixtures werden im 2D-Plan (bzw. im Grouping Tab der Channel Visualization) hellgrün bzw. rot umrandet. Inaktive dagegen dunkelgrün

Das Grouping Tool findet man am oberen Rand des 2D-Plans und auch als View in der Sidebar.

Das Grouping Tool zu benutzen ist sehr einfach:

```
>> Fixtures auswählen >> Grouping Tool öffnen >> Mode auswählen >> Mask Value einstellen >> Fan/Fx und Actions auswählen
```

Aufgrund der Einfachheit macht es Sin sich verschiedene Kombinationen der Modifier auszuprobieren. Je mehr man es benutzt desto mehr Usecases findet man.

![Grouping](Pics/10_grouping.png)

### Mode

| Option   | Erklährung                                                   |
| -------- | ------------------------------------------------------------ |
| `OFF`    | Schaltet das Grouping Tool aus                               |
| `Every`  | Wählt jede X-te Fixture aus                                  |
| `Block`  | Wählt immer x Fixtures am Stück aus                          |
| `Divide` | Teilt die Anzahl der Fixtures durch X                        |
| `Mirror` | Spiegelt die Fixtures von außen nach innen wobei X die Anzahl der aktiven Fixtures ist. Wenn X=2 werden die äußersten 2 Fixtures aktiv. |
| `Group`  | Wenn mehrere Groups an Fixtures ausgewählt werden kann man automatisch mit  `Next/Last` zwischen diesen wechslen (der Mak Value hat hier keine Funktion) |

### Mask Value

Mit dem Mask Value lässt sich die Anzahl der aktiven Fixtures einstellen. Die genau Wirkung hängt dabei vom ausgewählten Mode ab.

### Fan/Fx

Ermöglicht dem Fanning Tool nicht nur die aktiven Fixtures zu beeinflussen sondern alle. Was das genau heißt kommt im nächsten Abschnitt

### Actions

Ermöglicht weiter Modifikation zur vorher getroffenen Wahl bzw. zur Reihenfolge der Fixtures. Wichtig dabei zu wissen ist folgendes:

## Die Reihenfolge in der Effekte etc. durch die Fixtures laufen wird nicht durch die ID Nummer o.A. bestimmt sondern die Reihenfolge in der sie Ausgewählt werden. Dabei zeigt die Rot umrandete Fixture immer die zu Letzt ausgewählte Fixture an. Um die Riehe folge zu kontrollieren in der Channel Visualization im Reiter Grouping nachgucken. Die Reihenfolge der Auswahl wird auch in Groups recorded.

| Option        | Erklähurng                                                   |
| ------------- | ------------------------------------------------------------ |
| `REVERT`      | Geht zur ursprüchglich ausgewählten Reihenfolge zurück sollten Veränderungen an dieser vorgenommen sein |
| ` INVERT`     | Äquivalent zu: `/` `ENTER`. Wen gedrückt werden die zuvor aktiven Fixtures inaktiv und die inaktiven aktiv |
| `INVERT MASK` | Hat eine ähnliche Funktion wie `INVERT`                      |
| `RANDOM`      | Die Reihenfolge der ausgewählten Fixtures wird zufällig. Durch mehrmaliges drücken verändert sich die Reihenfolge immer |
| `REVERSE`     | Dreht die Reihenfolge der ausgewählten Fixtures um           |
| `SORT`        | Sortiert die ausgewählten Fixtures bei ihrer ID Nummer.      |

### Masks

Um noch mehr Zeit zu sparen können auch vorgefertigte Mode und Mask Value Kombis ausgewählt werden.

Wichtig: Genauso wie die Reihenfolge der ausgewählten Fixtures in Groups recorded wird können Masks recorded werden. Im Onyx Manual werden diese fast Select genannt. Fast Select Groups hbaen recht oben in der ecke jeweils einen Buchstaben und eine Zahl. Der Buchstabe sthet hierbei für den Mode, die Zahl für den Mask Value

![FastSelect](Pics/10_fastSelect.PNG)

In diesem Beispiel wurde der `MIRROR` Mode und ein Mask Value von 4 gewählt.
