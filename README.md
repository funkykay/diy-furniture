# diy-furniture

Ein kleines Möbel-Lab für Dinge, die irgendwo zwischen Skizze, Maßzeichnung und „das könnte man doch selber bauen“ liegen.

Hier landen Zeichnungen, Maße, Exporte und Notizen für DIY-Möbelprojekte. Nicht alles ist final, nicht alles ist schön, aber alles ist versioniert. Und das ist ja bekanntlich der halbe Sieg gegen das Chaos.

## Ordnerlogik

Ein Projekt, ein Ordner. Meistens.

## Workflow

Gezeichnet wird in draw.io. Schnell, unkompliziert und völlig ausreichend für Möbel, die am Ende hauptsächlich gerade sein sollen.

Dabei gilt:

- 1 pt in draw.io entspricht 1 mm in der Realität
- Maße können direkt aus der Zeichnung übernommen werden
- Die Zeichnung dient gleichzeitig als Skizze und Maßplan

So bleibt alles einfach, nachvollziehbar und ohne großes CAD-Gefrickel.

## KI-Workflow

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

### Beispiel: Materialliste erzeugen

```text
Analysiere die technische Zeichnung <Name> und erstelle eine Materialliste.

Berücksichtige:
- alle Holzteile
- Maße in mm
- Stückzahlen
- identische Teile zusammenfassen
- geschätzte Materialstärke erkennen
- Ergebnis als Tabelle ausgeben
```

### Beispiel: Maße ergänzen

```text
Analysiere die technische Zeichnung <Name> sund ergänze fehlende Maße sinnvoll im .drawio-Format.

Erstelle:
- vollständige Außenmaße
- Maße aller Zwischenräume
- Materialstärken
- Positionsmaße wichtiger Bauteile
```
