# prompt-engineering-library
A collection of tested and documented prompts for LLMs

# AI Running Coach – Prompt Engineering Library

This is a modular prompt engineering project designed to power an AI-based running coach. It supports personalized training plan generation, adaptive coaching feedback, motivation delivery, and beginner education—built entirely from tested, reusable prompt components.

**Built by Travis Johnson** to demonstrate real-world use of LLMs, contextual memory, and human-centered design in health + fitness applications.

---

## 💡 What It Does

This system acts as the brain of an AI running coach. It includes:
- Personalized training plan creation
- Weekly plan adjustment based on feedback
- Motivation tailored to the user’s coaching style
- On-demand check-ins and mental support
- Educational explanations of running concepts and workouts

Each capability is handled by a well-documented, reusable prompt module.

---

## 🧠 How It Works

The system follows a **hybrid interaction model**:
- **Structured onboarding form** to gather core user data
- **Conversational chat** for daily interaction, check-ins, and motivation
- **Context memory** to maintain tone, goals, gear, terrain, etc.

Prompt routing is managed logically based on user input and feedback loops.

See the [`interface-spec.md`](docs/interface-spec.md) for a breakdown of the flow.

---

## 📦 Prompt Modules

| Module | Description |
|--------|-------------|
| `training-plan-generator.md` | Builds a full training plan based on user background, goals, terrain, and preferences |
| `plan-adjustment.md` | Weekly check-in that adapts the plan based on performance, soreness, and energy |
| `daily-check-in.md` | Allows the user to submit casual, real-time updates to get immediate support |
| `motivation-style.md` | Generates motivational messages tailored to the user's selected coaching style |
| `run-explainer.md` | Explains workout types, pacing strategies, and training concepts in plain language |
| `context-template.md` | Shared context template used to simulate memory across prompts |

---

## 📁 Folder Structure

prompt-engineering-library/
├── prompts/
│ └── running-coach/
│ ├── training-plan-generator.md
│ ├── plan-adjustment.md
│ ├── daily-check-in.md
│ ├── motivation-style.md
│ └── run-explainer.md
├── metadata/
│ └── context-template.md
├── docs/
│ └── interface-spec.md
└── README.md


---

## 🚀 How to Use or Extend

- Clone the repo and explore each prompt module individually.
- Test prompts manually in ChatGPT or with the OpenAI API.
- Use the included context-template to simulate persistent user memory.
- Adapt the system to other domains (e.g., weightlifting coach, cycling coach, productivity assistant).
- Optional: build a front-end chatbot interface using the `interface-spec.md` as a guide.

---

## 🛣️ Future Plans

- Add gear recommendations and pacing calculators
- Connect to live weather and terrain APIs
- Build a web or mobile interface
- Publish a blog post walkthrough of the project

---

## 👤 Author

Built by Travis Johnson  
Project start: May 2025  
Goal: Portfolio-ready example of advanced prompt engineering for real-world applications

---

