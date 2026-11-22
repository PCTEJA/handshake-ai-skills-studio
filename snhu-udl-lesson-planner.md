# SNHU — Create a Universal Design Lesson Planner

- **Showcase:** https://app.joinhandshake.com/ai-showcase/projects/3836443
- **Title:** Universal Design Lesson Planner — UDL Lesson Plans for Introductory Python
- **Mission:** Create a Universal Design Lesson Planner (SNHU, Handshake AI Skills Studio)
- **Published:** 2026-11-22
- **Source doc:** https://docs.google.com/document/d/1yP0gS-y6by8rDzrXeTnOCsYEu3vCSF4fyQKP8mOcvNs/edit
- **Cover:** `snhu-udl-cover.png` (rendered title card showing the UDL options menu, 1800x1200, 3:2 — not a screenshot)

## What was built

A Universal Design Lesson Planner assistant set up in Google Gemini (signed in as pcteja2000@gmail.com) with the mission's UDL system prompt, used to plan two complete 60-minute introductory Python lessons:

- **Lesson 1 — Variables and Loops** (mixed class: English language learners, ADHD, a screen-reader user, a student with dyslexia)
- **Lesson 2 — Functions**

Each lesson has objectives, materials, timed steps, assessment options (Code Builder / Code Analyst / Logic Architect), teacher reflection prompts, and a UDL lens options menu (Lesson Goal, Engagement, Representation, Action and Expression, Materials, Assessment Options).

## Testing

- Barrier inspection found one flaw in the first draft (visual-only accommodations — sticky notes, index cards, "hold up fingers" check) and rewrote those steps with multi-sensory alternatives.
- A stress test as a first-time coder using a screen reader joining 12 minutes late exposed five failure points and led to four structural fixes: Quick-Start & Late-Arrival Hub, static snapshot files instead of live-typing, a 3-sentence mental-model recap, silent visual/text checkpoints instead of audible chimes.
- Lesson 2 confirmed the assistant reuses across topics.

## Notes

- Gemini's Gems manager was unavailable (gemini.google.com/gems returned 404, no Gems entry in sidebar), so the assistant was set up in a Gemini chat with the instructions as its first message — same behavior, recorded in the doc.
- In the Google Doc, the two UDL lens tables render with only the header and Lesson Goal row as a grid; remaining rows appear as labeled bullet lists (Gemini-to-Docs export limitation, persisted after regenerating with export-safe cells). All options content is present and complete.
- Only real, verified facts used (Teja, creator of the ZHuddle Python learning platform used by 550+ UNT students). No course codes, dates, student numbers beyond 550+, or testimonials invented.
