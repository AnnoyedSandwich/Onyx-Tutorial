# Playback, mit und ohne Hardware	

Die Playback Möglichkeiten für eine Show hängen stark von den Hardware Möglichkeiten ab. Am Anfang beschränkt sich diese Sektion nur auf Software Playback bzw auf Software Playback in Verbindung mit einem MIDI Controller. Sollte in Zukunft Onyx Hardware zur Verfügung stehen werde ich diese Abschnitt für die Entsprechende Hardware updaten. 

Das meiste hier besprochene sind nur Tipps bzw die Art und Weise wie ich es mache. Meine Art eine Show zu mache ist natürlich auch stark davon beeinflusst wie ich ein Showfile erstelle. Hat jemadn eine anderen Style ein Showfile zu erstellen ist es auch wahrscheinlich das er auch andere Entscheidungen bei den Playback Möglichkeiten trifft. Ich empfehle es jedem verschieden Sachen auszuprobieren. 

### Playback Grundlagen

Wie bereits im Kapitel Cues besrprochen gibt es drei Arten von Playbacks: Main Playback, Sub Playback und Playback Buttons.

Main Playback bietet auf Software Seite 4 Buttons zu jedem Fader. Diese sind per default `GO, Pause/Back, Select, Flash`. Diese lassen sich aber in den Cuelist Options unter dem Reiter `FUNKTION ASSIGNMENT` frei belegen (dazu gleich mehr). 

Sub Playback dagegen bietet nur einen Button. Sub Playbacks finden sich außerdem nur auf der NX4 Konsole.

Playback Buttons sind Software basierte Buttons die per Touchscreen, Mausklick oder MIDI Controller eine Cellist triggern.

### Playback Buttons

Für uns am wichtigsten sind die Playback Buttons. Den entsprechenden View `PLAYBACK BUTTONS` findet man auf der Sidebar. Am oberen Rand des View befinden sich verschieden Knöpfe mit denen man die Playback Buttons triggern, releasen etc kann. Um eine Aktion bei einer Cuelist auszuführen, erst auf die Aktion drücken und danach passiert diese Aktion für alle Cuelistst die man anklickt.



| Aktion                | Erklährung                                                   |
| --------------------- | ------------------------------------------------------------ |
| ![1](Pics/14_1.PNG)   | Custom, wenn aktiviert wird die Down bzw Up Action ausgeführt. Per Default ist diese Go, sie lässt sich allerdings in den Optionen unter `FUNCTION ASSIGNMENTS` ändern. |
| ![2](Pics/14_2.PNG)   | Go, triggert eine Cuelist bzw triggert die nächste Cue.      |
| ![3](Pics/14_3.PNG)   | Pause, pausiert die Fade Time einer fadenden Cue.            |
| ![4](Pics/14_4.PNG)   | Release, released die Cuelist.                               |
| ![5](Pics/14_5.PNG)   | Select, wählt/selected die Cuelist.                          |
| ![6](Pics/14_6.PNG)   | Direct Cuelist Access, ermöglicht es ein Pop-Up zu öffnen mit den gleichen Kontrollmöglichkeiten wie eine Cuelist die bei einer Main Playback Bank gespeichert ist, inkl. Fader. |
| ![7](Pics/14_7.PNG)   | Direct Cue, öffnet ein Popup mit allen Cues die in einer Cuelist enthalten sind. Ermöglicht es direkt zu einer bestimmten Cue zu springen. |
| ![8](Pics/14_8.PNG)   | Multiselect, ermöglicht es mehrere Cuelists auszuwählen um allen gleichzeitig einen `GO` oder `RELEASE` Befehl zu geben. Um diese Funktion zu benutzen erst Mulstiselct auswählen , dann mehrere Cuelsits und dann auf `GO` oder ` RELEASE` drücken. |
| ![9](Pics/14_9.PNG)   | Selection Cuelist, ändert das selection Verhalten wenn eine Cuelist einen Commadn bekommt. **Off**: wenn Go etc. dann wird die Cuelist nicht selectet. **On**: wenn Go etc. dann wird die Cuelist automatisch auch selected. **Chases (CH)**: nur Chases werden bei einem `GO` etc. selected, andere Cuelists nicht. |
| ![10](Pics/14_10.PNG) | Optionen und Page Nummer                                     |

#### Verschieben etc von Cuelisten

Cuelisten können ohne Probleme kopiert, bewegt und "gelöscht" werden (achtung, es wird nur der Button gelöscht, die eigene Cuelist ist immer noch verfügbar)

Um eine Cuelsit zu bewegen: 

```
>> Move (oder Ctrl+M) >> Cuelist die bewegt werden soll >> neuen Ort der Cuelist drücken
```

Um eine Cuelist zu kopieren:

```
>> Copy (oder Ctrl) >> Cuelist die kopiert werden soll >> Ort der Cuelist drücken
```

Um eine Cuelist zu "löschen":

```
>> Delete (oder Ctrl + Shift + Del) >> Cuelist die gelöscht werden soll >> Enter
```

Um eine Cuelist komplett zu löschen:

```
>> Sidebar View "Cuelist Directory" >> Directory Window >> Delete (oder Ctrl + Shift + Del) >> Cuelist die gelöscht werden soll >> Enter
```

### Active Cuelist Window

alle gerade laufende Cuelists lassen sich mit dem Active Cuelsits Window anzeigen. (Im Compose Workspace zu finden im "Cuelist Directory" View)

![AC](Pics/14_ActiveCuelists.PNG)

Die Knöpfe am oberen Rand haben die gleiche Funktion wie die der Playback Buttons. 

Am unteren Rand gibt es die möglichkeit die laufenden Cuelists 