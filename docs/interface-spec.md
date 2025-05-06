# AI Running Coach Interface Specification

## Overview

This project uses a **hybrid interaction model**: a combination of structured forms and conversational AI. Users begin by filling out a short onboarding form to generate a personalized training plan, and then transition into a flexible chat-based interaction with the coach. This approach allows for both reliable data collection and dynamic support.

## User Flow

| Step | Interaction | Triggered Prompt Module |
|------|-------------|--------------------------|
| 1. Onboarding | Form: name, goal, timeline, terrain, gear, coaching style | `training-plan-generator.md` |
| 2. Training Plan | AI-generated plan delivered via chat | — |
| 3. Daily Check-Ins | User sends updates as needed (chat): “Felt great today” / “Skipped long run” | `daily-check-in.md` |
| 4. Weekly Check-In | AI requests status update (scheduled or user-initiated) | `plan-adjustment.md` |
| 5. Motivation Support | Triggered by tone or request: “Feeling off” / “Need a boost” | `motivation-style.md` |
| 6. Run Type Education | Triggered when user asks “What’s a tempo run?” or similar | `run-explainer.md` |
| 7. Loop | User continues weekly + daily interactions | Prompt chain managed by backend |

## Prompt Routing Logic

- Form responses are used to populate context for the training plan prompt.
- Chat inputs are monitored for keywords, phrases, or emotional signals to trigger appropriate modules:
  - Missed workout → `plan-adjustment.md`
  - “What’s X?” → `run-explainer.md`
  - “Tired today” or “Need motivation” → `motivation-style.md`
  - General update → `daily-check-in.md`

## Future Implementation Notes

- Memory can be simulated with shared context fields (`context-template.md`) or managed with thread-based memory via OpenAI’s Assistants API.
- Could use LangChain for routing and tool integration if advanced capabilities are needed (e.g., connecting to weather APIs, race calendars).
- UI could be built with:
  - Web (Next.js, React + GPT API)
  - Mobile (React Native or Swift)
  - No-code front ends like Bubble or Glide for rapid testing

This spec defines how the AI modules will work together within a single user experience.
