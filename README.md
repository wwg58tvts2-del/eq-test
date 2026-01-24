# E-Test – Emotionale Intelligenz

Ein webbasiertes Selbsteinschätzungsinstrument zur Messung emotionaler Intelligenz in acht Dimensionen.

## 📋 Übersicht

Dieses Tool ermöglicht es Benutzern, ihre emotionale Intelligenz anhand von 80 Fragen selbst einzuschätzen. Die Auswertung erfolgt automatisch und liefert detaillierte Ergebnisse in acht verschiedenen Kompetenzbereichen.

## ✨ Features

### Befragung
- **80 Items**: Umfassender Fragebogen zur Selbsteinschätzung
- **5-stufige Likert-Skala**: Von "nicht zutreffend" bis "ganz zutreffend"
- **Auto-Save**: Antworten werden automatisch im Browser gespeichert
- **Validierung**: Prüfung auf Vollständigkeit mit visuellen Hinweisen
- **Einklappbare Bereiche**: Übersichtliche Navigation durch die Fragebereiche

### Auswertung
- **8 Dimensionen**: Detaillierte Bewertung in allen Bereichen emotionaler Intelligenz
- **Visuelles Feedback**: Fortschrittsbalken und Bewertungsklassen
- **Profilübersicht**: Tabellarische Zusammenfassung aller Ergebnisse
- **Bewertungsskala**: Von "schwach ausgeprägt" bis "stark ausgeprägt"

### Export & Vergleich
- **JSON-Export**: Speicherung der Ergebnisse mit Zeitstempel
- **Dateidownload**: Automatischer Download mit Datum und Uhrzeit
- **Drag & Drop**: Einfaches Hochladen mehrerer Ergebnisse
- **Vergleichsansicht**: Farbcodierte Balkendiagramme zum Vergleich mehrerer Personen

## 🎯 Dimensionen

Das Tool bewertet folgende acht Bereiche emotionaler Intelligenz:

1. **E1**: Selbsteinsicht und Selbstkontrolle
2. **E2**: Selbstsicherheit und Selbstvertrauen
3. **E3**: Offenheit und Anpassungsfähigkeit
4. **E4**: Ausgeglichenheit und Optimismus
5. **E5**: Leistungsorientierung
6. **E6**: Vertrauen in die Mitmenschen
7. **E7**: Einfühlungsvermögen und Mitgefühl
8. **E8**: Verantwortungsbewusstsein

## 🚀 Installation

### Voraussetzungen
- Moderner Webbrowser (Chrome, Firefox, Safari, Edge)
- Keine zusätzliche Software erforderlich

### Setup
1. Repository klonen oder Datei herunterladen
2. `eq-test.html` im Browser öffnen
3. Fertig! Das Tool funktioniert vollständig offline

```bash
git clone <repository-url>
cd eq-test
# Öffne eq-test.html in deinem Browser
```

## 📖 Verwendung

### 1. Befragung durchführen
1. Namen eingeben (optional, für Export)
2. Alle 80 Fragen beantworten (0-4 Punkte pro Frage)
3. Auf "Auswerten" klicken

### 2. Ergebnisse ansehen
- Detaillierte Auswertung in allen 8 Dimensionen
- Fortschrittsbalken zeigen die erreichten Punkte (max. 40 pro Dimension)
- Bewertungsklassen geben qualitative Einschätzungen

### 3. Ergebnisse exportieren
1. Auf "Export JSON" klicken
2. JSON-Daten in Zwischenablage kopieren oder als Datei speichern
3. Dateiname enthält automatisch Datum und Uhrzeit

### 4. Ergebnisse vergleichen
1. Zum Tab "Vergleichen" wechseln
2. Mehrere JSON-Dateien hochladen (Drag & Drop oder Dateiauswahl)
3. Vergleich aller Ergebnisse in farbcodierten Balkendiagrammen

## 📊 Bewertungssystem

Jede Dimension wird auf einer Skala von 0-40 Punkten bewertet:

- **0-8 Punkte**: Schwach ausgeprägt
- **9-16 Punkte**: Unterdurchschnittlich
- **17-24 Punkte**: Durchschnittlich
- **25-32 Punkte**: Überdurchschnittlich
- **33-40 Punkte**: Stark ausgeprägt

## 💾 Datenspeicherung

- **localStorage**: Antworten werden lokal im Browser gespeichert
- **Keine Server**: Alle Daten bleiben auf dem Gerät des Benutzers
- **Privatsphäre**: Keine Datenübertragung an externe Server

## 🔧 Technische Details

### Technologie-Stack
- **HTML5**: Struktur und Semantik
- **CSS3**: Responsive Design und Animationen
- **JavaScript (ES6+)**: Logik und Interaktivität
- **jQuery 3.7.1**: DOM-Manipulation und Event-Handling

### Browser-Kompatibilität
- Chrome/Edge ≥ 90
- Firefox ≥ 88
- Safari ≥ 14
- Mobile Browser werden unterstützt

### Features
- Responsive Design für alle Bildschirmgrößen
- Sticky Header für konstante Navigation
- Smooth Scrolling zu relevanten Bereichen
- Animierte Fortschrittsbalken
- Drag & Drop für Datei-Upload

## 📄 JSON-Format

Exportierte Dateien enthalten folgende Struktur:

```json
{
  "name": "Max Mustermann",
  "answers": {
    "x01": 3,
    "x02": 4,
    ...
  },
  "scores": {
    "E1": 28,
    "E2": 32,
    ...
  },
  "classes": {
    "E1": "überdurchschnittlich",
    "E2": "überdurchschnittlich",
    ...
  },
  "timestamp": "2026-01-24T17:30:45.123Z"
}
```

## ⚠️ Hinweise

- Dieses Tool dient nur zur **Selbstreflexion und Orientierung**
- Es ersetzt **keine psychologische Diagnose** oder Beratung
- Die Ergebnisse basieren auf **Selbstauskunft** und sind subjektiv
- Für professionelle Einschätzungen konsultieren Sie bitte Fachpersonal

## 🤝 Verwendung mit ChatGPT

Die exportierten JSON-Daten können für eine detaillierte Analyse an ChatGPT weitergegeben werden. Eine Anleitung finden Sie in `JSON-Format-Beschreibung.md`.

## 📝 Lizenz

Dieses Projekt ist für Bildungs- und Forschungszwecke frei verfügbar.

## 👤 Autor

Martin Wiesner

## 🔄 Version

1.0.0 - Januar 2026
