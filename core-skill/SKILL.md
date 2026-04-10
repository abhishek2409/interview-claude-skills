---
name: mock-interview-generator
description: Generate highly customizable, realistic mock interviews for software engineers. Supports single or multi-round interviews (tech screen → system design → behavioral), fully conversational with dynamic follow-ups, and complete customization (difficulty, depth, question count, follow-up style). Use this skill whenever the user wants to practice interviews, prepare for a specific company/role, or simulate a full interview day. Triggers include "mock interview", "practice interview", "interview prep", "interview questions", "interview simulation", "full day interview", or when the user provides job descriptions + resume. Always use this skill for ANY interview practice, regardless of company, level, round type, or customization needs.
---

# Mock Interview Generator - Advanced Edition

Generate highly realistic, fully conversational mock interviews tailored to a specific company, role, and interview round(s). This skill produces contextual questions, answer frameworks, and dynamic follow-ups that simulate real interview conversations. Support both single-round and full-interview-day scenarios with complete customization.

## When to Use This Skill

Use this skill whenever:
- User wants to practice for an interview at a specific company
- User provides a job description + resume + wants interview questions
- User asks for "mock interview", "interview prep", "practice round", or similar
- User wants to prepare for a specific round type (tech screen, system design, behavioral, coding)
- User wants realistic interview questions aligned with their background and target role

## How It Works

This skill acts as a context-aware interviewer. You provide:
1. **Company** - Target company name & context
2. **Job Description** - Role title, level, key responsibilities, required skills
3. **Resume** - Your background (as text, or key highlights)
4. **Interview Round** - Type (tech-screen, system-design, behavioral, coding) and duration
5. **Customization** (optional) - Difficulty level, depth, number of questions, follow-up style

The skill generates:
- Realistic, role-aligned interview questions
- Follow-up questions that probe deeper
- Expected answer frameworks & tips
- Common pitfalls to avoid
- How to stand out for this specific role

---

## Interview Round Types

### Tech Screen (45-60 min)
- Quick coding problems or architectural discussions
- Screening for competency & communication
- Focus: Problem-solving, coding clarity, explanation

### System Design (60-90 min)
- Design a system, feature, or architecture
- Shows breadth of knowledge & decision-making
- Focus: Trade-offs, scalability, real-world constraints

### Behavioral (30-45 min)
- Team collaboration, leadership, challenges overcome
- Assesses culture fit & soft skills
- Focus: Stories, impact, lessons learned

### Coding (60-90 min)
- LeetCode-style problems or real-world coding challenges
- Tests algorithms, code quality, optimization
- Focus: Clean code, edge cases, optimization

### Product/Design (45-60 min)
- Design a product, feature, or workflow
- Assesses end-to-end thinking
- Focus: User insights, trade-offs, metrics

---

## Customization Options

### Difficulty Level
- **Easy** - Warm-up questions, straightforward topics
- **Medium** - Standard questions, typical follow-ups
- **Hard** - Challenging edge cases, deep technical probing
- **Expert** - Industry-leading difficulty, research-level topics

### Depth
- **Surface** - Broad overview, quick answers (10-15 min per question)
- **Intermediate** - Standard depth, balanced (15-20 min per question)
- **Deep** - Exhaustive exploration, rabbit holes (20-30 min per question)

### Follow-Up Style
- **None** - Just questions, no follow-ups
- **Light** - 1-2 follow-ups per question
- **Moderate** - 2-3 follow-ups with probing
- **Heavy** - Dynamic conversation, continuous probing

---

## Input Format

Provide information in this format (structured or conversational):

### Required Fields
```
Company: [Company Name]
Role/Title: [e.g., Senior Frontend Engineer]
Resume: [Your background, key achievements, relevant experience]
Interview Round(s): [Single round OR multi-round below]
```

### Optional Customization (Full Control)

#### Single Round
```
Round: [tech-screen/system-design/behavioral/coding]
Duration: [45/60/90 minutes]
```

#### Multi-Round (Full Interview Day)
```
Rounds:
  1. Tech Screen (45 min, Medium difficulty, Moderate follow-ups)
  2. System Design (60 min, Hard difficulty, Heavy follow-ups)
  3. Behavioral (45 min, Medium difficulty, Light follow-ups)
```

#### Difficulty Level (Controls question complexity)
```
Difficulty: 
  - Easy (warm-up, straightforward topics)
  - Medium (standard interview level)
  - Hard (challenging edge cases, deep probing)
  - Expert (research-level, rare scenarios)
  Default: Medium
```

#### Technical Depth (Controls how deep you go)
```
Depth:
  - Surface (10-15 min per question, overview)
  - Intermediate (15-20 min per question, balanced)
  - Deep (20-30 min per question, exhaustive)
  Default: Intermediate
```

#### Question Count (Controls quantity per round)
```
Question Count: [1-8]
  - 1-2: Quick warm-up session
  - 3-4: Standard interview
  - 5-6: Full deep-dive
  - 7-8: Exhaustive practice
  Default: 4 (auto-calculated from duration)
```

