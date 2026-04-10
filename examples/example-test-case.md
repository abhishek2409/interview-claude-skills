# Example Test Case: Abhishek's Google Interview Prep

This example shows how the mock-interview-skill works with a real person preparing for a real company.

---

## INPUT

```
Company: Google
Role: Senior Frontend Engineer
Level: L4
Job Description: 
  "We're looking for a Senior Frontend Engineer (L4) to join our Shopping 
  Platform team. You'll work on high-traffic web applications serving 
  billions of users worldwide. Required: React, TypeScript, system design, 
  web performance, mentorship."

Resume: 
  "12 years of frontend engineering experience. Led frontend architecture 
  at Expedia (BotFly SEO validation platform handling 500K+ URLs). Built 
  micro-frontend systems at Paytm (Risk Ops redesign, 85% speed improvement). 
  Architected KYC onboarding at Moniepoint (99.9% uptime). Strong in React, 
  TypeScript, web performance, design systems, mentorship."

Interview Rounds to Prepare:
  - Tech Screen (45 min, Medium difficulty)
  - System Design (60 min, Hard difficulty)
  - Behavioral (45 min, Senior IC track)

Difficulty: Medium for tech screen, Hard for system design, Medium for behavioral
Follow-Ups: Moderate
Focus: Frontend with system design thinking
```

---

## EXPECTED OUTPUT 1: Tech Screen Interview

```
[MOCK INTERVIEW]
Company: Google
Role: Senior Frontend Engineer (L4)
Round: Tech Screen - 45 min
Difficulty: Medium

---

INTERVIEW SETUP:
Google's tech screen for L4 frontend engineers focuses on React fundamentals,
component design, and JavaScript problem-solving. At Google's scale, they want
to see if you can write clean, performant code quickly.

What's being evaluated:
- React component design & optimization
- JavaScript fundamentals
- Problem-solving & communication
- Code quality & scalability thinking

---

QUESTION 1: Implement a React component that renders a list of 10,000 items
with smooth scrolling performance. The list items have titles, descriptions,
and images.

Difficulty: Medium
Time estimate: 20 minutes
Why this matters for Google L4: Google's infrastructure serves billions of users.
This tests if you understand performance fundamentals at scale.

Background: At Expedia's BotFly, you've processed 500K URLs. At Google's 
Shopping Platform, you'll handle similar scale on the frontend. Your KYC 
onboarding at Moniepoint handled 100 signups/hour — showing you understand 
performance under load.

FOLLOW-UP 1: How would you handle dynamically adding/removing items from the list?

FOLLOW-UP 2: The backend now returns paginated results (50 items per page). 
How does your implementation change?

Expected approach:
- Virtual scrolling library (react-window, react-virtualized)
- Memoization & lazy loading for images
- Efficient data structure (index-based rendering)
- Pagination awareness

Answer signals (strong):
- Mentions virtual scrolling as primary strategy
- Discusses image lazy loading
- Considers bundle size (external lib vs. custom)
- References real-world tradeoffs

Common mistakes:
- Rendering all 10,000 items (performance disaster)
- Over-optimizing before understanding constraints
- Not mentioning accessibility (screen readers + virtual lists)

How to stand out:
- "In my BotFly work, we processed massive URL datasets. I'd apply similar 
  thinking here: batch updates, efficient indexing, progressive loading."
- Mention observability: "How would we measure this in production? Core Web Vitals."
- Discuss accessibility: "Virtual lists require ARIA labels for navigation."

---

QUESTION 2: Debug this React code. Why is the component re-rendering excessively?

[Code snippet showing a classic performance issue: 
object prop in dependency array, inline function, etc.]

Expected debugging approach:
- Use React DevTools Profiler
- Identify what's causing re-renders
- Propose fix (useMemo, useCallback, stable props)

---

INTERVIEW TIPS FOR GOOGLE:
- Google values clean, production-ready code
- They ask follow-ups to see how you think under pressure
- Mention scale: "How does this work with 1M items?"
- Discuss browser APIs: Can you use IntersectionObserver instead of a library?
- Think about SEO/accessibility — Google cares deeply about this
```

---

## EXPECTED OUTPUT 2: System Design Interview

