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

Wichtig: Verstehe erst die Zeichnung! Es gibt eventuell mehrere Ansichten... z.B. Seitenansicht und Frontansicht. Ich brauche die Materialien dann natürlich nur einmal, obwohl sie in beiden Sichten vorkommen.

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

Wichtig: Verstehe erst die Zeichnung!

Erstelle:
- vollständige Außenmaße
- Maße aller Zwischenräume
- Materialstärken
- Positionsmaße wichtiger Bauteile
```
