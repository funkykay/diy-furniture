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

## Beispiel: Materialliste erzeugen

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

## Beispiel: Maße ergänzen

```text
Analysiere die technische Zeichnung <Name> und ergänze fehlende Maße sinnvoll im .drawio-Format.

Erstelle:
- vollständige Außenmaße
- Maße aller Zwischenräume
- Materialstärken
- Positionsmaße wichtiger Bauteile
```
