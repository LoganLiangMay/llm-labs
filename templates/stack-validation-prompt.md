# Stack Validation Prompt Template
_Last updated: 2025-10-30_

## Purpose
Reusable prompt for validating tech stack decisions across multiple AI models before committing to a full PRD. Use this to catch potential issues early and gain confidence in your technology choices.

## When to Use
- After you've researched 2-3 potential tech stacks
- Before generating a full PRD
- When you're unsure about performance/scaling implications
- When you want multiple perspectives on your approach
- Before investing days of development time

## Which AI Tools to Use

### Recommended: Consult 2-3 of These (All Free Tiers)

| AI Tool | Best For | Free Tier | Access |
|---------|----------|-----------|--------|
| **ChatGPT** | General tech advice, common patterns | Yes (GPT-3.5) | chat.openai.com |
| **Claude.ai** | Architectural discussion, detailed analysis | Yes (limited) | claude.ai |
| **Grok** | Alternative perspectives, contrarian views | Yes (with X Premium) | x.com |
| **Perplexity** | Research-backed validation, citations | Yes | perplexity.ai |
| **Gemini** | Google ecosystem, Android/Firebase advice | Yes | gemini.google.com |

### Strategy:
- **Always use**: ChatGPT (fast, general) + Claude (thorough, architectural)
- **Add one**: Grok (alternatives), Perplexity (research), or Gemini (if using Google stack)

---

## The Prompt Template

```markdown
I'm in the planning stage of a project and need your help evaluating my tech stack decisions before I commit to development.

---

## Project Overview

**Project Name**: [PROJECT_NAME]

**Brief Description**: [1-2 sentence description of what you're building]

**Timeline**:
- MVP Deadline: [e.g., 24 hours, 1 week, 1 month]
- Final Deadline: [if different]

**Key Features (MVP)**:
1. [Feature 1]
2. [Feature 2]
3. [Feature 3]
4. [Feature 4]
5. [Feature 5]

**Target User**: [User persona and their main pain points]

**Key Technical Requirements**:
- [e.g., Real-time data sync]
- [e.g., Offline-first functionality]
- [e.g., Cross-platform (iOS + Android)]
- [e.g., AI integration with LLMs]
- [e.g., Handle 100+ concurrent users]

---

## Tech Stack Options I'm Considering

### Option 1: [Stack Name]
**Frontend**: [e.g., React Native + Expo]
**Backend**: [e.g., Firebase (Firestore, Auth, Cloud Functions)]
**Database**: [e.g., Firestore for cloud, SQLite for local]
**AI/ML**: [e.g., OpenAI GPT-4 via Cloud Functions]
**Deployment**: [e.g., Expo Go]

**Why I'm considering this**:
- [Reason 1]
- [Reason 2]

**My concerns**:
- [Concern 1]
- [Concern 2]

---

### Option 2: [Alternative Stack Name]
**Frontend**: [e.g., Swift/SwiftUI (iOS native)]
**Backend**: [e.g., Supabase (PostgreSQL, Realtime, Auth)]
**Database**: [e.g., PostgreSQL]
**AI/ML**: [e.g., Anthropic Claude via edge functions]
**Deployment**: [e.g., TestFlight]

**Why I'm considering this**:
- [Reason 1]
- [Reason 2]

**My concerns**:
- [Concern 1]
- [Concern 2]

---

### Option 3 (Optional): [Another Alternative]
[Same format as above, if applicable]

---

## Specific Questions I Need Help With

Please address these questions in your response:

### 1. Tech Stack Comparison
- Which stack is better suited for my MVP timeline and requirements?
- What are the deal-breakers or show-stoppers with each option?

### 2. Performance & Scalability
- How will each stack handle [specific requirement, e.g., "real-time messaging with 50+ users"]?
- What performance bottlenecks should I anticipate?
- Are there scaling issues that will hit me early?

### 3. Development Velocity
- Which stack will let me ship MVP fastest given my timeline?
- What's the learning curve if I'm not familiar with these technologies?
- Where will I get stuck or spend the most time?

### 4. Cost Implications
- What are the ongoing costs with each stack (APIs, hosting, third-party services)?
- Are there free tier limits I'll hit quickly?
- Any hidden costs I'm not seeing?

### 5. Risk Assessment
- What could go wrong with each approach?
- What am I overlooking or underestimating?
- Are there better alternatives I haven't considered?

### 6. MVP Scope Reality Check
- Is my MVP scope realistic for the timeline with each stack?
- What features should I cut to make the deadline?
- What's the absolute minimum viable version?

---

## My Context

**My Experience Level**:
[e.g., "Senior engineer with 5 years React, but new to mobile development"]

**What I'm Most Worried About**:
[e.g., "Real-time sync reliability under poor network conditions"]

**What I'm Most Excited About**:
[e.g., "Building cross-platform from a single codebase"]

**Constraints**:
[e.g., "Must support offline mode", "Budget: $50/month", "Solo developer"]

---

## What I Need from You

Please provide:

1. **Recommendation**: Which stack should I choose and why?
2. **Key Risks**: Top 3 risks with your recommended stack
3. **Mitigation Strategies**: How to address those risks
4. **MVP Scope Advice**: What to cut or keep for my timeline
5. **Alternatives**: Any better options I haven't considered?
6. **Next Steps**: What should I research or prototype first?

Be honest about tradeoffs and realistic about timelines. I'd rather hear hard truths now than discover problems mid-development.
```

---

## How to Use This Template

