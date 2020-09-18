# Cuelist Values und Move in Black

Im View `Cuelist Values` können veränderungen an Cuelists vorgenommen werden, Timings geändert werden, (MIDI)-Macros eingestellt werden etc. 

Eine weiter Wichtige Funktion des Cuelist Values VIews ist die Funktion Move In Black. 

### Cuelist Values

Wie bereits erwähnt muss man um z.B die Timings einer Cue zu bearbeiten die entsprechende Cue auswählne und dann in der Sidebar auf Cuelist-Values drücken. Alleridngs kann man dort auch noch mehr als nur Fade Times einstellen:

Auf der Linken Seite gibt es die Möglichkeit die Cue zu bearbeiten, auf der rechten Seite kann man sehen was in den einzelnen Cues recorded ist.

Fangen wir  mit der linken Seite an:

![CLL](Pics/12_CLValuesL.PNG)

Dieses Fenster wird auch `Selected Cuelist Window gennant` und kann unter diesem Namen im View Editor gefunden werden.

Die Knöpfe am oberen Rand haben folgende Funktionen:

| Option                        | Erklährung                                                   |
| ----------------------------- | ------------------------------------------------------------ |
| `OPTIONS`                     | eine weiter Möglichkeit die Optionen einer Cuelist zu öffnen |
| `FOLLOW VALUES ` (default On) | Alle drei Einstellungen verändern das Verhalten des Cuelist values Views. Sie haben keien Einfluss auf die Cuelist. |
| `FOLLOW CUE` (default On)     |                                                              |
| `FOLLOW GRIND` (default On)   |                                                              |
| `ADD MACRO`                   | Fügt ein Macro an der Cue hinzu die ausgewählt wurde. Im Kapitel Macros dazu mehr |
| `INSERT LINK`                 | Fügt einen Cuelist Link hinzu an der Cue die ausgewählt wurde. Im Kapitel Macros dazu mehr |
| `MARK TOGGLE`                 | Aktiviert bzw deaktiviert Move In Black                      |
| `RENUMBER`                    | Ermöglicht es die Position einer ausgewählten Cue in der Cuelist zu verändern. |
| `EDIT MODE`                   | Ermöglicht zugriff auf `ADD MACRO; INSERT LINK; NAME; TRIGGER; DELAY; FADE; FADE MODE; PATH; COMMENT` |
| `PRE-SELECT FOR NEXT GO`      | wenn aktiviert wird der nächste `GO ` Befehl nicht die nächste Cue in der Cuelist auslösen sondern die im Cuelist Values View ausgewählte Cue. Die Cue wird in dem falle über die Nummer ausgewählt. |

Will man den Namen der Cuelist ändern:

```
>> Edit Mode >> auf den aktuellen Namen klicken >> neuen Namen wählen >> Enter drücken
```

Unter den grade besprochenen Knöpfen sind 8 Spalten:

| Option                         | Erklähurng                                                   |
| ------------------------------ | ------------------------------------------------------------ |
| `NO`                           | Die Nummer der Cue. Kann geändert werden wenn `RENUMBER` aktiviert ist |
| `NAME`                         | Der Name der Cue.                                            |
| `TRIGGER`                      | Die Trigger Typen `GO: WAIT: FOLLOW` können hier ausgewählt werden. Weiter unten dazu mehr |
| `DELAY`                        | Delay Timing, die Zeit die gewartet wird bevor die nächste Cue eingefaded wird |
| `FADE`                         | Die fade Time                                                |
| `FADE MODE`                    | Es gibt drei verschiedene fade Modi                          |
| `FADE MODE::DEFAULT FADE`      | Alle Attribute werden so eingefaded wie sie recorded wurden  |
| `FADE MODE::SNAP ALL CHANNELS` | Alle Attribute haben eine Fade Time von 0, rercordete Fade times werden überschrieben |
| `FADE MODE::FADE ALL CHANNELS` | Alle Attribute werden mit der recordeten fade Time eingefadet, auch Attribute die normalerweise snappen |
| `PATH`                         | Der `PATH` ist der Style in der der fade erfolgt             |
| `PATH::LINEAR` (default)       | Der Fade hat über die komplette Zeit eine gleichbleibende Geschwindigkeit |
| `PATH::ACCELERATE`             | Die Geschwindigkeit startet langsam und wird immer schneller |
| `PATH::BREAK`                  | Die Geschwindigkeit startet schnell und wird immer langsamer |
| `PATH::ACCELERATE-BREAK`       | Geschwindigkeit startet langsam, wird schneller und dann wieder langsamer |
| `PATH::SHAKE`                  | Die Geschwindigkeit ändert sich konstant                     |
| `COMMENT`                      | Ermöglicht es einen Comment mit max. 21 Zeichen hinzuzufügen |



Die Rechte Seite sieht folgendermaßen aus:

![CLR](Pics/12_CLValuesR.PNG)

In diesem Fenster sieht man was alles in der grade ausgewählten bzw. grade aktuellen Cue gespeichert ist. Über die Knöpfe `SHOW FX` `SHOW TIMTING` und `SHOW TRACKED` kann man noch auswählen was alles angezeigt werden soll. Rechts oben kann man wie im Programmer auch wechseln ob er die Preset Namen oder die Attribut-Werte zeigen soll.

### MARK oder Move in Black

Move in Black (in Onyx MARK genannt) bedeute das Onyx manche Attributs Änderungen automatisch vornimmt. Zum Beispiel kann eine Pan Tilt Position erreicht werden noch bevor die Scheinwerfer angehen. Um MARK zu benutzen muss in der Cuelist ein Intensity Wert recorded sein. Dieser kann auch getracked sein. Sobald der Intensity Wert 0% hat wird das MARK ausgeführt.

