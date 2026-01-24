# Export JSON Format - E-Test Emotionale Intelligenz

## Beschreibung für ChatGPT

Das E-Test Tool exportiert die Testergebnisse als JSON-Datei mit folgender Struktur:

## JSON-Struktur

```json
{
  "name": "Max Mustermann",
  "answers": {
    "x01": 3,
    "x02": 4,
    "x03": 2,
    "...": "...",
    "x80": 1
  },
  "scores": {
    "E1": 28,
    "E2": 32,
    "E3": 25,
    "E4": 30,
    "E5": 27,
    "E6": 24,
    "E7": 35,
    "E8": 29
  },
  "classes": {
    "E1": "überdurchschnittlich",
    "E2": "überdurchschnittlich",
    "E3": "durchschnittlich",
    "E4": "überdurchschnittlich",
    "E5": "überdurchschnittlich",
    "E6": "durchschnittlich",
    "E7": "stark ausgeprägt",
    "E8": "überdurchschnittlich"
  },
  "timestamp": "2026-01-24T15:30:45.123Z"
}
```

## Feld-Erklärungen

### `name` (String)
- Der Name der Person, die den Test durchgeführt hat
- Wird vom Benutzer im Eingabefeld eingegeben
- Fallback: "Unbenannt" wenn kein Name eingegeben wurde

### `answers` (Object)
- Enthält alle 80 Antworten des Tests
- Schlüssel: Fragen-IDs von `x01` bis `x80`
- Werte: Likert-Skala von 0 bis 4
  - 0 = trifft nicht zu
  - 1 = trifft wenig zu
  - 2 = trifft teilweise zu
  - 3 = trifft überwiegend zu
  - 4 = trifft voll zu

### `scores` (Object)
- Berechnete Punktzahlen für die 8 Dimensionen emotionaler Intelligenz
- Schlüssel: `E1` bis `E8`
- Werte: Punktzahl von 0 bis 40
- Berechnung erfolgt nach spezifischen Formeln mit positiven/negativen Gewichtungen und Konstanten

### `classes` (Object)
- Bewertungskategorien für jede Dimension
- Schlüssel: `E1` bis `E8`
- Werte: Eine der folgenden Kategorien:
  - "schwach ausgeprägt" (0-8 Punkte)
  - "unterdurchschnittlich" (9-16 Punkte)
  - "durchschnittlich" (17-24 Punkte)
  - "überdurchschnittlich" (25-32 Punkte)
  - "stark ausgeprägt" (33-40 Punkte)

### `timestamp` (String)
- ISO 8601 Zeitstempel des Exports
- Format: YYYY-MM-DDTHH:mm:ss.sssZ
- Wird beim Export automatisch generiert

## Die 8 Dimensionen (E1-E8)

1. **E1**: Selbsteinsicht und Selbstkontrolle (Fragen 1-10)
2. **E2**: Selbstsicherheit und Selbstvertrauen (Fragen 11-20)
3. **E3**: Offenheit und Anpassungsfähigkeit (Fragen 21-30)
4. **E4**: Ausgeglichenheit und Optimismus (Fragen 31-40)
5. **E5**: Leistungsorientierung (Fragen 41-50)
6. **E6**: Vertrauen in die Mitmenschen (Fragen 51-60)
7. **E7**: Einfühlungsvermögen und Mitgefühl (Fragen 61-70)
8. **E8**: Verantwortungsbewusstsein (Fragen 71-80)

## Verwendungszweck

Diese JSON-Dateien können:
- Zur eigenen Dokumentation gespeichert werden
- In die Vergleichs-Funktion des E-Tests hochgeladen werden
- Mit anderen Personen geteilt werden
- Für statistische Auswertungen verwendet werden
- Als Backup der Testergebnisse dienen

## Beispiel-Prompt für ChatGPT

```
Ich habe einen Test zur emotionalen Intelligenz durchgeführt. 
Das Tool exportiert die Ergebnisse als JSON. Hier ist meine Datei:

[JSON hier einfügen]

Die Struktur enthält:
- name: Name der Person
- answers: 80 Antworten (x01-x80) auf Likert-Skala 0-4
- scores: 8 Dimensionen (E1-E8) mit Punkten 0-40
- classes: Bewertung jeder Dimension
- timestamp: Zeitpunkt des Tests

Die 8 Dimensionen sind:
E1: Selbsteinsicht und Selbstkontrolle
E2: Selbstsicherheit und Selbstvertrauen
E3: Offenheit und Anpassungsfähigkeit
E4: Ausgeglichenheit und Optimismus
E5: Leistungsorientierung
E6: Vertrauen in die Mitmenschen
E7: Einfühlungsvermögen und Mitgefühl
E8: Verantwortungsbewusstsein

Kannst du meine Ergebnisse analysieren und mir eine detaillierte 
Auswertung mit Stärken, Entwicklungspotenzialen und konkreten 
Empfehlungen geben?
```

## Technische Details

- **Dateiformat**: JSON (JavaScript Object Notation)
- **Encoding**: UTF-8
- **Dateiendung**: `.json`
- **MIME-Type**: `application/json`
- **Dateiname-Schema**: `eq-test-YYYY-MM-DD.json`