```
[MOCK INTERVIEW]
Company: Google
Role: Senior Frontend Engineer (L4)
Round: System Design - 60 min
Difficulty: Hard

---

INTERVIEW SETUP:
At L4, Google expects you to think like a tech lead designing frontend 
systems, not just building features. This round evaluates:
- Architectural thinking across frontend & backend
- Trade-off analysis under constraints
- Scalability & performance at Google's scale
- Your ability to influence technical direction

---

PROBLEM 1: Design the frontend architecture for Google Shopping product 
pages. Millions of users visit these pages daily from mobile & web. New 
products are added every minute. You need to support:
- Product details, images, reviews
- Real-time inventory & pricing updates
- Personalization (recommendations, history)
- Mobile & desktop experiences
- Launch new features every 2 weeks

Difficulty: Hard
Time estimate: 45-50 minutes

Why this matters for Google L4:
Google's Shopping platform is critical business infrastructure. Your role 
isn't just building features — it's thinking about systems that enable 
teams to move fast while maintaining quality.

Expected clarification questions you should ask:
- "How many daily active users? Mobile vs. desktop split?"
- "What's the latency budget? Is this P99 or average?"
- "How do we handle real-time inventory updates?"
- "Are there A/B testing requirements?"
- "What's the team structure?"

Design areas to discuss:
- Component architecture (atomic to page level)
- Server-side rendering vs. client-side
- State management approach
- API contract between frontend & backend
- Real-time update strategy
- Performance optimization (images, code splitting)
- Monitoring & debugging at scale

Key decisions to probe:

PROBE 1 (Tradeoff): "You say server-side rendering. But that increases 
backend load. How do you balance TTM and server cost?"

Your answer signals (strong):
- Discuss edge caching, incremental static regeneration
- Mention "we'd use Next.js ISR for product pages"
- Show understanding of cost-performance tradeoff
- Suggest: "For high-traffic products, SSR. For niche products, static + ISR."

PROBE 2 (Real-time): "Prices change constantly. Inventory sells out. How 
do we show accurate, real-time data without overwhelming the backend?"

Your answer signals (strong):
- Mention: Real-time WebSocket, periodic polling, or hybrid
- Discuss cache invalidation strategy
- Show understanding of user experience: stale data is OK if it updates fast
- Reference: "At Paytm, we handled case status updates similarly with GraphQL subscriptions."

PROBE 3 (Scale): "Next holiday season, traffic increases 10x. How does 
your architecture handle this?"

Your answer signals (strong):
- Discuss: CDN, caching layers, database optimization
- Mention: Progressive enhancement, graceful degradation
- Show: "We'd load critical content first, defer secondary"
- Reference experience: "At Moniepoint, we handled 100 signups/hour at launch."

Expected architecture (one approach):
- Frontend: Next.js with component-based architecture
- State: React Context for page-level, Zustand/Redux for complex state
- API: GraphQL for flexible product queries
- Real-time: WebSocket subscriptions for price/inventory
- Caching: Redis for API responses, CDN for assets
- Monitoring: StatsD/DataDog for performance, feature flags for rollouts

Common mistakes:
- Over-engineering: "We'll use micro-frontends for every component"
- Ignoring operations: Not mentioning monitoring, error handling
- Assuming perfect network: Not discussing offline or slow connections
- Not mentioning the team: "How do 10 engineers maintain this?"

How to stand out:
- Reference your Paytm case management work: "I'd apply the same rule-driven 
  architecture here. React UI → GraphQL → Backend rules engine."
- Show pragmatism: "We don't need a micro-frontend framework day 1. We adopt 
  it when the team grows beyond 5-6 people."
- Mention operations: "We'd use feature flags for gradual rollouts, structured 
  logging for debugging, and error budgets for reliability."
- Discuss developer experience: "How do we empower other frontend engineers 
  to build features fast? Design system, shared components, clear API contracts."

---

SYSTEM DESIGN TIPS FOR GOOGLE:
- Google values scale thinking — always ask "What if this is 10x bigger?"
- They respect using proven tech, not reinventing everything
- Mention monitoring, alerting, and observability — it's often overlooked
- Show understanding of business: Time-to-market vs. technical debt
- Reference industry standards: "We'd follow Google's Web Vitals framework"
```

