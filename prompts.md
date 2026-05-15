# KI-Workflow

Das Repository funktioniert überraschend gut zusammen mit KI-Tools.  
Da die Zeichnungen gleichzeitig Skizze und Maßplan sind, lassen sich daraus oft direkt sinnvolle Informationen ableiten.

Zum Beispiel:

- Materiallisten erzeugen
- Zuschnitt planen
- Maße ergänzen
- Konstruktionen prüfen
- Stückzahlen zusammenfassen
- Dokumentation erzeugen

Einfach die `.drawio`-Datei oder einen Export zusammen mit einem Prompt an ein KI-Tool geben.

## Allgemeiner Starter für eigene Tasks

```text
Analysiere die technische Zeichnung <Name> und führe folgende Aufgabe aus:

<AUFGABE HIER BESCHREIBEN>

Wichtig:

* Verstehe zuerst die gesamte Zeichnung und die dargestellte Konstruktion.
* Die Zeichnung kann mehrere Ansichten enthalten (z. B. Front-, Seiten-, Drauf- oder Schnittansichten).
* Dasselbe Bauteil kann in mehreren Ansichten dargestellt sein und darf nicht doppelt interpretiert werden.
* Analysiere Zusammenhänge zwischen den Ansichten, bevor Schlussfolgerungen gezogen werden.

Technische Hinweise:

* Die Zeichnung ist maßstäblich.
* In der .drawio-Datei entspricht 1 pt genau 1 mm in der Realität.
* Fehlende Maße dürfen geometrisch aus der Zeichnung abgeleitet werden.
* Proportionen und Abstände der Zeichnung sind verbindlich.
* Falls explizite Maße und gezeichnete Abstände voneinander abweichen, haben explizit angegebene Maße Vorrang.
* Nutze Objektpositionen und Objektgrößen der .drawio-Datei zur direkten Maßermittlung.

Anforderungen:

* Arbeite technisch konsistent und nachvollziehbar.
* Verwende realistische technische Annahmen, falls Informationen fehlen.
* Kennzeichne geschätzte oder unsichere Werte eindeutig.
* Verändere keine vorhandenen Maße oder Konstruktionen ohne Begründung.
* Behalte bestehende Geometrien und Proportionen bei.

Ausgabe:

<GEWÜNSCHTES AUSGABEFORMAT HIER BESCHREIBEN>
```

## Beispiel: Materialliste erzeugen

```text
Analysiere die technische Zeichnung <Name> und erstelle daraus eine vollständige Materialliste.

Wichtig:

* Verstehe zuerst die gesamte Zeichnung und die dargestellte Konstruktion.
* Die Zeichnung kann mehrere Ansichten enthalten (z. B. Front-, Seiten-, Drauf- oder Schnittansichten).
* Dasselbe Bauteil kann in mehreren Ansichten dargestellt sein und darf nur einmal gezählt werden.
* Berücksichtige Zusammenhänge zwischen den Ansichten, um doppelte Erfassung zu vermeiden.

Technische Hinweise:

* Die Zeichnung ist maßstäblich.
* In der .drawio-Datei entspricht 1 pt genau 1 mm in der Realität.
* Fehlende Maße dürfen direkt aus der Zeichnung geometrisch abgeleitet werden.
* Proportionen und Abstände der Zeichnung sind verbindlich.
* Falls explizite Maße und gezeichnete Abstände voneinander abweichen, haben explizit angegebene Maße Vorrang.

Erstelle die Materialliste unter Berücksichtigung von:

* allen Holzteilen
* Maßen in mm (Länge × Breite × Stärke)
* Stückzahlen
* Zusammenfassung identischer Teile
* geschätzter Materialstärke, falls diese nicht eindeutig angegeben ist
* plausibler Interpretation unvollständiger Maße

Gib das Ergebnis als übersichtliche Tabelle aus.

Die Tabelle soll folgende Spalten enthalten:
| Pos. | Bauteil | Länge (mm) | Breite (mm) | Stärke (mm) | Stückzahl | Bemerkung |

Falls Maße oder Materialstärken nicht eindeutig erkennbar sind:

* realistische technische Schätzwerte verwenden
* unsichere Werte in der Bemerkung kennzeichnen.

```

## Beispiel: Maße ergänzen

```text
Analysiere die technische Zeichnung <Name> und ergänze fehlende Maße sinnvoll im .drawio-Format.

Wichtig:

* Verstehe zuerst die gesamte Zeichnung und die dargestellte Konstruktion.
* Die Zeichnung kann mehrere Ansichten enthalten (z. B. Front-, Seiten-, Drauf- oder Schnittansichten).
* Analysiere die Beziehungen zwischen den Ansichten, bevor Maße ergänzt werden.
* Bereits vorhandene Maße dürfen nicht widersprochen oder doppelt eingetragen werden.
* Fehlende Maße sollen technisch plausibel und konsistent ergänzt werden.

Technische Hinweise:

* Die Zeichnung ist maßstäblich.
* In der .drawio-Datei entspricht 1 pt genau 1 mm in der Realität.
* Fehlende Maße dürfen direkt aus der Zeichnung geometrisch abgeleitet werden.
* Proportionen und Abstände der Zeichnung sind verbindlich.
* Falls explizite Maße und gezeichnete Abstände voneinander abweichen, haben explizit angegebene Maße Vorrang.
* Nutze die Objektpositionen und Objektgrößen der .drawio-Datei zur direkten Maßermittlung.
* Ergänzte Maße müssen konsistent zu den vorhandenen Koordinaten und Skalierungen sein.

Ergänze insbesondere:

* vollständige Außenmaße
* Maße aller relevanten Zwischenräume
* Materialstärken
* Positionsmaße wichtiger Bauteile
* Abstände, Achsmaße und Einbaumaße
* symmetrische Maße konsistent

Anforderungen:

* Maße in mm
* technisch saubere und logisch konsistente Bemaßung
* keine redundanten Maße
* Maße möglichst fertigungsgerecht platzieren
* Schätzwerte nur verwenden, wenn Maße nicht eindeutig ableitbar sind
* unsichere Maße kennzeichnen

Ausgabeformat:

* Ergebnis direkt als gültige .drawio-Struktur erzeugen
* Vorhandene Geometrien beibehalten
* Ergänzte Maße als separate Dimensionselemente einfügen
* Klare Layer-/Objektstruktur verwenden
* Maßtexte gut lesbar und nicht überlappend platzieren.
```
