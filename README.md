# AI Mood Recommendation App

A Flask-based web application that allows users to submit daily mood entries and receive AI-generated personalized recommendations based on their context.

## Features

- Create daily mood entries with mood score, event type, location and description
- Generate personalized recommendations using the OpenAI API
- Store mood entries and recommendations in a SQLite database
- Display all entries dynamically in the frontend
- Delete individual entries
- Basic user and event data handling with custom CRUD modules

## Tech Stack

| Area | Technology |
|---|---|
| Backend | Python, Flask |
| Frontend | HTML, CSS, JavaScript |
| API Communication | Fetch API, JSON |
| Database | SQLite |
| AI Integration | OpenAI API |

## Project Structure

```text
ai-mood-recommendation-app/
├── database/
├── models/
├── static/
├── templates/
├── app.py
├── requirements.txt
└── README.md
```

## How It Works

1. The user submits a mood entry through a web form.
2. The frontend sends the data as JSON to the Flask backend.
3. The backend processes the input and sends the context to the OpenAI API.
4. The AI model generates a short personalized recommendation.
5. The entry and recommendation are stored in SQLite.
6. Saved entries are displayed dynamically in the frontend.

## Setup

Install dependencies:

```bash
pip install -r requirements.txt
```

Set your OpenAI API key:

```bash
export OPENAI_API_KEY=your_api_key_here
```

Run the application:

```bash
python app.py
```

The app runs at:

```text
http://localhost:5000
```

## Screenshots

Add screenshots here.

```markdown
![Mood Entry Form](screenshots/form.png)
![Entry Overview](screenshots/entries.png)
```

## Context

Developed as part of the B.Sc. Artificial Intelligence and Data Science program at Hochschule Aalen.