---

## EXPECTED OUTPUT 3: Behavioral Interview

```
[BEHAVIORAL INTERVIEW]
Company: Google
Role: Senior Frontend Engineer (L4)
Track: Senior Individual Contributor
Duration: 45 min
Difficulty: Medium

---

INTERVIEW SETUP:
Google's behavioral round for L4 engineers focuses on:
- Collaboration & communication
- Technical influence & ownership
- Learning from mistakes & growth
- Impact on team & product

---

QUESTION 1: Tell me about a time you led a technical decision without 
having direct authority. How did you build consensus?

Why this question: L4 engineers should influence architecture & tech direction, 
not just execute. This shows how you build credibility and drive decisions.

Expected STAR answer:
- Situation: "At Paytm, we had legacy case management built with jQuery and 
  vanilla JS. It was slow and hard to maintain."
- Task: "As a senior engineer, I wasn't the official tech lead, but I saw 
  an opportunity to modernize it."
- Action: "I built a prototype of the UI in React, showed performance 
  improvements (85% speed increase). Presented data to the team and got 
  buy-in from 3 senior engineers."
- Result: "We got approval to rewrite. Delivered in 2 months. Reduced case 
  backlog from 40K to 1K, improving team efficiency significantly."

Answer signals (strong):
- Specific metrics (85% speed increase, 40K → 1K cases)
- Shows persuasion & consensus-building
- Demonstrates impact on business/product
- Shows initiative & ownership

Common mistakes:
- Vague: "I suggested using React and they agreed"
- Blame: "Our tech lead was wrong, so I had to fix it"
- No outcome: "I proposed it but not sure what happened"

FOLLOW-UP: "How did you measure the 85% improvement? What were you optimizing for?"

How to stand out:
- Mention: Your Paytm redesign work directly (show familiarity with your resume)
- Discuss: How you worked with product & operations teams, not just engineers
- Reflection: "I learned that data wins arguments. I always back up suggestions 
  with evidence now."

---

QUESTION 2: Tell me about a time you made a significant mistake and what 
you learned.

Why this question: Shows self-awareness, accountability, and growth mindset.

Expected answer:
- Situation: [A real mistake — performance regression, shipped bug, missed deadline]
- Task: [Your role & responsibility]
- Action: [How you owned it, debugged it, fixed it]
- Learning: [What you changed in your process]

Answer signals (strong):
- Own the mistake ("I shipped this")
- Focus on root cause ("I didn't test edge case X")
- Show learning ("Now I always do Y")
- Business impact ("This affected 10K users")

Common mistakes:
- Blaming others ("My colleague reviewed it poorly")
- Minimizing ("It was a tiny bug")
- No learning ("I fixed it and moved on")

---

QUESTION 3: Describe your approach to mentoring junior engineers. Give 
an example.

Why this question: L4 engineers are expected to grow others and raise 
team capability.

Expected answer:
- Philosophy: "I believe in hands-on mentoring with progressively harder work"
- Example: [Specific mentee, problem, how you helped, outcome]
- Growth: "They shipped X, improved in Y, now they're leading Z"
- Reflection: "I learned that patience and asking questions beats just telling"

Answer signals (strong):
- Concrete example with names & outcomes
- Shows how you develop people
- Demonstrates impact on team

---

TIPS FOR GOOGLE:
- Google values collaboration and "building consensus"
- They ask about learning & growth frequently
- Mention how you've made your team better
- Show humility: Mistakes are OK if you learned
- Talk about impact: Did your work affect users/business?
```

---

## How to Use This Output

1. **Read each interview carefully** — Get familiar with the question styles
2. **Practice answering out loud** — Better simulation of real interview
3. **Record yourself** — Review for clarity, confidence, pacing
4. **Iterate** — Regenerate 2-3 times and compare answers
5. **Track improvements** — See how your answers evolve

## Success Metrics

After practicing with this skill:
- ✅ You can answer technical questions clearly with examples
- ✅ You can design systems at Google's scale
- ✅ You tell stories with impact (metrics, outcomes)
- ✅ You feel confident speaking about your experience
- ✅ You understand what Google values in L4 engineers

