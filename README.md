# 🎙️ Voice-Based AI Agent with Memory & Tools

A voice-enabled AI agent that manages a **To-Do list** using function calling tools and remembers important past user interactions — built as part of a college assignment.

---

## 📌 Features

- 🎤 **Voice Interface** — Accepts voice input via microphone, transcribes speech to text (STT), and responds using text-to-speech (TTS)
- ✅ **To-Do Management (CRUD)** — Add, update, delete, and list tasks using AI-powered tool calling
- 🧠 **Memory System** — Stores and recalls important past user interactions across sessions
- 🤖 **Smart Agent Behavior** — Decides when to invoke tools vs. respond conversationally

---

## 🛠️ Tech Stack

| Component        | Technology                        |
|------------------|-----------------------------------|
| Language         | Python                            |
| Speech-to-Text   | OpenAI Whisper / SpeechRecognition |
| Text-to-Speech   | gTTS / pyttsx3 / ElevenLabs       |
| LLM / Agent      | OpenAI GPT (Function Calling)     |
| Memory           | JSON / SQLite / LangChain Memory  |
| Audio I/O        | PyAudio / sounddevice             |

> Update this table to match your actual stack.

---

## 📁 Project Structure

```
voice-ai-agent/
│
├── main.py               # Entry point — starts the voice agent
├── agent.py              # Agent logic & prompt definition
├── tools.py              # Tool definitions (add/update/delete/list tasks)
├── memory.py             # Memory system (store & recall interactions)
├── voice.py              # Speech-to-Text & Text-to-Speech handlers
├── todo_store.json       # Persistent To-Do storage
├── memory_store.json     # Persistent memory storage
├── requirements.txt      # Python dependencies
├── .gitignore            # Files to ignore in Git
├── LICENSE               # MIT License
└── README.md             # This file
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/voice-ai-agent.git
cd voice-ai-agent
```

### 2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up your API key
Create a `.env` file in the root directory:
```
OPENAI_API_KEY=your_openai_api_key_here
```

### 5. Run the agent
```bash
python main.py
```

---

## 🗣️ How to Use

1. Run the agent and wait for the prompt: `"Listening..."`
2. Speak your command, for example:
   - *"Add buy groceries to my to-do list"*
   - *"What tasks do I have?"*
   - *"Mark task 2 as done"*
   - *"Delete the first task"*
   - *"What did I tell you last time?"*
3. The agent processes your voice, decides whether to use a tool or reply conversationally, and responds with audio.

---

## 🧰 Available Tools

| Tool            | Description                          |
|-----------------|--------------------------------------|
| `add_task`      | Adds a new task to the To-Do list    |
| `list_tasks`    | Lists all current tasks              |
| `update_task`   | Updates an existing task by ID       |
| `delete_task`   | Deletes a task by ID                 |
| `recall_memory` | Retrieves past important interactions |

---

## 📦 Requirements

See [`requirements.txt`](./requirements.txt). Key packages:

```
openai
speechrecognition
pyaudio
gTTS
python-dotenv
langchain
```

---

## 📄 License

This project is licensed under the [MIT License](./LICENSE).

---



> ⭐ If you found this useful, consider starring the repo!
