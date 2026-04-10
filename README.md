# Mock Interview Generator Skill

Generate realistic, personalized mock interviews for software engineers. Practice for interviews at Google, Meta, Amazon, Microsoft, and other top tech companies.

**Status**: ✅ Alpha (Core skill complete, community contributions welcome)

---

## Features

🎯 **Company-Aware**: Google asks different questions than Meta. We know that.

📋 **Resume-Personalized**: Get questions that reference *your* experience, not generic ones.

🔄 **Multiple Round Types**: Tech Screen → System Design → Behavioral → Coding (expandable)

⚙️ **Difficulty Levels**: Easy/Medium/Hard/Expert calibrated for each company & level.

💬 **Follow-Ups**: Optional conversational follow-ups for realistic practice.

🎓 **Answer Frameworks**: Learn *how* to answer, not just *what* to answer.

🚀 **Zero Setup**: Use directly in Claude, or integrate with your own AI app.

---

## Quick Start

### Option 1: Use in Claude (Easiest)

1. Copy the [SKILL.md](./SKILL.md) content
2. Share it with Claude or upload as a project skill
3. Tell Claude: 
   ```
   I want a mock interview for Senior Frontend Engineer at Google.
   Here's my resume: [paste resume]
   Job description: [paste job description]
   Round: System Design, 60 minutes, Hard difficulty
   ```
4. Get your interview, practice answering, iterate

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

See [CONTRIBUTING.md](./CONTRIBUTING.md) for setup instructions.

---

## Interview Types

### 🔧 Tech Screen (45-60 min)
Quick assessment of coding skills and problem-solving.

**Questions cover:**
- React component design & optimization
- JavaScript algorithms
- Browser APIs
- State management
- Code quality

**Best for:** All engineering levels

---

### 🏗️ System Design (60-90 min)
Architectural thinking, trade-off analysis, scalability.

**Questions cover:**
- Frontend architecture
- API design & optimization
- Caching strategies
- Real-time systems
- Scaling & performance

**Best for:** L4/L5/Staff+ engineers

---

### 💬 Behavioral (30-45 min)
Teamwork, leadership, impact, culture fit.

**Questions cover:**
- Technical influence & ownership
- Mentorship & team building
- Learning from mistakes
- Handling conflict & ambiguity
- Motivation & impact

**Best for:** All levels, especially for manager/staff/principal roles

---

### 💻 Coding (60-90 min)
Algorithm & problem-solving challenges (coming soon).

---

## Usage Examples

### Basic Interview

```
Company: Google
Role: Senior Frontend Engineer
Resume: 
  12 years experience, React expert, built micro-frontends
  at Expedia and Paytm
Interview Round: Tech Screen, 45 min, Medium difficulty
```

**Result:** 2-3 technical questions with answer frameworks and follow-ups.

---

### Advanced Interview

```
Company: Google
Role: Senior Frontend Engineer (L4)
Level: L4
Resume: [full resume]
Job Description: [full job description]
Interview Rounds: 
  1. Tech Screen (45 min, Medium)
  2. System Design (60 min, Hard)
  3. Behavioral (45 min, Medium)
Customization:
  - Difficulty: Medium/Hard/Hard
  - Follow-Ups: Moderate
  - Focus: Frontend with system design thinking
```

**Result:** 3 full interview rounds, each fully customized, ready to practice.

---

## Company-Specific Insights

### Google 🔴

**What they value:**
- Scale thinking (how does this work for billions?)
- Technical depth in your specialty
- Influence & leadership without authority
- Pragmatism (use proven tech)

**Common focus areas:**
- Web Vitals & performance
- Real-time systems
- Distributed systems
- Accessibility

**Tips:**
- Always ask "What if this is 10x bigger?"
- Reference your systems thinking
- Discuss monitoring & observability

---

### Meta 🔵

**What they value:**
- Move fast, iterate
- Impact on billions of users
- Building culture & mentoring
- Product & business thinking

**Common focus areas:**
- Real-time feed systems
- Client-server sync
- Performance at scale
- User experience

