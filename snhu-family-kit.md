# SNHU — Reach Every Family in Their Language

- **Showcase:** https://app.joinhandshake.com/ai-showcase/projects/3836516
- **Title:** Reach Every Family in Their Language — ZHuddle Multilingual Family-Communication Kit
- **Mission:** Reach Every Family in Their Language (SNHU, Handshake AI Skills Studio)
- **Published:** 2026-11-22
- **Source doc:** https://docs.google.com/document/d/1WOfWperIUOr0ZwlHOCyhDxzu3R94cpK2dnC1uPDNLHs/edit?tab=t.0
- **Cover:** `snhu-family-cover.png` (rendered title card, 1800x1200, 3:2, dark green matching mission 1 — Welcome / Bienvenidos / स्वागत है / స్వాగతం — not a screenshot)

## What was built

A multilingual family-communication kit for ZHuddle, the Python learning platform used by 550+ students at UNT. Three plain-English family messages — welcome, progress update, help guide — each translated into Spanish, Hindi, and Telugu, plus a 12-row verification table, reusable BRIDGE assistant instructions, six behavioral test transcripts, and a second-topic run (practice at home).

## How it was built

Assistant set up in Google Gemini ("ZHuddle Translation Assistant Ready", pcteja2000@gmail.com) with the BRIDGE instructions; three translation requests with audience, purpose, action, deadline, languages, tone, and reading level; every translation reviewed line by line. Four revisions confirmed: Spanish "idioma principal" → "su idioma"; Spanish welcome → neutral "Les damos la bienvenida"; Hindi "छात्र" → neutral "विद्यार्थी" throughout; Telugu welcome opening shortened.

## Testing

All six behavioral tests passed: indirect request, missing details, unclear "soon" deadline, high-consequence suspension/appeal letter (assistant stopped and escalated), message with personal details (assistant refused, required placeholders), date/time mismatch (flagged Sept 8 vs 9 and 8:30 vs 8:00 a.m., marked NOT READY). Second-topic run passed verification in all three languages. All nine Build checkboxes marked complete.

## Notes

- Only verified facts used (ZHuddle, 550+ UNT students; first lessons variables and loops, then functions — from mission 1). No course codes, dates, invented numbers, testimonials, real names, or contact details.
- Sept 8/9 and 8:30/8:00 a.m. figures were example dates from the mission's own stress test, labeled as such in the kit.
- Kit states a fluent speaker should review messages before sending, and high-consequence messages need a qualified human translator.
- One empty duplicate doc created during setup was moved to trash.
