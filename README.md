# 🧠 AI Automation Assistant

**AI Automation Assistant** is a modular Python-based command-line system designed for intelligent command execution, automation routines, and persistent state management. It integrates SQLite for lightweight local storage, JSON for session cookies, and a flexible engine that allows rapid extension of new features or automation tasks. Built for developers, automation enthusiasts, and experimental AI systems.


---

## 🚀 Features

- 🧩 *Modular Architecture* – Clean separation between core layers:
  - *Frontend (CLI Interface)* – Lightweight, intuitive command-line interface for issuing commands and viewing responses.
  - *Backend (Python Engine)* – Modular processors handle command routing, logic execution, and feature control.
  - *Data Layer (SQLite + JSON)* – Persistent storage of user preferences, notes, and session cookies.

- 📡 *Persistent Session State* – Stores and retrieves session state using cookies.json, enabling continuity between sessions.

- 📚 *Database-Driven Storage* – Uses SQLite3 for storing structured data like contacts, saved notes, logs, etc.

- ⚙ *Command Dispatcher* – Central router (command.py) intelligently maps user commands to specific feature logic in features.py.

- 🛠 *Extensibility First* – Add new commands or logic without touching core files. Easily integrate APIs, system calls, or new automation flows.

- 🧠 *Smart Automations* – Built-in features to automate common tasks like opening apps, web browsing, setting timers, and saving contextual data.

- 🖥 *CLI-First Design* – Headless operation makes it perfect for remote shells, voice-assistant backends, or chatbot integration.

- 🔌 *Plug & Play Helpers* – Utility functions in helper.py simplify execution of OS-level tasks or I/O.

- 🧪 *Test-Friendly Codebase* – Structured layout makes unit testing and debugging simple.

---

## 🛠 Technologies Used

- *Python 3.10+* – Core scripting language
- *SQLite3* – Lightweight relational database
- *JSON* – For storing session cookies and state
- *OS/Subprocess* – System-level command execution
- *Modular Design* – Easily extendable structure

---

## 📁 Project Structure


jarvis-automation-assistant/
│── main.py                # App entry point
│── run.py                 # Optional launcher
│── contacts.csv           # Sample data file
│── jarvis.db              # SQLite DB
│── requirements.txt       # Python packages
│── .gitignore             # Ignore patterns
├── engine/
│   ├── command.py         # Command dispatcher
│   ├── config.py          # Config values and keys
│   ├── cookies.json       # Session persistence
│   ├── db.py              # DB handler
│   ├── features.py        # Core assistant actions
│   └── helper.py          # Utility functions


---

## ⚙ Installation & Setup Guide

### 1. Clone the Project

bash
git clone https://github.com/yourhandle/jarvis-automation-assistant.git
cd jarvis-automation-assistant


### 2. Create a Virtual Environment

bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate


### 3. Install Dependencies

bash
pip install -r requirements.txt


---

## ▶ How It Works

1. User runs the app from terminal using main.py
2. CLI prompts for input
3. command.py interprets the input and routes it to the correct handler
4. features.py executes logic—this may include system calls, file writes, or DB updates
5. cookies.json updates session state; jarvis.db stores structured data

---

## 🧪 Supported Command Examples

### 💻 System Commands:
- "Open Notepad" — Launches Notepad (Windows)
- "Set Timer" — Starts a countdown timer
- "Save Note" — Stores a note in the database

### 🌐 App Controls:
- "Open YouTube" — Opens YouTube in browser
- "Check Cookies" — Displays session data
- "Update Contact" — Updates contact CSV or DB

### 🤖 Automation Flows:
- "Log Daily Summary" — Appends summary entry with timestamp
- "Clean Temp Files" — Deletes predefined folder contents

---

## 📦 Requirements

- *Python 3.10+*
- Modules: sqlite3, json, os, subprocess, etc.
- Install using:

bash
pip install -r requirements.txt


---

## 🔮 Future Enhancements

- 🎙 Integrate voice input (e.g., via Android app or Whisper API)
- 🤖 Add LLM support (ChatGPT/GPT-4) for contextual responses
- 🌐 Expand modules into Flask API microservices
- 📊 UI dashboard for command history & logs
- 🏠 Home automation integration via MQTT

---

