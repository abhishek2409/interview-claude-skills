# Mock Interview Generator Skill

Generate realistic, personalized mock interviews for software engineers. Practice for interviews at Google, Meta, Amazon, Microsoft, and other top tech companies.

---

## What's in This Repo

| File / Folder | Purpose |
|---|---|
| [core-skill/SKILL.md](core-skill/SKILL.md) | The main skill definition — start here |
| [system-prompts/](system-prompts/) | Individual prompts for each interview round type |
| [examples/example-test-case.md](examples/example-test-case.md) | Google L4 interview walkthrough |
| [examples/advanced-example-full-day-conversational.md](examples/advanced-example-full-day-conversational.md) | Full interview day with realistic dialogue |
| [examples/mock-interview-skill-design.md](examples/mock-interview-skill-design.md) | Architecture & roadmap |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to contribute |

---

## Quick Start

### Option 1: Use in Claude (Easiest)

1. Copy the contents of [core-skill/SKILL.md](core-skill/SKILL.md)
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

### Option 2: Use in Claude Code (CLI)

```bash
npx claude-code <<EOF
Create a mock interview for:
- Company: Google
- Role: Senior Frontend Engineer L4
- Resume: [your resume]
- Job: [job description]
- Round: System Design, 60 min, Hard
EOF
```

### Option 3: Self-Host (Advanced)

Clone the repo, copy the system prompts into your own Claude API integration, and use the skill definitions to drive your own interview UI or automation.

---

## Features

- **Company-Aware** — Google asks different questions than Meta. We know that.
- **Resume-Personalized** — Get questions that reference *your* experience, not generic ones.
- **Multiple Round Types** — Tech Screen → System Design → Behavioral → Coding (expandable)
- **Difficulty Levels** — Easy/Medium/Hard/Expert calibrated for each company & level
- **Conversational Follow-Ups** — Optional dynamic follow-ups for realistic practice
- **Answer Frameworks** — Learn *how* to answer, not just *what* to answer
- **Zero Setup** — Use directly in Claude, no API keys or installs needed

---

## Interview Types

### Tech Screen (45-60 min)
Quick assessment of coding skills and problem-solving.

Covers: React component design & optimization, JavaScript algorithms, Browser APIs, State management, Code quality

**Best for:** All engineering levels

### System Design (60-90 min)
Architectural thinking, trade-off analysis, scalability.

Covers: Frontend architecture, API design & optimization, Caching strategies, Real-time systems, Scaling & performance

**Best for:** L4/L5/Staff+ engineers

### Behavioral (30-45 min)
Teamwork, leadership, impact, culture fit.

Covers: Technical influence & ownership, Mentorship & team building, Learning from mistakes, Handling conflict & ambiguity

**Best for:** All levels, especially manager/staff/principal roles

### Full Day Simulation
Runs all three rounds in sequence with realistic pacing, different interviewers per round, and an end-of-day assessment with offer likelihood.

### Coding (coming soon)
Algorithm & problem-solving challenges (LeetCode-style).

---

## Usage Examples

### Basic

```
Company: Google
Role: Senior Frontend Engineer
Resume: 12 years experience, React expert, built micro-frontends at Expedia and Paytm
Interview Round: Tech Screen, 45 min, Medium difficulty
```

Result: 2-3 technical questions with answer frameworks and follow-ups.

### Advanced (Full Day)

```
Company: Google
Role: Senior Frontend Engineer (L4)
Resume: [full resume]
Job Description: [full job description]
Interview Rounds:
  1. Tech Screen (45 min, Medium)
  2. System Design (60 min, Hard)
  3. Behavioral (45 min, Medium)
Customization:
  - Follow-Ups: Moderate
  - Interviewer Style: Conversational
```

Result: 3 full interview rounds, each fully customized, with realistic dialogue and a final assessment.

---

## Company-Specific Insights

### Google
**Values:** Scale thinking, technical depth, influence without authority, pragmatism
**Focus areas:** Web Vitals & performance, real-time systems, distributed systems, accessibility
**Tips:** Always ask "What if this is 10x bigger?" — discuss monitoring & observability

### Meta
**Values:** Move fast, iterate, impact on billions of users, product & business thinking
**Focus areas:** Real-time feed systems, client-server sync, performance at scale

### Amazon
**Values:** Customer obsession, leadership principles, ownership & accountability, bias to action
**Focus areas:** E-commerce architecture, scalability, operations & reliability

### Microsoft
**Values:** Collaboration & inclusion, technical excellence, growth mindset, cloud-native thinking

---

## How to Practice

1. Pick a target company & role
2. Generate a mock interview (tech screen is easiest to start)
3. Practice out loud — record yourself if possible
4. Evaluate your answer: Did you explain your thinking? Was it grounded in real experience? Did you mention metrics/outcomes?
5. Regenerate with different questions, see if you improve
6. Move to harder difficulty or a different round type

**Pro tip:** Practice the same round 3-5 times. Answers get stronger, more concise, and more confident each time.

---

## How to Contribute

We're looking for:
- New question types (Coding, Product Design, etc.)
- Company-specific improvements (more detailed insights, real questions)
- Translations (Chinese, Spanish, Hindi, etc.)
- Bug reports & feature requests
- Success stories (interviews you got offers from!)

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## Limitations

**What this is:**
- A practice tool to build confidence & get feedback
- Representative of real interview question styles
- A starting point for answer frameworks

**What this is NOT:**
- A guarantee you'll get certain questions
- A substitute for studying data structures & algorithms
- A replacement for real interview feedback from hiring managers

---

## Roadmap

### v1 (Current)
- [x] Tech Screen, System Design, Behavioral rounds
- [x] Difficulty levels (Easy → Expert)
- [x] Conversational follow-ups
- [x] Company-specific context
- [x] Full-day simulation

### v2
- [ ] Coding interview questions (LeetCode-style)
- [ ] Product design interviews
- [ ] Interactive web UI
- [ ] Export to PDF/Markdown
- [ ] Answer evaluation & scoring

### v3
- [ ] Video interview simulation
- [ ] Speech-to-text practice
- [ ] Performance scoring & analytics
- [ ] Integration with interview platforms

---

## FAQ

**Will these questions exactly match what I'll see in a real interview?**
No, interviews vary. But the style, difficulty, and focus areas are representative. Think of it as a realistic simulation, not a prediction.

**Can I use this to prepare for non-tech interviews?**
The skill is optimized for software engineering interviews but could be adapted for product management, design, or operations. Contributions welcome.

**Is this free?**
Yes. The skill files are open-source and free to use. Normal Claude API or subscription costs apply if you use it through Claude.

**Can I contribute new questions or insights?**
Absolutely — open an issue or submit a PR. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Support

- Questions? Open an issue on GitHub
- Found a bug? Please report it
- Like this? Star the repo and share it

---

## License

MIT — use freely, credit appreciated.
