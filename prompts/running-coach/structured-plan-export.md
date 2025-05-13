# Prompt: Weekly Training Plan to Structured Output (JSON or CSV)

**Category**: Running Coach / Developer Tooling
**Module**: Data Export & Integration
**Goal**: Convert a human-readable weekly training plan into structured JSON or CSV format.
**Model Used**: GPT-4
**Author**: Travis Johnson
**Version**: 1.0
**Status**: In Progress
**Date**: 2025-05-10

---

## Prompt Template

You are an AI running coach assistant. Convert the weekly training plan below into structured data so it can be exported or used in external tools.

For each day in the plan, return the following fields:

* `date`
* `day`
* `run_type` (e.g., easy, long, speed, rest, cross-train)
* `distance_miles` or `duration_minutes`
* `effort_level` (easy, moderate, hard)
* `notes`
* `tag` (optional: e.g., “build”, “recovery”, “race prep”, “speedwork”)
* `warning` (e.g., “back-to-back hard efforts”, “missing rest day”)

### Additional Instructions:

* If only weekdays are provided, infer full dates using the provided `start_date`.
* If a field is missing in the input, leave it blank but maintain structure.
* If `"CSV"` is mentioned, respond in CSV format. Otherwise, respond in JSON.
* Return **only the structured data**, no commentary.

---

## Example Input

**Start date:** May 13, 2025
**Format:** JSON

```
- Mon: Rest
- Tue: 6 miles easy, stay relaxed
- Wed: 5 x 3 minutes hard effort, full recovery jogs
- Thu: 4 miles easy, with 4 strides
- Fri: Cross-train 45 min
- Sat: Long run, 9 miles steady
- Sun: Optional 3 miles or walk
```

---

## Example Output (JSON)

```json
[
  {"date": "2025-05-13", "day": "Mon", "run_type": "rest", "distance_miles": "", "duration_minutes": "", "effort_level": "easy", "notes": "Rest day", "tag": "recovery", "warning": ""},
  {"date": "2025-05-14", "day": "Tue", "run_type": "easy", "distance_miles": 6, "duration_minutes": "", "effort_level": "easy", "notes": "Stay relaxed", "tag": "base", "warning": ""},
  {"date": "2025-05-15", "day": "Wed", "run_type": "speed", "distance_miles": "", "duration_minutes": "", "effort_level": "hard", "notes": "5 x 3 min hard, full recovery jogs", "tag": "speedwork", "warning": "Back-to-back hard efforts if Friday is intense"},
  {"date": "2025-05-16", "day": "Thu", "run_type": "easy", "distance_miles": 4, "duration_minutes": "", "effort_level": "easy", "notes": "Include 4 strides", "tag": "base", "warning": ""},
  {"date": "2025-05-17", "day": "Fri", "run_type": "cross-train", "distance_miles": "", "duration_minutes": 45, "effort_level": "moderate", "notes": "", "tag": "maintenance", "warning": ""},
  {"date": "2025-05-18", "day": "Sat", "run_type": "long", "distance_miles": 9, "duration_minutes": "", "effort_level": "moderate", "notes": "Steady pace", "tag": "long run", "warning": ""},
  {"date": "2025-05-19", "day": "Sun", "run_type": "easy", "distance_miles": 3, "duration_minutes": "", "effort_level": "easy", "notes": "Optional or walk", "tag": "recovery", "warning": ""}
]
```

---

## Example Output (CSV)

```csv
date,day,run_type,distance_miles,duration_minutes,effort_level,notes,tag,warning
2025-05-13,Mon,rest,,,,Rest day,recovery,
2025-05-14,Tue,easy,6,,easy,Stay relaxed,base,
2025-05-15,Wed,speed,,,hard,"5 x 3 min hard, full recovery jogs",speedwork,"Back-to-back hard efforts if Friday is intense"
2025-05-16,Thu,easy,4,,easy,Include 4 strides,base,
2025-05-17,Fri,cross-train,,45,moderate,,maintenance,
2025-05-18,Sat,long,9,,moderate,Steady pace,long run,
2025-05-19,Sun,easy,3,,easy,Optional or walk,recovery,
```

---

## Related Prompts

* `plan-adjustment.md` — This can use structured output to compare weekly modifications
* `plan-review-evaluator.md` — Can flag risky structures before formatting
* `run-summary-zero-shot.md` — Could be appended to notes fields in daily records
