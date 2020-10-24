# Cue Macros

Mit Macros kann man automatisiert bestimmte Cues/Cuelists triggern. Macros werden dabie zu einer bestimmten Cue hinzugefügt und getriggert sobald diese Cue getriggert wird. Offiziell lassen sich Macros nur zu normalen Cuelisten und Timecode Cuelisten hinzufügen allerdings gibt es einen Bug der es zumindest auf dieser Version ermöglicht Macros auch bei Chases zu benutzen. Allerdings nur am Start der Cuelist.

### Macro Typen

Es gibt zur Zeit 18 Macro Typen, allerdings sind nicht alle wirklich sinnvoll oder nutzbar. Den `MIDI MACRO` Typ kennen wir bereits.

| Macro                  | Erklährung                                                   |
| ---------------------- | ------------------------------------------------------------ |
| `TRIGGER`              | Triggert eine zu spezifizierende Cuelist. Gleiche Effekt wie der `GO` Command. |
| `Release`              | Released eine zu spezifizierende Cuelist.                    |
| `Pause`                | Paused eine zu spezifizierende Cuelist.                      |
| `Select`               | Selected eine zu spezifizierende Cuelist.                    |
| `SelectMain`           | Designiert eine eine zu spezifizierende Cuelist als die Main Go Cuelist. Dadurch lässt sie sich durch die Main Go Sektion auf Hardware triggern. |
| `GOTOBANK`             | Wechselt zu einer bestimmten Playback Bank. Es lässt sich auswählen ob der Wechsel nur in der Software oder auch auf Hardware Seite stattfinden soll. (Verschiedene Wings werden per WING ID unterschieden) |
| `GOTOSUBBANK`          | Gleich wie `GOTOBANK` aber bezieht sich auf die Submaster    |
| `SCRIPTEXECUTE`        | Damit werden Skripte aus dem Onyx Manager ausgeführt. (Für uns nicht relevant) |
| `REL ALL`              | Es werden ALLE Cuelisten released. Bietet die Möglichkeit Ausnahmen zu spezifizieren |
| `REL ALL CL`           | Es werden alle Cuelisten außer Overrides released. Bietet die Möglichkeit Ausnahmen zu spezifizieren |
| `REL ALL OR`           | Es werden alle Overrides released. Bietet die Möglichkeit Ausnahmen zu spezifizieren |
| `SET CL VALUE`         | Ändert den INT Wert einer Cuelist                            |
| `MIDI MACRO`           | Ermöglicht MIDI Macros. Wurde [hier](https://github.com/AnnoyedSandwich/Onyx-Tutorial/blob/master/Newbie/MIDI_MACROS.md) schon besprochen. |
| `REL CUELIST`          | Es wird entweder eine oder mehrere aufeinanderfolgender Cuelisten released. Biete auserdem die Möglichkeit die Fade-Out Time zu bestimmen. |
| `RELEASE BANKS`        | Released alle Cuelsiten auf einer bestimmten Playback Bank oder auf allen Inaktiven Banks |
| `RELEASE THIS CUELIST` | Released die Cuelsit zu der das Macro gehöhrt                |
| `External Macro`       | Funktioniert meines Wissens nach mit Showcockpit. Da wir das aber nicht besitzen weil zu teuer ist das für uns eher weniger relevant |
| `TIMECODE`             | Startet, Pausiert oder Stoppt den internen Timecode. Eine Kurzeinführung für Timecode mit Reaper gibt es ~~hier~~ noch nicht |

### Ein Macro zu einer Cuelist hinzufügen

Wie bereits erwähnt werden Macros nur dann getriggert, wenn die Cue zu der sie gehören auch getriggert werden.

```
>> Cuelist selecten >> Selected Cuelist >> Edit Mode >> eine Cue auswählen >> Add Macro
```

Danach wird unter der ausgewählten Cue eine nuee Zeile eingefügt mit den Worten `UNDEFINDED MACRO`. 

![add1](Pics/Macro_add1.PNG)

Um das Macro zu bearbeiten darauf klicken:

![add2](Pics/Macro_add2.PNG)

Über das Drop-Down Menu ein Macro Typ auswählen und danach auf `APPLY` drücken.

### Tipps zu Macros

- Mit Macros können bestimmte Cues innherhalb Cuelisten getriggert werden. Es ist allerdings zu beachten das Onyx dies so betrachtet als würde man durch alle Cuelsiten klicken bis man bei der gewünschten ist. Das heißt das alle bis Werte die bis dahin getracked werden auch in den Output kommen.
- Theoretisch lässt sich dieses Verhalten mit der Option `Retrack all parameters` abschalten, allerdings funktioniert das bei mir nicht wie es soll. Sobald ich eine Antwort vom Support erhalte wird das hier geupdatet. (Außer ich vergesse es, dann pech gehabt)

