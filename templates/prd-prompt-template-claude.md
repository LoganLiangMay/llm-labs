# PRD Prompt Template (Claude-Optimized)
_Last updated: 2025-10-30_

## Purpose
Reusable prompt template for generating Product Requirements Documents (PRDs) via Claude (Claude Code, Claude.ai, or API). Optimized for Claude's conversational style and context handling.

## When to Use
- Starting a new project with Claude Code as your implementation tool
- Using Claude.ai web interface for planning
- When you want conversational refinement of your PRD
- Projects where you'll use Claude throughout development

## Differences from Cursor Version
- More conversational tone (Claude prefers natural language)
- Explicit BMAD methodology mention (Claude Code supports this)
- Built-in iteration prompts (Claude excels at refinement)
- References to Claude Code's file operations

---

## The Claude-Optimized Prompt Template

```markdown
I'm planning to build [PROJECT_NAME] and I need your help creating a comprehensive Product Requirements Document (PRD) that will guide implementation.

I'll be using you (Claude) throughout this project for both planning and implementation, so the PRD should be detailed enough that you can later help me build it using the BMAD method (Break down, Make, Approve, Deploy).

Let's start with the PRD focused **exclusively on MVP scope** - what needs to ship in the first version to prove the concept works.

---

## Project Context

**What I'm Building:**
[PROJECT_NAME] - [1-2 sentence description]

**Why This Matters:**
[Brief explanation of the problem this solves or value it provides]

**Timeline:**
- MVP deadline: [e.g., 24 hours, 1 week]
- Final deadline: [if different from MVP]

**Key Constraints:**
[Any technical, time, or resource constraints]

---

## Full Project Specification

[PROJECT_SPEC_DOC]

(Paste your complete project specification, rubric, or requirements document here. Don't summarize - include everything so Claude has full context.)

---

## My Chosen Approach

I've already researched options and made these decisions:

**Platform/Frontend:**
- [e.g., React Native with Expo, Swift/SwiftUI, Next.js, etc.]
- Why: [brief reason]

**Backend/Infrastructure:**
- [e.g., Firebase (Firestore, Auth, Cloud Functions, FCM)]
- Why: [brief reason]

**Database/Persistence:**
- [e.g., Expo SQLite for local, Firestore for cloud]
- Why: [brief reason]

**AI Integration:**
- [e.g., OpenAI GPT-4, Anthropic Claude]
- Architecture: [e.g., Hybrid - dedicated AI chat + contextual inline features]
- Why: [brief reason]

**Target User Persona:**
- [e.g., Remote Team Professional]
- Their main pain points: [list 3-5 specific problems]

**Core Features (Required for MVP):**
1. [Feature 1]
2. [Feature 2]
3. [Feature 3]
4. [Feature 4]
5. [Feature 5]

**Advanced Feature (Post-MVP but planned):**
- [e.g., Multi-step agent that autonomously plans team events]

**Deployment Target:**
- [e.g., Expo Go, TestFlight, production web hosting]

---

## What I Need from You

Please generate a complete PRD with these sections:

### 1. Executive Summary
- 2-3 paragraph overview
- What we're building, why it matters, what MVP achieves

### 2. User Stories (MVP Focus)
- 8-12 user stories in format: "As a [user type], I want [action] so that [benefit]"
- Each marked **[MVP]** or **[Post-MVP]**
- Cover all key user types and workflows
- Prioritize by importance

### 3. MVP Feature Requirements
- Organized by category (e.g., Core Functionality, AI Features, Infrastructure)
- Each feature includes:
  - Description
  - Acceptance criteria (how we know it works)
  - Priority (P0 = must-have, P1 = important, P2 = nice-to-have)
- Functional requirements (what it does)
- Non-functional requirements (performance, reliability, UX)

### 4. Technical Architecture
- Component breakdown
- Data flow diagrams (in text/mermaid if helpful)
- Key technical decisions with rationale
- Third-party services and APIs needed

### 5. Tech Stack Justification
- For each technology choice, explain:
  - What it does
  - Why it's the right choice for this project
  - Alternatives considered (briefly)
  - Known limitations or tradeoffs

### 6. Out of Scope (Explicitly)
- What we're NOT building in MVP
- Features deferred to post-MVP
- "Nice to haves" that got cut
- Why each was excluded

### 7. Technical Risks & Mitigation
- 5-7 potential risks including:
  - Technical risks (e.g., API rate limits, performance bottlenecks)
  - UX risks (e.g., poor offline experience)
  - Timeline risks (e.g., complex features taking longer)
- For each risk:
  - Description
  - Impact if it occurs (High/Medium/Low)
  - Likelihood (High/Medium/Low)
  - Mitigation strategy
  - Fallback plan if mitigation fails

### 8. Success Metrics
- How we'll measure if MVP is successful
- Technical metrics (e.g., message delivery latency < 500ms)
- User metrics (e.g., user completes first message flow)
- Business metrics if applicable

### 9. Development Phases (BMAD-Ready)
- Suggested order of implementation
- Dependencies between features
- What can be built in parallel vs. sequentially
- Milestone checkpoints

---

## After You Generate the PRD

Once you've created the PRD:

1. **Pause and let me review it**
2. I'll give you feedback on:
   - Anything missing or unclear
   - Scope adjustments needed
   - Technical decisions I want to reconsider
3. We'll iterate on the PRD together until it's solid
4. Then we'll save it and use it throughout implementation

Remember: A great PRD makes implementation 10x easier. Let's take the time to get this right.

---

## Additional Context (Optional)

**My Experience Level:**
[e.g., Senior engineer, comfortable with React but new to React Native]

**What I'm Most Worried About:**
[e.g., Real-time sync reliability, AI feature accuracy, tight deadline]

**What I'm Most Excited About:**
[e.g., The multi-step agent capability, cross-platform from one codebase]

---

Please generate the PRD now. Be thorough, specific, and honest about risks. I want a document that will guide us successfully through implementation.
```