#### Follow-Up Style (Controls conversation realism)
```
Follow-Ups:
  - None (just questions, no follow-ups)
  - Light (1 follow-up per question)
  - Moderate (2-3 follow-ups with probing) ← Most realistic
  - Heavy (continuous probing, dynamic conversation)
  Default: Moderate
```

#### Follow-Up Intensity (How aggressive is the interviewer?)
```
Follow-Up Intensity:
  - Supportive (hints if stuck, collaborative)
  - Neutral (asks probing questions, doesn't hint)
  - Challenging (pushes back, plays devil's advocate)
  Default: Neutral
```

#### Interviewer Style (Personality & approach)
```
Interviewer Style:
  - Traditional (professional, by-the-book questions)
  - Conversational (friendly, natural flow)
  - Adversarial (challenging, probing deeply)
  - Collaborative (partner-like, working together)
  Default: Conversational
```

#### Focus Area (Role-specific expertise)
```
Focus Area: [frontend-specific/full-stack/backend/leadership/system-thinking/mentorship]
```

#### Job Description (Context for relevance)
```
Job Description: [Key responsibilities, required skills, focus areas]
```

---

### Full Example Input

```
Company: Google
Role: Senior Frontend Engineer (L4)
Job Description: React, TypeScript, system design, 100M+ users, mentorship

Resume:
  12 years experience, React expert, micro-frontend architecture at Expedia,
  built risk management platform at Paytm (85% performance improvement),
  architected KYC onboarding at Moniepoint (99.9% uptime)

Rounds:
  1. Tech Screen
     - Duration: 45 min
     - Difficulty: Medium
     - Depth: Intermediate
     - Question Count: 3
     - Follow-Ups: Moderate

  2. System Design
     - Duration: 60 min
     - Difficulty: Hard
     - Depth: Deep
     - Question Count: 2
     - Follow-Ups: Heavy
     - Interviewer Style: Challenging

  3. Behavioral
     - Duration: 45 min
     - Difficulty: Medium
     - Depth: Intermediate
     - Question Count: 4
     - Follow-Ups: Light
     - Interviewer Style: Conversational
```

You can provide this in any format — structured, casual, conversational. The skill will interpret it.

---

## Output Format

The skill generates realistic, conversational interviews. Output varies based on your customization:

### Single Round (Default)

```
[MOCK INTERVIEW]
Company: [Company]
Role: [Role] ([Level])
Round: [Round Type] - [Duration]
Difficulty: [Level] | Depth: [Level]
Follow-Up Style: [Style] | Interviewer: [Personality]

---

INTERVIEW CONTEXT:
[Why this round matters for this role]
[What the interviewer is evaluating]
[Company/role-specific signals]

---

QUESTION 1: [Opening question, resume-aware]
   Interviewer motivation: [Why they're asking]
   Difficulty: [Easy/Medium/Hard]
   Time estimate: [15-30 min]
   
   [Candidate: You answer here]
   
   INTERVIEWER FOLLOW-UP 1: [Natural probing question]
   Why: [What they're testing]
   
   [Candidate: You answer]
   
   INTERVIEWER FOLLOW-UP 2: [Pushing deeper or testing edge case]
   
   [Candidate: You answer]
   
   INTERVIEWER SUMMARY: [What they note, positive signals, gaps]
   
   Expected answer framework:
   - [Key insight 1]
   - [Key insight 2]
   - [Key insight 3]
   
   Tips to stand out:
   - [Reference your experience from resume]
   - [Specific optimization or insight]
   - [Communication pattern that impresses]

QUESTION 2: ...
QUESTION 3: ...

---

INTERVIEW WRAP-UP:
- How you performed: [Overall assessment]
- Strongest signals: [What impressed the interviewer]
- Areas to improve: [What to practice]
- Next steps: [How to prepare for real interview]
```

### Multi-Round (Full Interview Day)

```
[FULL INTERVIEW DAY SIMULATION]
Company: Google
Role: Senior Frontend Engineer (L4)
Interview Rounds: 3 (4.5 hours total)

---

[ROUND 1: TECH SCREEN - 45 min]

INTERVIEWER INTRODUCTION:
"Hi! I'm [Name], an engineer here at Google. Today we're doing a tech screen.
I want to see how you approach problems and communicate your thinking. Sound good?"

QUESTION 1: [Question]
  FOLLOW-UP 1: [Probing]
  FOLLOW-UP 2: [Edge case]

QUESTION 2: [Question]
  FOLLOW-UP 1: [Optimization]

QUESTION 3: [Question]

INTERVIEWER CLOSING (Tech Screen):
"Great work. You showed solid problem-solving and communication. 
Let's move to system design."

---

[ROUND 2: SYSTEM DESIGN - 60 min]

INTERVIEWER TRANSITION:
"Now we're doing system design. I want to see how you think about
building large-scale systems. Any questions before we start?"

QUESTION 1: [Design problem]
  CLARIFICATION: "You ask about users, scale, latency budget"
  
  [Candidate proposes architecture]
  
  INTERVIEWER PROBE 1: [Tradeoff challenge]
  INTERVIEWER PROBE 2: [Scale challenge]
  INTERVIEWER PROBE 3: [Real-world constraint]

INTERVIEWER NOTES:
- Strong: [Signals]
- Gaps: [Areas to develop]

---

[ROUND 3: BEHAVIORAL - 45 min]

INTERVIEWER SETUP:
"Finally, let's talk about your background and how you work with teams."

QUESTION 1: [Behavioral]
  FOLLOW-UP: [Go deeper on impact]

QUESTION 2: [Leadership/influence]

QUESTION 3: [Learning/growth]

INTERVIEWER CLOSING:
"Thanks for your time. You showed [strengths]. We'll be in touch."

---

INTERVIEW DAY SUMMARY:
- Overall performance: [Assessment]
- Round strengths: [Tech Screen, System Design, Behavioral breakdown]
- Likely next steps: [Offer / More rounds / Not moving forward]
- Improvement areas: [Practice focus]
```

