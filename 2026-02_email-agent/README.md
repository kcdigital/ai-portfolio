# Email Agent — Automated Client Response System

## 📌 Project Overview
This project is a small agent-based email automation system designed to handle first responses to potential clients.

It simulates multiple reply styles, evaluates response quality, and automatically sends the most appropriate email reply.

## 🎯 Motivation
As an independent 3D fashion designer, I often missed client inquiries due to time constraints.  
This project was built to reduce response delays and improve communication efficiency.

## ⚙️ Key Features
- Multi-style email draft generation
- LLM-based response evaluation
- Automated subject line creation
- Email formatting and sending workflow
- Notification integration (Pushover)

## 🧠 Tech Stack
- Python
- OpenAI API
- Pydantic
- SMTP / Email API
- Agentic workflow design

## 🧭 System Workflow

Below is a simplified architecture of the multi-agent email automation system:

Client Inquiry
(Purchase / Collaboration)
            │
            ▼
     Intent Understanding
            │
            ▼
   ┌──────────────────────┐
   │  Multi-Agent Drafting │
   └──────────────────────┘
      │        │        │
      ▼        ▼        ▼
   Agent 1  Agent 2  Agent 3
      │        │        │
      └────────┴────────┘
               │
               ▼
        LLM Evaluation Agent
        (Quality Scoring +
         Best Draft Selection)
               │
               ▼
        Selected Email Draft
               │
      ┌────────┴─────────┐
      ▼                  ▼
Subject Writing      Format Refining
    Agent               Agent
      │                  │
      └────────┬─────────┘
               ▼
          Final Email
               │
               ▼
          Email API
               │
               ▼
           Sent Out
