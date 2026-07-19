# OSAI-GSM
AI Interface for GSM brick phones - Dump Smartphones

## VoiceKanban MVP

A personal AI phone assistant that lets you manage tasks by calling a phone number from any phone.

Example:

> Call → "Create task record Hotmart lesson 3"

Response:

> "Task created."

---

# Goal

Replace smartphone task capture with voice calls.

---

# Features

* Create task
* Complete task
* List tasks
* Move task between columns

Kanban:

* TODO
* DOING
* DONE

---

# Tech Stack

* Twilio (phone number)
* Gemini API
* SQLite
* Python FastAPI
* Text-to-Speech

---

# Architecture

Phone Call

↓

Speech-to-Text

↓

Gemini

↓

Task Engine

↓

SQLite

↓

Voice Response

---

# Implementation Steps

## Step 1 — Database

Create SQLite database.

Time: 30 minutes

Output:

* tasks table
* CRUD functions

---

## Step 2 — Task API

Create endpoints:

* create_task
* move_task
* complete_task
* list_tasks

Time: 1 hour

---

## Step 3 — Gemini Parser

Convert natural language into actions.

Example:

"Create task buy HDMI cable"

↓

```json
{
  "action": "create_task",
  "title": "Buy HDMI cable"
}
```

Time: 1–2 hours

---

## Step 4 — Telephony

Connect incoming calls.

Time: 2–3 hours

---

## Step 5 — Speech-to-Text

Convert caller voice to text.

Time: 1 hour

---

## Step 6 — Text-to-Speech

Generate voice confirmations.

Example:

> "Task created."

Time: 1 hour

---

## Step 7 — End-to-End Testing

Test:

* Create task
* Move task
* Complete task
* List tasks

Time: 2 hours

---

# Total Estimate

Experienced automation developer:

8–12 hours

Weekend project:

1–2 days

---

# MVP Success Criteria

User can:

* Call from any phone
* Speak a command
* Update tasks
* Receive voice confirmation

Without opening an app or using a smartphone.

---

# Future Versions

* Calendar integration
* WhatsApp integration
* Daily AI review
* Priority levels
* Voice reminders
* CRM support
* Multi-user support
