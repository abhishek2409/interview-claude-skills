# Mock Interview Generator Skill - Design Document

## Overview
A reusable, shareable AI skill that generates contextual mock interviews for software engineers based on:
- Company name & context
- Job description & level
- User's resume
- Interview round type (tech screen, system design, behavioral, etc.)

---

## Inputs

### Required Fields
```json
{
  "company": {
    "name": "Google",
    "domain": "Search/Cloud/Android (optional context)"
  },
  "jobDescription": {
    "title": "Senior Frontend Engineer",
    "level": "L4/L5/Staff/Principal",
    "keyResponsibilities": "...",
    "skills": ["React", "System Design", "TypeScript"]
  },
  "resumeContent": "... full resume text or key highlights ...",
  "interviewRound": {
    "type": "tech-screen | system-design | behavioral | coding",
    "duration": "45-60 minutes",
    "focus": "frontend-specific | full-stack | leadership | etc"
  }
}
```

### Optional Customization
```json
{
  "difficulty": "easy | medium | hard | expert",
  "depth": "surface | intermediate | deep",
  "questionCount": 3-5 (default: 4),
  "followUpDepth": "none | light | moderate | heavy",
  "style": "traditional | case-study | collaborative | adversarial"
}
```

---

## Outputs

### Interview Session Format
```
[MOCK INTERVIEW]
Company: Google
Role: Senior Frontend Engineer (L4)
Round: System Design - 45 min
Difficulty: Hard

---

INTERVIEWER CONTEXT:
- Focused on your experience with [...]
- Will probe deeper on [...]
- Evaluating: [skill1, skill2, skill3]

---

QUESTION 1: [Opening question based on your resume/role]
[Follow-up if enabled]
[Expected answer framework]
[Interviewer tips]

QUESTION 2: ...
...

---

INTERVIEW TIPS:
- Focus on [X]
- Common pitfalls: [X, Y]
- How to stand out: [X, Y, Z]
```

---

## Skill Features

### v1 (MVP)
- [ ] Basic mock interview generation
- [ ] Resume-aware questioning
- [ ] Company-specific context
- [ ] Round type customization
- [ ] Difficulty levels

### v2 (Enhanced)
- [ ] Interactive web UI for input collection
- [ ] Multi-round generation (all rounds at once)
- [ ] Follow-up questions & conversational mode
- [ ] Answer evaluation & feedback
- [ ] Export to PDF/Markdown

### v3 (Advanced)
- [ ] Scoring rubric & grading
- [ ] Video interview simulation (with speech-to-text)
- [ ] Analytics (strengths/weaknesses)
- [ ] Personalized improvement plan
- [ ] Integration with interview prep platforms

---

## Technical Architecture

### Skill Components
1. **SKILL.md** - Core prompt engineering + instructions
2. **system-prompts/** - Specialized prompts for each round type
3. **examples/** - Sample interviews, test cases
4. **web-ui/** - Interactive HTML/React interface (optional)
5. **github-template/** - Setup guide for sharing

### Key Dependencies
- Claude API (for interview generation)
- Optional: Node.js (for CLI version)
- Optional: React/Next.js (for web UI)

---

## GitHub Structure

```
mock-interview-skill/
├── SKILL.md                          # Anthropic skill definition
├── system-prompts/
│   ├── base-interviewer.md
│   ├── tech-screen.md
│   ├── system-design.md
│   ├── behavioral.md
│   └── coding.md
├── examples/
│   ├── sample-interviews.json
│   └── test-cases.json
├── web-ui/                           # Optional interactive UI
│   ├── index.html
│   ├── app.js
│   └── styles.css
├── cli/                              # Optional CLI version
│   └── mock-interview.js
├── README.md
├── CONTRIBUTING.md
└── LICENSE
```

---

## Usage Examples

### As a Claude Skill (Direct)
```
"I want a mock interview for a Senior Frontend Engineer role at Google.
Here's my resume: [resume]
Job description: [job description]
Round: System Design, 45 minutes, Hard difficulty"
```

### As a Web UI
1. Fill company, job description, resume
2. Select round type & difficulty
3. Click "Generate Interview"
4. Get interactive mock interview

### As a CLI (future)
```bash
node mock-interview.js \
  --company "Google" \
  --role "Senior Frontend Engineer" \
  --resume ./resume.txt \
  --round "system-design" \
  --difficulty "hard"
```

---

## Success Metrics

- [ ] Interview questions are relevant to role + resume
- [ ] Difficulty level is appropriate
- [ ] Follow-ups feel natural + realistic
- [ ] Answer frameworks are helpful but not spoiler-ish
- [ ] Users report increased confidence for real interviews
- [ ] GitHub stars & community contributions

---

## Timeline

- **Week 1**: Design + skill-creator script
- **Week 2**: System prompts + test cases
- **Week 3**: Eval + iteration
- **Week 4**: Web UI + GitHub setup
- **Week 5**: Documentation + launch