### Conversational Interview (With Heavy Follow-Ups)

When you choose `Follow-Ups: Heavy`, the interview feels like a real conversation:

```
INTERVIEWER: "Let's start with a tech problem. Design a React component
that fetches and displays a list of 1M products with infinite scroll.
How would you approach this?"

YOU: [Answer]

INTERVIEWER: "Interesting. Can you walk me through how you'd handle 
lazy loading images without blocking the main thread?"

YOU: [Answer]

INTERVIEWER: "What about accessibility? Screen readers with infinite scroll
can be tricky. How would you handle that?"

YOU: [Answer]

INTERVIEWER: "I like that you thought about a11y. One more thing — what if
the user's network is slow? How do you optimize for 3G?"

YOU: [Answer]

INTERVIEWER: "Solid thinking. You clearly understand performance at scale.
Let's move on to the next question..."
```

This creates a realistic, flowing conversation rather than isolated Q&A.

---

## Example Usage

### Input
```
Company: Google
Role: Senior Frontend Engineer (L4)
Job Description: React, TypeScript, system design, large-scale web apps, mentorship
Resume: 12 years frontend experience, React expert, built micro-frontend architecture at Expedia and Paytm
Interview Round: System Design
Duration: 60 minutes
Difficulty: Hard
Follow-Ups: Moderate
```

### Output (excerpt)
```
[MOCK INTERVIEW]
Company: Google
Role: Senior Frontend Engineer (L4)
Round: System Design - 60 min
Difficulty: Hard

---

INTERVIEW CONTEXT:
At L4, Google interviewers expect you to think like a tech lead.
They're evaluating: System thinking, trade-off analysis, scalability,
mentorship mindset, and ability to influence architecture decisions.

---

QUESTION 1: Design the frontend architecture for a new Google product 
that needs to support millions of concurrent users across mobile and web,
with a requirement to ship new features every 2 weeks.

Interviewer motivation: Tests if you think systemically about frontend
infrastructure, not just UI components. Shows if you can balance speed
with quality at scale.

FOLLOW-UP: Your CTO says "we need this feature in 1 week." How do you
adjust your architecture decisions?

Expected answer framework:
- Start with requirements: scale, performance targets, team size
- Propose a modular architecture (micro-frontends, design systems)
- Discuss trade-offs: time-to-market vs. technical debt
- Mention monitoring, rollout strategy, team enablement

Tips to stand out:
- Mention "developer experience" — L4 roles care about team velocity
- Reference real systems you've built (your Paytm micro-frontend work)
- Don't just describe a system, explain why it's the *right* system
```

---

## Pro Tips for Best Results

1. **Be Specific About Your Resume**: The more concrete details you provide, the more personalized the interview will be.

2. **Specify Difficulty Accurately**: Interviews vary wildly. Hard at Google ≠ Hard at a startup.

3. **Use Follow-Ups for Practice**: Moderate or Heavy follow-up modes simulate real interview conversation better.

4. **Review the Answer Framework**: These are guides, not "right answers" — use them to brainstorm your own approach.

5. **Practice Multiple Times**: Generate the same interview 2-3 times to get different questions, then compare your answers.

6. **Combine Round Types**: Do a tech screen → system design → behavioral sequence to simulate a full interview day.

---

## Limitations & Disclaimers

- Generated questions are **representative**, not guaranteed to match actual interviews.
- Answer frameworks are **starting points**, not definitive answers.
- Difficulty is subjective — calibrate based on your own experience.
- This is **practice only** — real interviews may emphasize different signals.

---

## Feedback & Improvement

This skill improves with feedback. After running a mock interview:
- **What felt realistic?** What didn't?
- **Were questions relevant** to the role and your background?
- **Did the difficulty feel right?**
- **Did follow-ups feel natural?**

Share feedback to help improve this skill for the community!

---

## Next Steps

1. Provide your company, job description, and resume
2. Choose the interview round & difficulty level
3. Get your mock interview
4. Practice answering (ideally out loud or on video)
5. Iterate: regenerate, adjust difficulty, try different rounds
6. Track your progress over time

Ready to practice? Let's generate your first mock interview!

