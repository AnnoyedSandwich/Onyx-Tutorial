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

### Tracking Beispiel

| Cue  | Int  | Pan     | Tilt | Red  | Green | Blue |
| ---- | ---- | ------- | ---- | ---- | ----- | ---- |
| 1    | 100% | 50%     | 28%  | 100% | 0%    | 0%   |
| 2    |      |         |      | 0%   | 100%  | 100% |
| 3    | 5%   |         |      |      |       |      |
| 4    |      | 62%-38% | 28%  |      |       |      |

