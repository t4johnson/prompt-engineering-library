# Prompt Engineering Library

A curated collection of structured, modular prompt engineering examples for real-world applications. Focused on fitness, coaching, and gear, this repo blends lived experience with AI tooling to create useful, adaptable systems — not just demos.

---

## AI Running Coach

A modular AI-based running coach designed to deliver:

- Personalized training plan generation
- Weekly adaptive pla# Prompt Engineering Library

A curated set of **modular, context-aware prompt systems** built for real-world coaching, fitness, and self-guided support tools. This library blends lived experience with applied prompt engineering to produce tools that are consistent, safe, and human-centered.

---

## 🧠 AI Running Coach (Flagship Project)

A fully modular, test-ready prompt suite that functions as a **tone-safe, consistency-driven virtual coach**. It is built to be:

- 🏃‍♂️ **Customizable** by user experience level, coaching style, and goals
- 🧠 **Memory-aware** when integrated into a stateful agent loop
- 🔍 **Self-auditing** via red-team, plan review, and injury risk detection
- ✍️ **Portfolio-ready** with polished system messages and JSON I/O

---

## 🧩 Included Modules (v1.3)

| File                             | Function |
|----------------------------------|----------|
| `training-plan-generator.md`     | Builds structured training plans based on runner profile |
| `plan-adjustment.md`             | Adapts plans weekly using structured and emotional feedback |
| `daily-check-in.md`              | Captures body/mood state and flags issues or insights |
| `weekly-check-in.md`             | Synthesizes patterns from daily logs and adjusts accordingly |
| `route-generator.md`             | Generates location-aware, surface-specific route options |
| `fueling-hydration-planner.md`   | Recommends safe fueling strategies based on heat, run type, gear |
| `injury-recovery-module.md`      | Triage + guidance for pain reports and setbacks |
| `journal-logger.md`              | Builds a lightweight, longitudinal training log |
| `red-team-checker.md`            | Flags unsafe or misaligned training advice and tone |
| `plan-review-evaluator.md`       | Audits training blocks for imbalance or overreach |
| `structured-plan-export.md`      | Converts plan data to exportable JSON or markdown |
| `motivation-style.md`            | Adapts tone to user's emotional + motivational preferences |
| `run-explainer.md`               | Explains structured runs in accessible, plain language |
| `run-summary-zero-shot.md`       | Generates day-of summaries from minimal user input |
| `runner-intake-form.md`          | Initializes user profile for downstream system use |

---

## 📁 Folder Structure

```
prompt-engineering-library/
├── prompts/
│   └── running-coach/           # Core prompt modules (v1.3)
├── metadata/
│   └── context-template.md      # Example persistent memory profile
├── docs/
│   └── interface-spec.md        # High-level architecture / chaining guide
└── README.md
```

---

## 🔄 How It Works

The full system is designed to run in a modular agent loop:

- **Input**: `runner-intake-form.md` seeds profile with race goals, terrain, gear, experience
- **Output**: `training-plan-generator.md` builds week 1; other modules extend and adapt from there
- **Check-ins**: `daily-check-in.md` → `weekly-check-in.md` → `plan-adjustment.md`
- **Safety Net**: `red-team-checker.md` and `injury-recovery-module.md` catch breakdowns
- **Memory**: `journal-logger.md` stores summaries and patterns for weekly synthesis

You can simulate the entire loop via CLI, notebook, or API integration — or test individual modules in isolation.

---

## 🎯 Philosophy

> *“The job is not to optimize every interval — it’s to keep people running, adapting, and enjoying it long enough to grow.”*

This system is governed by **The Consistency Principle**: a training philosophy that prioritizes long-term health, joy, and motivation over short-term mileage, perfectionism, or performance obsession. Every module reflects this in tone, structure, and fallback logic.

---

## 🛠️ Usage

- Clone the repo and explore each prompt in `prompts/running-coach/`
- Test using OpenAI’s playground, Claude, or a local LLM
- Extend with memory using the `context-template.md`
- Reference `interface-spec.md` if building a UI or agent layer

---

## 📌 Future Work

- Add shoe tracker + rotation system
- Build React frontend (with Vite/Tailwind)
- Connect to weather, race, and trail APIs
- Publish user-facing journaling + progress dashboard
- Port select modules to strength/cycling domains

---

## Author

Created by [Travis Johnson](https://github.com/t4johnson)  
Started: May 2025  
Goal: A polished, real-world portfolio project demonstrating advanced prompt architecture and system thinking
n adjustment
- Motivation tailored to user coaching style
- On-demand check-ins and mental support
- Beginner-friendly running education

Each capability is powered by a reusable, well-documented prompt module.

Built to demonstrate practical use of large language models (LLMs), contextual memory, and user-centered interaction design in fitness and health.

---

## Prompt Modules

| Module                          | Description |
|--------------------------------|-------------|
| `training-plan-generator.md`   | Builds a 7-day structured training plan |
| `plan-adjustment.md`           | Weekly check-in to adjust based on feedback |
| `daily-check-in.md`            | Day-of input prompt to log effort and state |
| `motivation-style.md`          | Provides support in user’s preferred tone |
| `run-explainer.md`             | Explains workouts in clear, plain language |
| `fueling-hydration-planner.md` | Recommends fueling based on run type and weather |
| `run-summary-zero-shot.md`     | Generates post-run summaries with no examples |
| `route-generator.md`           | Suggests routes based on location, plan, and terrain |
| `plan-review-evaluator.md`     | Critiques and improves training plan quality |
| `red-team-checker.md`          | Flags risky, harmful, or unsafe coaching advice |
| `structured-plan-export.md`    | Converts plans to structured JSON or CSV |


---

## Folder Structure

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

## How It Works

The system follows a hybrid interaction model:

- Structured onboarding form gathers core data (experience, goals, availability, terrain, gear, injuries)
- Conversational prompts allow for adaptive check-ins and motivation
- Memory prompts maintain tone, context, and history across sessions

For an overview of system architecture and chaining logic, see [`interface-spec.md`](docs/interface-spec.md).

---

## Philosophy

This project reflects a philosophy of building AI tools that solve *real* problems in practical domains — especially where nuance, personalization, and lived experience matter. The prompts are built on retail, coaching, and endurance sport experience — not just abstract AI ideas.

---

## How to Use or Extend

- Clone the repo and explore each prompt module in isolation
- Test prompts directly in ChatGPT or with the OpenAI API
- Use the `context-template.md` to simulate persistent memory
- Adapt the framework to other domains (e.g., strength training, cycling, nutrition, productivity)
- Optional: build a chatbot interface using the `interface-spec.md` as a guide

---

## Future Plans

- Add gear recommendations and pacing calculators
- Connect to live weather, location, and terrain APIs
- Expand to nutrition, hydration, and injury recovery tracking
- Publish a blog post or walkthrough series

---

## Author

Created by [Travis Johnson](https://github.com/t4johnson)  
Project started: May 2025  
Objective: Publish a portfolio-quality example of applied prompt engineering focused on real-world value
