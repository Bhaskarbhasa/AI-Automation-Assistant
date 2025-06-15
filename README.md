# 🧠 AI Automation Assistant

**AI Automation Assistant** is a modular, Python-based command-line system designed for intelligent command execution, personal automation routines, and persistent state management. Tailored for developers, automation enthusiasts, and experimental AI systems, it offers an extensible and smart automation platform with persistent memory and system integration.

---

## 🚀 Features

### 🧩 Modular Architecture
- **Frontend (CLI Interface):** Lightweight, interactive command-line interface for real-time command execution.
- **Backend (Python Engine):** Modular processing layer to route and execute logic for various features.
- **Data Layer (SQLite + JSON):** Persistent storage for user preferences, session state, contacts, and logs.

### 📡 Persistent Sessions
- Stores session state in `cookies.json` to maintain continuity between sessions.

### 📚 Database-Driven Storage
- Uses `SQLite3` (`jarvis.db`) for structured data like notes, logs, contacts, and settings.

### ⚙ Smart Command Dispatcher
- `command.py` intelligently routes user commands to relevant logic in `features.py`.

### 🛠 Extensibility First
- Easily add new commands, automations, or integrations with minimal changes to core files.

### 🧠 Built-in Automations
- Launch applications, manage notes, set timers, clean files, and more using simple commands.

### 🖥 CLI-First Design
- Headless and terminal-focused; ideal for remote shells, bots, or backend assistants.

### 🔌 Utility Helpers
- `helper.py` provides system-level utilities (file ops, time handling, OS commands).

---

## 🛠 Technologies Used

- **Python 3.10+** – Core programming language  
- **SQLite3** – Lightweight relational database  
- **JSON** – For session state and cookies  
- **os / subprocess** – For system-level command execution  
- **Modular Python design** – Easy to extend and maintain  

---

## 📁 Project Structure

```
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
```

---

## ⚙ Installation & Setup Guide

### 1. Clone the Project

```bash
git clone https://github.com/yourhandle/jarvis-automation-assistant.git
cd jarvis-automation-assistant
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
# Activate on Windows
venv\Scripts\activate
# Activate on macOS/Linux
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶ How It Works

1. Run the assistant from terminal:
    ```bash
    python main.py
    ```
2. CLI prompts for input commands.
3. `command.py` parses and routes input to relevant handler in `features.py`.
4. Automation tasks execute and update `cookies.json` or `jarvis.db` as needed.
5. Output is displayed in terminal and saved persistently when necessary.

---

## 🧪 Supported Command Examples

### 💻 System Commands:
- `Open Notepad` — Launches Notepad (Windows)
- `Set Timer` — Starts a countdown timer
- `Save Note` — Stores a note in the database

### 🌐 App Controls:
- `Open YouTube` — Opens YouTube in browser
- `Check Cookies` — Displays session data
- `Update Contact` — Updates contact CSV or DB

### 🤖 Automation Flows:
- `Log Daily Summary` — Appends summary entry with timestamp
- `Clean Temp Files` — Deletes predefined folder contents

---

## 📦 Requirements

- Python 3.10+
- Required modules are listed in `requirements.txt`

```bash
pip install -r requirements.txt
```

---

## 🔮 Future Enhancements

- 🎙 Voice input integration (e.g., Whisper API, Android voice assistant)
- 🤖 LLM support (ChatGPT/GPT-4) for intelligent and contextual command handling
- 🌐 Modular API using Flask or FastAPI for network-based control
- 📊 Web-based dashboard to view logs, session data, and command history
- 🏠 Home automation control via MQTT or similar protocols
