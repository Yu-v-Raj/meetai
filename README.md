<div align="center">

# 🧠 MeetAI

### *Your Intelligent AI Meeting Assistant*

<p align="center">
Transform meetings into actionable insights with AI-powered transcription, summarization, task extraction, and intelligent meeting assistance.
</p>

<br>

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi)
![React](https://img.shields.io/badge/React-Frontend-61DAFB?style=for-the-badge&logo=react)
![NextJS](https://img.shields.io/badge/Next.js-Framework-black?style=for-the-badge&logo=next.js)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT-black?style=for-the-badge&logo=openai)
![Whisper](https://img.shields.io/badge/OpenAI-Whisper-purple?style=for-the-badge)
![LangChain](https://img.shields.io/badge/LangChain-AI-orange?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG-Enabled-success?style=for-the-badge)

</div>

---

# 📖 Overview

**MeetAI** is an intelligent AI-powered meeting assistant that goes beyond traditional meeting recording and note-taking. Instead of simply converting speech into text, MeetAI actively understands conversations, tracks context, extracts actionable insights, and assists participants throughout the meeting lifecycle.

The platform leverages **Large Language Models (LLMs)**, **Speech Recognition**, **Natural Language Processing (NLP)**, **Retrieval-Augmented Generation (RAG)**, and **Vector Databases** to create an intelligent meeting companion capable of listening, understanding, organizing, and retrieving meeting knowledge.

Whether you're attending team stand-ups, client discussions, technical interviews, brainstorming sessions, or project planning meetings, MeetAI ensures that every important decision, task, and discussion is captured accurately and remains easily searchable.

---

# 🎯 Why MeetAI?

Modern meetings generate a massive amount of valuable information, but much of it is quickly forgotten or buried in lengthy recordings.

Common challenges include:

- 📝 Manual note-taking distracts participants from discussions.
- ❌ Important action items are often forgotten.
- 📂 Meeting recordings are difficult to search.
- ⏳ Reviewing hour-long meetings wastes time.
- 🤝 Teams struggle to track responsibilities.
- 💡 Valuable knowledge gets lost after meetings.

MeetAI addresses these challenges by transforming conversations into structured, searchable, and actionable knowledge.

---

# ✨ Core Features

## 🎙️ Real-Time Speech Recognition

- Live meeting transcription
- High-accuracy speech-to-text
- Timestamp generation
- Speaker identification
- Noise reduction support

---

## 🧠 AI-Powered Meeting Understanding

MeetAI continuously understands:

- Discussion topics
- Meeting objectives
- Context between conversations
- Decisions
- Agreements
- Disagreements
- Pending questions
- Follow-up requirements

Unlike traditional transcription software, MeetAI understands **what is being discussed**, not just **what is being said**.

---

## 📝 Intelligent Meeting Summaries

Automatically generates:

- Executive Summary
- Key Discussion Points
- Decisions Taken
- Risks Identified
- Blockers
- Questions Raised
- Next Steps

All summaries are generated in a structured and easy-to-read format.

---

## ✅ Action Item Extraction

Automatically detects:

- Tasks
- Responsible person
- Priority
- Deadline
- Dependencies

Example:

```text
Task:
Deploy Backend API

Assigned To:
Alex

Deadline:
Friday

Priority:
High
```

---

## 📌 Decision Tracking

Every important decision discussed during the meeting is automatically extracted and stored.

Example:

```text
Decision:
Switch backend from Flask to FastAPI

Status:
Approved
```

---

## 💬 AI Meeting Chat

After the meeting, users can ask:

- What decisions were made?
- Who owns deployment?
- Summarize today's meeting.
- What are the pending tasks?
- What problems were discussed?
- What deadlines are approaching?

MeetAI answers using contextual understanding of previous meetings.

---

## 🔍 Semantic Search

Instead of searching exact keywords, users can search naturally.

Examples:

```
Authentication discussion

Sprint planning

Budget meeting

Marketing strategy

Database migration
```

MeetAI retrieves the most relevant meeting segments using semantic similarity.

---

## 🧠 Long-Term Memory

Every meeting contributes to a searchable organizational knowledge base.

# 🤖 AI Agent Architecture

MeetAI is designed around a modular **Multi-Agent AI Architecture**, where each AI agent is responsible for a specialized task. This design improves scalability, maintainability, and allows different AI components to collaborate efficiently.

---

## 🎤 Speech Agent

Responsible for capturing and processing meeting audio.

### Responsibilities

- Capture live meeting audio
- Perform Speech-to-Text conversion
- Speaker Diarization
- Timestamp generation
- Noise filtering

**Technologies**

- OpenAI Whisper
- WebRTC
- FastAPI WebSockets

---

## 🧠 Context Agent

Maintains contextual understanding throughout the meeting.

### Responsibilities

- Track discussion flow
- Maintain conversation memory
- Preserve context across long meetings
- Understand topic transitions

---

## 📝 Summary Agent

Continuously generates structured meeting summaries.

### Responsibilities

- Executive Summary
- Discussion Highlights
- Important Decisions
- Key Insights
- Next Steps

---

## ✅ Task Extraction Agent

Automatically detects actionable items from conversations.

### Responsibilities

- Extract Tasks
- Assign Owners
- Detect Deadlines
- Identify Priorities
- Track Pending Work

---

## 🔍 Research Agent

Provides contextual assistance whenever additional information is required.

### Responsibilities

- Retrieve relevant documents
- Perform semantic search
- Answer factual questions
- Support ongoing discussions

---

## 📚 Memory Agent

Maintains long-term organizational knowledge.

### Responsibilities

- Store embeddings
- Vector indexing
- Semantic retrieval
- Historical meeting search

---

## 💬 Assistant Agent

Acts as an intelligent AI companion for users.

Users can ask questions like:

- What decisions were taken?
- Who owns deployment?
- Summarize last week's meetings.
- Which tasks are still pending?
- What did the client request?

---

# 🏗️ System Architecture

```text
                          ┌─────────────────────────────┐
                          │      User joins Meeting     │
                          └──────────────┬──────────────┘
                                         │
                                         ▼
                           ┌──────────────────────────┐
                           │   Audio Capture Layer    │
                           └──────────────┬───────────┘
                                          │
                                          ▼
                           ┌──────────────────────────┐
                           │ Speech Recognition Agent │
                           │   (OpenAI Whisper)       │
                           └──────────────┬───────────┘
                                          │
                                          ▼
                           ┌──────────────────────────┐
                           │  Context Understanding   │
                           │      (LLM Engine)        │
                           └───────┬────────┬─────────┘
                                   │        │
               ┌───────────────────┘        └────────────────────┐
               ▼                                                 ▼
     ┌────────────────────┐                         ┌────────────────────┐
     │  Summary Agent     │                         │ Task Agent         │
     └────────────────────┘                         └────────────────────┘
               │                                                 │
               └──────────────────┬──────────────────────────────┘
                                  ▼
                    ┌──────────────────────────────┐
                    │  Vector Database + Memory    │
                    │      (RAG Knowledge Base)    │
                    └──────────────┬───────────────┘
                                   ▼
                      ┌──────────────────────────┐
                      │    AI Chat Assistant     │
                      └──────────────────────────┘
```

---

# 🔄 Meeting Workflow

```text
        Join Meeting
              │
              ▼
      Capture Live Audio
              │
              ▼
      Speech Recognition
              │
              ▼
      Speaker Identification
              │
              ▼
      AI Context Analysis
              │
              ▼
      Live Summary Generation
              │
              ▼
     Action Item Extraction
              │
              ▼
      Decision Identification
              │
              ▼
       Vector Embedding Storage
              │
              ▼
      Semantic Search Enabled
              │
              ▼
      AI Meeting Assistant
```

---

# 🛠️ Technology Stack

| Category | Technology |
|-----------|------------|
| **Programming Language** | Python 3.12 |
| **Backend** | FastAPI |
| **Frontend** | React.js |
| **Framework** | Next.js |
| **Styling** | Tailwind CSS |
| **UI Components** | ShadCN UI |
| **AI Models** | OpenAI GPT |
| **Speech Recognition** | OpenAI Whisper |
| **AI Framework** | LangChain |
| **Multi-Agent Framework** | LangGraph |
| **Embeddings** | Sentence Transformers |
| **Retrieval** | RAG |
| **Vector Database** | Pinecone / FAISS / ChromaDB |
| **Database** | PostgreSQL / MongoDB |
| **Caching** | Redis |
| **Authentication** | JWT |
| **Real-Time Communication** | WebSockets |
| **Deployment** | Docker |
| **Hosting** | Vercel / Railway / Render |
| **Version Control** | Git & GitHub |

---

# 📁 Project Structure

```text
MeetAI/
│
├── backend/
│   ├── api/
│   ├── agents/
│   │     ├── speech_agent.py
│   │     ├── summary_agent.py
│   │     ├── task_agent.py
│   │     ├── research_agent.py
│   │     ├── memory_agent.py
│   │     └── assistant_agent.py
│   │
│   ├── database/
│   ├── rag/
│   ├── models/
│   ├── services/
│   ├── utils/
│   └── main.py
│
├── frontend/
│   ├── app/
│   ├── components/
│   ├── hooks/
│   ├── pages/
│   ├── styles/
│   └── public/
│
├── docs/
├── assets/
├── docker/
├── requirements.txt
├── docker-compose.yml
└── README.md
```

---

# 🚀 Key Highlights

✔️ Real-Time Meeting Intelligence

✔️ AI-Powered Summarization

✔️ Multi-Agent Architecture

✔️ Retrieval-Augmented Generation (RAG)

✔️ Semantic Meeting Search

✔️ Long-Term Meeting Memory

✔️ Context-Aware AI Assistant

✔️ Enterprise-Ready Modular Design

---

# 🚀 Getting Started

Follow the instructions below to set up MeetAI on your local machine.

---

# 📋 Prerequisites

Before running the project, make sure you have the following installed:

- Python 3.11+
- Node.js 18+
- npm / yarn / pnpm
- Git
- Docker (Optional)
- PostgreSQL
- Redis (Optional)
- Pinecone / ChromaDB (Optional)

---

# ⚙️ Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/MeetAI.git

cd MeetAI
```

---

## 2️⃣ Backend Setup

```bash
cd backend

python -m venv venv
```

### Activate Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## 3️⃣ Frontend Setup

```bash
cd frontend

npm install
```

or

```bash
yarn install
```

---

## 4️⃣ Environment Variables

Create a `.env` file inside the backend directory.

```env
OPENAI_API_KEY=your_api_key

DATABASE_URL=postgresql://localhost/meetai

SECRET_KEY=your_secret_key

REDIS_URL=redis://localhost:6379

PINECONE_API_KEY=your_pinecone_key

PINECONE_INDEX=meetai

MODEL_NAME=gpt-4

WHISPER_MODEL=large
```

---

# ▶️ Running the Backend

```bash
cd backend

uvicorn main:app --reload
```

Backend will run at

```
http://localhost:8000
```

---

# 💻 Running the Frontend

```bash
cd frontend

npm run dev
```

Frontend will run at

```
http://localhost:3000
```

---

# 📡 API Endpoints

## Health Check

```
GET /health
```

Returns server status.

---

## Start Meeting

```
POST /api/meeting/start
```

Creates a new meeting session.

---

## Stop Meeting

```
POST /api/meeting/stop
```

Ends the active meeting.

---

## Upload Audio

```
POST /api/audio/upload
```

Uploads an audio recording for transcription.

---

## Generate Summary

```
POST /api/summary
```

Returns an AI-generated meeting summary.

---

## Extract Action Items

```
POST /api/tasks
```

Returns detected tasks, owners, and deadlines.

---

## AI Chat

```
POST /api/chat
```

Ask questions about previous meetings.

---

## Semantic Search

```
POST /api/search
```

Retrieve relevant meeting information using natural language.

---

# 💻 Usage

### Start the backend

```bash
uvicorn main:app --reload
```

Start the frontend

```bash
npm run dev
```

Open your browser

```
http://localhost:3000
```

Create a meeting.

Start speaking.

MeetAI will automatically

- Transcribe conversations
- Understand discussions
- Generate summaries
- Extract tasks
- Identify decisions
- Store meeting knowledge

---

# 📸 Screenshots

> Add screenshots here after the project is complete.

### Dashboard

```
assets/dashboard.png
```

---

### Live Meeting

```
assets/live-meeting.png
```

---

### AI Summary

```
assets/summary.png
```

---

### Analytics Dashboard

```
assets/analytics.png
```

---

### AI Chat Assistant

```
assets/chat.png
```

---

# 📊 Example AI Output

## Executive Summary

```
The meeting focused on the upcoming product release.

The backend API has been completed.

Frontend integration will finish by Friday.

Deployment is scheduled for next Tuesday.
```

---

## Action Items

| Task | Owner | Deadline | Priority |
|------|-------|----------|----------|
| Complete UI | Alex | Friday | High |
| Deploy Backend | John | Tuesday | High |
| Testing | Sarah | Monday | Medium |

---

## Decisions

```
Backend Framework

FastAPI

Status

Approved
```

---

## AI Chat Example

### User

```
Who is responsible for deployment?
```

### MeetAI

```
John is responsible for deployment.

Deadline:
Tuesday

Priority:
High
```

---
This allows users to retrieve historical discussions without manually reviewing recordings.

---
