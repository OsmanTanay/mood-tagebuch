# Stimmungstagebuch – KI-gestützte Webanwendung

Eine Webanwendung, die Nutzern ermöglicht, tägliche Erlebnisse und Stimmungen einzutragen und darauf basierend automatisch personalisierte KI-Empfehlungen zu erhalten.

## Funktionsweise

1. Nutzer füllt ein Webformular aus – Name, Stimmungswert (1–10), Ereignistyp, Ort und Beschreibung
2. Formulardaten werden per **JSON via Fetch API** an das Flask-Backend gesendet
3. Das Backend verarbeitet die Daten und sendet sie an die **OpenAI API (GPT-3.5-turbo)**
4. Das Sprachmodell generiert eine kurze, alltagsnahe Empfehlung (max. 2–3 Sätze)
5. Eintrag und Empfehlung werden in einer **SQLite-Datenbank** gespeichert
6. Alle Einträge werden dynamisch im Frontend geladen und können einzeln gelöscht werden

## Technologien

| Bereich | Technologie |
|---|---|
| Backend | Python, Flask |
| Datenbank | SQLite |
| KI-Integration | OpenAI API (GPT-3.5-turbo) |
| Frontend | HTML, CSS, JavaScript (Fetch API) |
| Datenbankzugriff | Eigene CRUD-Module für Events und User |

## Features

- Stimmungseintrag mit Skala 1–10 erstellen
- Automatische KI-Empfehlung basierend auf Eintrag und Nutzerprofil
- Alle Einträge chronologisch (neueste zuerst) anzeigen
- Einzelne Einträge löschen
- Nutzerverwaltung mit eigenem Datenbankmodul

## Projektstruktur

```
Tagebuch/
├── app.py              # Flask-Routen und Hauptlogik
├── database/           # SQLite-Datenbankdatei
├── models/             # CRUD-Module für Events und User
├── static/             # CSS, JavaScript (Formular & Anzeige)
└── templates/          # HTML-Templates
```

## Projektstart

```bash
# Abhängigkeiten installieren
pip install -r requirements.txt

# OpenAI API-Key setzen
export OPENAI_API_KEY=dein-api-key

# Anwendung starten
python app.py
```

Die App läuft dann unter `http://localhost:5000`

## Entwickelt von

Osman Tanay – Gruppenprojekt im Rahmen des Wahlpflichtfachs "Programmieren in Python" (1. Semester), B.Sc. Artificial Intelligence and Data Science, Hochschule Aalen
