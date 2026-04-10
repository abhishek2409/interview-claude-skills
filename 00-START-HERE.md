# Mock Interview Generator Skill — Quick Start

A Claude skill that generates realistic, personalized mock interviews for software engineers. Practice for interviews at Google, Meta, Amazon, Microsoft, and other top tech companies.

---

## What's in This Repo

### Core Skill
- [core-skill/SKILL.md](core-skill/SKILL.md) — The main skill definition. Copy this into Claude to get started.

### System Prompts
- [system-prompts/system-prompt-tech-screen.md](system-prompts/system-prompt-tech-screen.md) — Coding & architecture screening
- [system-prompts/system-prompt-system-design.md](system-prompts/system-prompt-system-design.md) — Architecture design problems
- [system-prompts/system-prompt-behavioral.md](system-prompts/system-prompt-behavioral.md) — Teamwork & leadership questions
- [system-prompts/system-prompt-conversational.md](system-prompts/system-prompt-conversational.md) — Realistic dialogue engine
- [system-prompts/system-prompt-full-day-interview.md](system-prompts/system-prompt-full-day-interview.md) — Multi-round full-day simulation

### Examples
- [examples/example-test-case.md](examples/example-test-case.md) — Google L4 interview walkthrough
- [examples/advanced-example-full-day-conversational.md](examples/advanced-example-full-day-conversational.md) — Full interview day with realistic dialogue
- [examples/mock-interview-skill-design.md](examples/mock-interview-skill-design.md) — Architecture & roadmap

---

## Quick Start

1. Open [core-skill/SKILL.md](core-skill/SKILL.md) and copy its contents
2. Paste it into [claude.ai](https://claude.ai) as a Project instruction or directly into a conversation
3. Tell Claude:
   ```
   Generate a mock interview for:
   - Company: Google
   - Role: Senior Frontend Engineer L4
   - Resume: [paste your resume]
   - Rounds: Full day (Tech Screen → System Design → Behavioral)
   - Difficulty: Medium/Hard/Hard, Heavy follow-ups, Conversational style
   ```
4. Practice, get feedback, iterate

For more detail, see [README.md](README.md).
