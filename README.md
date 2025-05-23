# Prompt Engineering Library

A curated collection of structured, modular prompt engineering examples for real-world applications. Focused on fitness, coaching, and gear, this repo blends lived experience with AI tooling to create useful, adaptable systems — not just demos.

---

## AI Running Coach

A modular AI-based running coach designed to deliver:

- Personalized training plan generation
- Weekly adaptive plan adjustment
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
