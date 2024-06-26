# automated-support-helper

Phase 1: Setup und Vorbereitung
Woche 1: Projektziele definieren und Anwendungsfälle festlegen
1. Projektziele definieren:

Hauptziel: Ein KI-Chatbot, der den Kundenservice automatisiert, um die Effizienz zu steigern und die Wartezeiten zu verkürzen.
Nebenziele: Reduzierung der Arbeitslast für das Support-Team, Verbesserung der Kundenzufriedenheit, Demonstration der Fähigkeiten eines KI-Chatbots als Vorzeigemodell.
2. Anwendungsfälle festlegen:

Kundenservice und Support:
Automatische Beantwortung von FAQs.
Bestellstatus und Lieferanfragen.
Automatisierte Ticketerstellung:
Ticket-Erstellung und Priorisierung.
Personalassistenz:
Terminvereinbarungen und Erinnerungen.
Verkaufsunterstützung:
Produktberatung und Angebotserstellung.
Internes Wissensmanagement:
Mitarbeiter-Onboarding und Informationszugriff.
Phase 2: Technologieauswahl und Entwicklungsumgebung einrichten
Woche 2: Technologieauswahl und Einrichtung der Entwicklungsumgebung
1. Technologieauswahl:

Programmiersprache: Python
Machine Learning Framework: PyTorch
Web-Framework: Flask
Cloud-Dienste: Microsoft Azure für Hosting und Skalierbarkeit
2. Entwicklungsumgebung einrichten:

Schritte zur Einrichtung der Entwicklungsumgebung:

Python und Anaconda installieren:

Python: Python Download
Anaconda: Anaconda Download
Erstellen eines virtuellen Environments mit Anaconda:

bash
Code kopieren
conda create -n chatbot-env python=3.8
conda activate chatbot-env
Installieren der benötigten Bibliotheken:

bash
Code kopieren
pip install torch torchvision torchaudio
pip install flask
pip install transformers
pip install azure-storage-blob
Erstellen einer Verzeichnisstruktur:

plaintext
Code kopieren
project-root/
├── data/
├── models/
├── scripts/
├── app/
│   ├── templates/
│   ├── static/
│   ├── __init__.py
│   ├── routes.py
├── config.py
├── requirements.txt
├── README.md
Einrichten einer einfachen Flask-App:

python
Code kopieren
# app/__init__.py
from flask import Flask

def create_app():
    app = Flask(__name__)
    from .routes import main
    app.register_blueprint(main)
    return app

# app/routes.py
from flask import Blueprint, render_template

main = Blueprint('main', __name__)

@main.route('/')
def index():
    return "Hello, this is the Chatbot!"

# run.py
from app import create_app

app = create_app()

if __name__ == "__main__":
    app.run(debug=True)
Starten der Flask-App:

bash
Code kopieren
python run.py

## Collaborate with GPT Engineer

This is a [gptengineer.app](https://gptengineer.app)-synced repository 🌟🤖

Changes made via gptengineer.app will be committed to this repo.

If you clone this repo and push changes, you will have them reflected in the GPT Engineer UI.

## Tech stack

This project is built with React and Chakra UI.

- Vite
- React
- Chakra UI

## Setup

```sh
git clone https://github.com/GPT-Engineer-App/automated-support-helper.git
cd automated-support-helper
npm i
```

```sh
npm run dev
```

This will run a dev server with auto reloading and an instant preview.

## Requirements

- Node.js & npm - [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