---

### Amazon 🟠

**What they value:**
- Customer obsession
- Leadership principles
- Ownership & accountability
- Bias to action

**Common focus areas:**
- E-commerce architecture
- Scalability
- Operations & reliability

---

### Microsoft 🔷

**What they value:**
- Collaboration & inclusion
- Technical excellence
- Growth mindset
- Cloud-native thinking

---

## How to Practice

1. **Pick a target company & role**
2. **Generate a mock interview** (tech screen is easiest to start)
3. **Practice out loud** (record yourself)
4. **Evaluate your answer**:
   - Did you answer the question?
   - Did you explain your thinking?
   - Was your answer grounded in real experience?
   - Did you mention relevant metrics/outcomes?
5. **Regenerate** (get different questions, see if you improve)
6. **Move to harder difficulty** or different round type

**Pro tip:** Practice the same round 3-5 times. You'll notice your answers get stronger, more concise, and more confident.

---

## How to Contribute

We're looking for:
- ⭐ **New question types** (Coding, Product Design, etc.)
- 🏢 **Company-specific improvements** (more detailed insights, common questions)
- 🌍 **Translations** (Chinese, Spanish, Hindi, etc.)
- 🐛 **Bug reports** & feature requests
- 💡 **Success stories** (interviews you got offers from!)

See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

---

## Limitations & Disclaimers

✅ **What this is:**
- A practice tool to build confidence & get feedback
- Representative of real interview question styles
- A starting point for answer frameworks

❌ **What this is NOT:**
- A guarantee you'll get certain questions
- A substitute for studying data structures & algorithms
- A replacement for real interview feedback from hiring managers

---

## Roadmap

### v1 (Current) ✅
- [x] Tech Screen questions
- [x] System Design questions
- [x] Behavioral questions
- [x] Difficulty levels
- [x] Follow-up questions
- [x] Company-specific context

### v2 (Q2)
- [ ] Coding interview questions (LeetCode-style)
- [ ] Product design interviews
- [ ] Interactive web UI
- [ ] Multi-round generator
- [ ] Export to PDF/Markdown
- [ ] Answer evaluation & scoring

### v3 (Q3)
- [ ] Video interview simulation
- [ ] Speech-to-text practice
- [ ] Performance scoring & analytics
- [ ] Personalized improvement plan
- [ ] Integration with interview platforms (Interviewing.io, Pramp)

---

## FAQ

**Q: Will these questions exactly match what I'll see in a real interview?**

A: No, interviews vary. But the *style*, *difficulty*, and *focus areas* are representative. Think of it as a realistic simulation, not a prediction.

---

**Q: Can I use this to prepare for non-tech interviews?**

A: The skill is optimized for software engineering interviews. It could be adapted for product management, design, or operations roles. Contributions welcome!

---

**Q: How often are questions updated?**

A: As companies' tech stacks change and interview practices evolve, we update the skill. The core framework is stable, but questions improve continuously.

---

**Q: Is this free?**

A: Yes. The SKILL.md is open-source and free to use. If you use it through Claude or Claude Code, normal API/subscription costs apply.

---

**Q: Can I contribute new questions or insights?**

A: Absolutely! See [CONTRIBUTING.md](./CONTRIBUTING.md). We credit all contributors.

---

## Examples

See [example-test-case.md](./example-test-case.md) for a full walkthrough of an interview from start to finish (mock interview for Abhishek's Google interview prep).

---

## Support

- 📧 Questions? Open an issue on GitHub
- 💬 Feedback? Let's chat — PRs welcome
- 🐛 Found a bug? Please report it
- ⭐ Like this? Star the repo and share it!

---

## License

MIT — Use freely, credit appreciated!

---

## Acknowledgments

Built with ❤️ by engineers who've done hundreds of interviews. Special thanks to the community for feedback and contributions.

---

## Call to Action

**Ready to practice?**

1. Star ⭐ this repo
2. Fork it or copy the SKILL.md
3. Generate your first mock interview
4. **Tell us how it went** — we'd love to hear about your offer! 🎉

