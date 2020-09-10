# Intro zu Onyx



## Workflow

1. Patchen von Scheinwerfern

2. Gruppieren von Schweinwerfern (Setup des 2D Visualizers)

3. DMX Werte, FX etc. für Gruppen hinzufügen - *diese werden dem **Programmer** hinzugefügt*

4. Werte aus dem Programmer als **Presets** recorden

2. Gruppen bzw Scheinwerfer auswählen, Presets anwenden/mit **Encodern** FX etc erstellen. Werte aus dem Programmer in **Cuelisten** recorden


## LTP vs HTP

HTP | LTP
----|----
highest takes precednece | latest takes precedence
höchster DMX wert wird gesendet | der zuletzt geämderte DMX wert wird gesendet



## Tracking

Onyx arbeitet als tracking Konsole. Das heißt das in der theorie nur DMX veränderungen gespeichert werden. Der Output einer Cue ist eine Zusammenfassung aller Werte bzw Veränderungen aus der gleichen Cuelist. Dabei ist es egal wann diese Veränderung getroffen wurde.


> Programmer: speichert alle aktiven Attribute und Scheinwerfer die ausgewählt wurden. Attribute die im Programmer gespeichert werden, werden an Schweinwerfer gesendet, egal welceh Cuelisten aktiv sind. 
>
>  Mit der Record Taste (<code>CTR-R</code>) werden Werte aus dem Programmer recorded 
>
>  Mit der Clear Taste (<code>CTRL-DEL</code> mehrmals drücken) werden alle Attribute aus dem Programmer gelöscht 

>Presets: Bausteine die schnelleres erstellen von Cues erlauben. Presets werden immer für alle zur Zeit ausgewählten Scheinwerfer angewendet. Jedes Preset speichert jeweils immer nur eine Information, also eine Farbe, eine Intensität etc. und sind auch unter diesen Kategorien separiert. 


>Cuelisten: "Ordner" die von einer oder mehreren Cues gefüllt sind.