---

## How to Use This Template (Claude-Specific)

### Step 1: Prepare Your Information
Before opening Claude, gather:
- Full project specification document
- Your tech stack research and decisions
- User persona details
- Feature priorities

### Step 2: Fill in the Template
Replace all `[...]` placeholders:

| Section | What to Include | Example |
|---------|-----------------|---------|
| `[PROJECT_NAME]` | Your project name | ChatIQ, VideoEditor AI, TaskFlow |
| `[PROJECT_SPEC_DOC]` | Complete specification | Paste entire requirements doc |
| Platform/Frontend | Your chosen framework | React Native + Expo, Swift/SwiftUI |
| Backend | Backend services | Firebase, Supabase, custom Node.js |
| Target User Persona | Who you're building for | Remote Team Professional, Busy Parent |
| Core Features | 5-7 must-have features | List specific functionality |
| Experience Level | Your technical background | Helps Claude calibrate explanations |

### Step 3: Submit to Claude

**Option A: Claude Code (Terminal)**
- Paste the filled prompt into Claude Code terminal
- Claude can later save the PRD directly to your project files
- Claude has access to file operations for implementation

**Option B: Claude.ai (Web Interface)**
- Paste into a new conversation
- Claude will generate the PRD in markdown
- Copy the output and save to your project

**Option C: Claude API**
- Use the prompt as a system message or user prompt
- Parse the markdown response

### Step 4: Iterate & Refine

Claude excels at iteration. After the initial PRD:

**Common Follow-Up Prompts:**
```markdown
"The scope seems too ambitious for [timeline]. Can you trim it to the absolute minimum MVP?"

"I'm concerned about [specific risk]. Can you elaborate on mitigation strategies?"

"Can you add more detail to the [section name] section?"

"I want to change the tech stack from [X] to [Y]. Update the PRD and highlight what changes."

"Break down the 'Development Phases' section into a day-by-day implementation plan."
```

### Step 5: Save & Use

Once finalized:

**If using Claude Code:**
```markdown
"Save this PRD to `/docs/PRD.md` in my project"
```

**If using Claude.ai:**
- Copy the final PRD
- Save to your project as `PRD.md`
- Reference it throughout development

**Then:**
1. Link to the PRD in your vault: `/ai-drafts/[project-name]-prd.md`
2. Use it to guide BMAD implementation with Claude
3. Update as you learn during development

---

## Tips for Best Results with Claude

### 1. Provide Full Context
Claude handles long context well. Paste your **entire** project spec, don't summarize.

### 2. Be Conversational
Claude responds well to natural language:
- ✅ "I'm worried about X because..."
- ✅ "What do you think about..."
- ❌ "Generate PRD. Use format X."

### 3. Iterate Out Loud
Share your thinking:
```markdown
"I initially wanted to use X, but I'm now leaning toward Y because [reason].
What are the implications for the PRD?"
```

### 4. Ask for Claude's Opinion
```markdown
"Based on my timeline and constraints, do you think this scope is realistic?"
"What am I missing in my risk analysis?"
"Are there any technical landmines I should know about with this stack?"
```

### 5. Use Claude Throughout Implementation
After the PRD is done:
```markdown
"Using the PRD we created, let's implement [Feature 1] using BMAD.
Break it down into tasks first."
```

---

## Why Claude-Optimized is Different

| Aspect | Cursor Prompt | Claude Prompt |
|--------|---------------|---------------|
| **Tone** | Directive, structured | Conversational, collaborative |
| **Context** | Assumes Cursor's code context | Assumes fresh conversation |
| **Detail** | Concise, action-focused | Comprehensive, explanatory |
| **Iteration** | Less emphasis on back-and-forth | Explicitly encourages refinement |
| **BMAD** | Not mentioned (Cursor agnostic) | Explicitly mentioned (Claude Code feature) |
| **Length** | Shorter, efficient | Longer, thorough |
| **Follow-up** | Assumes you'll edit code directly | Assumes conversational iteration |

---

## Example Usage Flow

### 1. Initial Prompt
Paste filled template → Claude generates comprehensive PRD

### 2. Review & Question
"The AI features seem too complex for MVP. Can you simplify to just [X] and [Y]?"

### 3. Claude Revises
Claude updates the PRD, explains tradeoffs

### 4. Finalize
"This looks great. Please save it as `PRD.md`" (Claude Code) or copy/paste manually

### 5. Implementation
"Let's build the authentication system from the PRD. Break it down using BMAD."

### 6. Reference During Development
"According to our PRD, we said offline sync is P0. Let's implement that next."

---

## Related
- [[templates/prd-prompt-template]] - Cursor-optimized version
- [[workflows/project-initialization]] - Full workflow using this template
- [[ai-drafts/chatiq-prd-example]] - Example output (adaptable for Claude)
- [[tools/claude-code]] - Tool reference for Claude Code

---

## Advanced: Claude Code Integration

If using Claude Code terminal, you can chain this with implementation:

```markdown
1. [Paste PRD prompt above]
2. [Claude generates PRD]
3. "Save this PRD to `/docs/PRD.md`"
4. "Now, using this PRD, create a project structure with folders for all components mentioned"
5. "Let's start with [Feature 1]. Break it down into tasks using BMAD."
```

Claude Code can:
- Generate the PRD
- Save it to your project files
- Read it back during implementation
- Update it as you build

---

**Tags**: #template #prd #product-planning #claude #claude-code #reusable
**Type**: Prompt Template
**Optimized For**: Claude (all interfaces)
**Use Case**: Project initialization and planning with Claude
