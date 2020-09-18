# MIDI MACROS

Cuelisten nur über einen Touchscreen bzw. mit der Maus zu triggern ist umständlich und nicht sonderlich schnell. Besonders bei Veranstaltungen wie Partys bei denen man wenig Vorprogrammierten kann. Für solche Fälle kann man Cuelisten auch per Midi Controller triggern. 

Bei Midi Controllern gibt es zwei Unterschide, generische von AKAI, Novation etc und Onyx eigene Wings wie das NX Wing oder das NX Touch. NX Wing und NX Touch funktionieren zwar auch über das Midi Protokoll allerdings sind diese Plug and Play. Wir behandeln hier Generische Midi Controller. 

Für Beispielzwecke benutze ich ein AKAI LPD8 und ein DIY Midi Controller, man kann alles allerings analog auch auf andere übertragen. 

### Limitationen

Ohne externe Software ermöglicht Onyx uns nur das Triggern, Releasen und Flashen von Cuelisten. Es ist nicht möglich den fader einer Cuelsit mit einem Midi fader zu kontrollieren. Das geht nur mit einem Programm ShowCockpit oder via TouchOSC und einem Tablet. 

Eine weiter Limitation ist das Onyx keine Midi Signale ausgibt. Das klingt zuerst nicht weiter wichtig, heißt allerdings das Status LEDs, die am Midi Controller eingebaut sind, nicht auf den Status einer Cuelist reagieren können. (Auch das geht nur mit ShowCockpit)

### Grundlagen von MIDI

Midi steht für **Musical Instrument Digital Interface** und ist eigentlich ein Protokoll für den Austausch von Informationen zwischen elektronischen Instrumenten. Allerdings kann man genau diese Informationen auch benutzen um bestimmte Aktionen in Programmen zu triggern. Ein MIDI Signal besteht aus verschieden Teilen, allerdings brauchen wir nicht alle in Onyx. Was bei einem Tastendruck eines MIDI Controllers übertragen wird lässt sich am einfachsten mit einem Programm wie MIDI-OX anzeigen.

Folgende Bestandteile eines MIDI Events gibt es: 

| Teil                          | Erklährung                                                   |
| ----------------------------- | ------------------------------------------------------------ |
| Timestamp                     | Irrelevant für Onyx                                          |
| Event Type (In Onyx: Message) | Es gibt verschiedene Event Types, Note-On, Note-Off etc, gleich mehr dazu |
| In                            | Irrelevant für Onyx                                          |
| Port                          | Irrelevant für Onyx                                          |
| Status                        | Irrelevant für Onyx                                          |
| Data1                         | Erstes Datenfeld                                             |
| Data2                         | Zweites Datenfeld                                            |
| Channel                       | Der Channel des jeweiligen Knopfes etc. Durch verschieden Channels lassen sich verschiedene Midi Signale über den gleichen Knopf senden |
| Note                          | Die ursprüngliche Note des Midi Signals; Irrelevant für Onyx |

(Wer ein wenig erfahrng mit Midi Signalen hat weiß warschienlich das es zusätzlich noch note Velocity gibt. Die meisten Midi Controller die für uns relevant sind senden diese Signal nichtmal mit da es keine Möglichkeit für den Benutzer gibt diesen Wert zu verändern)

Wie man sehen kann ist ein großteil des Midi Standarts für uns komplett egal, dies ist übrigens keine Eigenheit von Onyx sondern bei den meisten Modernen Programmen der Fall. Kaum noch Software hält sich an die ursprüngliche Semantik eines Midi Signals.

Folgende Event Types kann Onyx verarbeiten:

| Event Type      | Erklährung                                                   |
| --------------- | ------------------------------------------------------------ |
| Note-On         | Wird gesendet sobald ein Knopf gedrückt wird                 |
| Note-Off        | Wird (bei den meisten Midi Controllern) automatisch gesendet sobald der Knopf losgelassen wird. Ein Tastendruck besteht also immer aus einem Note-on und einem Note-Off Event. |
| Key-After       | Irrelevant für Onyx                                          |
| Ctrl-Change     | Wird mit CC abgekürzt, ändert den Zustand des angeschloseenen Controllers. kann aber auch die Art Signal sein die gesendet wird wenn ein Potentiometer/fader bedient wird |
| Programm Change | Irrelevant für Onyx                                          |
| Channel After   | Irrelevant für Onyx                                          |
| Pitch           | Irrelevant für Onyx                                          |

Der einzige wirklich wichtige Event Type für uns ist allerdings Note- On und Note-Off. 

### MIDI in ONYX

Zuerst sollte man sich sicher sein das der Midi Controller auhc von Onyx erkannt wird.

