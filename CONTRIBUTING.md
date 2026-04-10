# Contributing to Mock Interview Generator

We love contributions! This guide will help you contribute effectively.

---

## Ways to Contribute

### Add New Interview Questions

**Complexity:** Medium | **Time:** 30-60 min

1. Pick a company + role you're familiar with
2. Write 1-3 realistic interview questions for a specific round type
3. Include answer frameworks & follow-ups
4. Test with someone in that field
5. Submit a PR with your questions

**Template:**

```markdown
## [Company] - [Round Type]

**Role:** [Senior Frontend Engineer / Staff Engineer / Engineering Manager]

**Question 1:** [Clear, specific question]
- **Why this matters:** [Why this question is asked]
- **Expected approach:** [How to structure answer]
- **Common mistakes:** [Pitfalls to avoid]
- **How to stand out:** [What impresses interviewers]

**Follow-up:** [Probing question]
```

---

### Improve Company-Specific Context

**Complexity:** Low | **Time:** 15-30 min

Each company has unique interview styles and values. Help us capture these nuances:

- What questions does [Company] consistently ask?
- What technologies do they prefer?
- What are their stated values (Google's OKRs, Amazon's leadership principles)?
- What red flags do interviewers look for?

---

### Report Issues

Found something wrong? Questions that don't fit? Unclear guidance?

**Please include:**
- What you tried
- What you expected
- What actually happened
- Your context (role, company, difficulty level)

---

### Share Success Stories

Did this skill help you land an interview or an offer? Open an issue with the `success-story` label and tell us:

- Which round did you practice with?
- What questions came up in your real interview?
- What was most helpful?
- Any feedback for improvement?

---

### Translations

Help make this accessible globally!

1. Copy `core-skill/SKILL.md` and rename to `SKILL.[language].md`
2. Translate the entire file
3. Submit a PR

Languages needed:
- [ ] Spanish
- [ ] Hindi
- [ ] Chinese Simplified
- [ ] Japanese

---

### Build Tools & Integrations

Help us build tools around this skill:

- **Web UI** — React app to collect inputs and display interviews
- **CLI** — Node.js command-line tool
- **PDF Export** — Generate printable interview guides
- **Slack Bot** — Daily mock interview questions

---

## Development Setup

### Prerequisites

- Git & GitHub account
- Claude (API key optional, can use claude.ai)
- A text editor

### Local Setup

```bash
# Clone the repo
git clone https://github.com/abhishek2409/interview-claude-skills.git
cd interview-claude-skills

# Create a new branch for your work
git checkout -b add-amazon-questions

# Make your changes
# (Edit SKILL.md, add company profiles, etc.)

# Commit & push
git add .
git commit -m "Add Amazon-specific interview questions"
git push origin add-amazon-questions

# Open a PR on GitHub
```

---

## Code of Conduct

- **Be respectful** — We're all learning
- **Be constructive** — Feedback should help people improve
- **Be inclusive** — Make this useful for everyone globally
- **Give credit** — Acknowledge sources, cite studies, credit contributors

---

## Review Process

1. You submit a PR with your contribution
2. Maintainers review — we test the questions, check for accuracy
3. Community feedback — others comment with suggestions
4. Iteration — you make adjustments if needed
5. Merge — once approved, your contribution goes live

**Average review time:** 3-7 days

---

## Tips for Successful Contributions

**Do this:**
- Test your questions with someone in the target field
- Reference real interview experiences
- Include metrics or data where relevant
- Break large contributions into smaller PRs

**Avoid this:**
- Generic questions that could apply to any company
- Actual leaked interview questions (privacy)
- Unsourced claims
- Large PRs without prior discussion — open an issue first

---

## What We're Looking For

**High priority:**
- System design questions for emerging roles (ML Engineer, DevOps, QA)
- More detailed company profiles
- Interactive features (web UI, scoring system)

**Medium priority:**
- Coding interview questions (LeetCode-style)
- Product design interviews
- More behavioral questions
- Translations

---

## FAQ

**Q: Can I contribute if I'm not an expert interviewer?**

A: Absolutely. If you've done a few interviews, you have valuable perspective. We'll help refine your questions during review.

**Q: Do I need to contribute code?**

A: No. We welcome content, documentation, feedback, and community help.

**Q: How long does review take?**

A: Most PRs are reviewed within 3-7 days.

**Q: Can I become a maintainer?**

A: Yes — reach out after your 2nd or 3rd contribution.

---

## Thank You!

Contributing to open source takes time and energy. We genuinely appreciate you helping make interview prep better for everyone.