### Step 1: Fill in All Placeholders
Replace `[...]` with your specific information:
- Project name and description
- Timeline and deadlines
- All 5 MVP features
- Each tech stack option with components
- Your concerns and reasons
- Your experience level

### Step 2: Submit to Multiple AIs

**Copy the filled prompt and paste into:**

#### ChatGPT (chat.openai.com)
- Use GPT-3.5 (free) or GPT-4 (paid)
- Good for: Quick general advice, common patterns
- Save the response

#### Claude.ai (claude.ai)
- Free tier available (limited messages)
- Good for: Deep architectural discussion, tradeoff analysis
- Save the response

#### One Additional Tool (Choose One):

**Grok (x.com)** - if you have X Premium
- Good for: Alternative perspectives, contrarian takes
- May suggest options you hadn't considered

**Perplexity (perplexity.ai)** - free
- Good for: Research-backed recommendations with citations
- Validates claims with sources

**Gemini (gemini.google.com)** - free
- Good for: Google ecosystem advice (Firebase, GCP, Android)
- Best if you're considering Google stack

### Step 3: Compare Responses

Create a comparison document in `/ai-drafts/[project-name]-stack-validation.md`:

```markdown
# [Project Name] - Stack Validation Results

## Responses Summary

### ChatGPT Recommendation
- **Stack**: [which one]
- **Key reason**: [main argument]
- **Top risks**: [list]

### Claude Recommendation
- **Stack**: [which one]
- **Key reason**: [main argument]
- **Top risks**: [list]

### [Third AI] Recommendation
- **Stack**: [which one]
- **Key reason**: [main argument]
- **Top risks**: [list]

## Common Themes Across All AIs
- [Theme 1]
- [Theme 2]
- [Theme 3]

## Disagreements / Different Perspectives
- [Point 1]
- [Point 2]

## Risks All AIs Flagged
1. [Risk 1]
2. [Risk 2]
3. [Risk 3]

## MVP Scope Adjustments Suggested
- [Adjustment 1]
- [Adjustment 2]

## Final Decision
Based on multiple AI consultations, I'm choosing: **[Stack Name]**

**Reasons**:
1. [Reason 1]
2. [Reason 2]
3. [Reason 3]

**Risks I'm Accepting**:
1. [Risk 1] - Mitigation: [strategy]
2. [Risk 2] - Mitigation: [strategy]

**Next Step**: Generate PRD with [[templates/prd-prompt-template]] or [[templates/prd-prompt-template-claude]]
```

### Step 4: Make Your Decision

Look for:
- ✅ **Consensus**: If 2-3 AIs recommend the same stack, that's strong validation
- ⚠️ **Split opinions**: Dig deeper into why they disagree
- 🚨 **Common risks**: If all AIs flag the same issue, take it seriously
- 💡 **New options**: Did any AI suggest something you hadn't considered?

### Step 5: Document & Proceed

1. Save your validation notes in `/ai-drafts/`
2. Update your project context with the chosen stack
3. Proceed to Step 4: Generate PRD with confidence

---

## Tips for Best Results

### Be Specific
❌ "I need real-time features"
✅ "I need 50+ users to see message updates within 500ms, even on 3G networks"

### Provide Context
- Your experience level matters (affects "development velocity" advice)
- Budget constraints (free tiers vs. paid services)
- Solo vs. team project (different considerations)

### Ask Follow-Up Questions

After getting initial responses, ask:
```markdown
"You recommended [Stack A]. But I'm concerned about [specific issue].
How would you address that? Does that change your recommendation?"
```

### Challenge Recommendations

```markdown
"Most tutorials I've seen use [Stack B] for this use case.
Why are you suggesting [Stack A] instead? What am I missing?"
```

### Compare to Real-World Examples

```markdown
"WhatsApp was originally built with [Stack]. How does your recommendation
compare to that approach for a messaging app?"
```

---

## Common Validation Scenarios

### Scenario 1: Tight Timeline (24-48 hour MVP)
**Focus your questions on**:
- Development velocity
- Pre-built solutions vs. custom
- Learning curve if stack is new

**Key question**: "Can I realistically ship MVP in [timeline] with [stack]?"

### Scenario 2: Performance-Critical App
**Focus your questions on**:
- Benchmarks and performance data
- Scaling considerations
- Real-time data handling

**Key question**: "How will [stack] handle [specific performance requirement]?"

### Scenario 3: Budget-Constrained
**Focus your questions on**:
- Free tier limits
- API costs at scale
- Hidden expenses

**Key question**: "What will this cost at [X users/requests] per month?"

### Scenario 4: New Technology for You
**Focus your questions on**:
- Learning resources
- Common pitfalls
- Development time with learning curve

**Key question**: "If I'm new to [technology], how much overhead does that add?"

---

## Example: ChatIQ Messaging App

See [[ai-drafts/chatiq-stack-validation-example]] for a complete example of this template filled out for a WhatsApp-clone project.

---

## Related
- [[workflows/project-initialization]] - Full workflow using this template (Step 3)
- [[templates/prd-prompt-template]] - Next step: Cursor-optimized PRD
- [[templates/prd-prompt-template-claude]] - Next step: Claude-optimized PRD
- [[ai-drafts/chatiq-stack-validation-example]] - Example validation

---

**Tags**: #template #stack-validation #tech-stack #ai-consultation #planning
**Type**: Prompt Template
**Use Case**: Pre-PRD tech stack validation across multiple AI models
**Time Investment**: 15-20 minutes across 2-3 AIs
**ROI**: Catches 80% of stack mistakes before coding starts
