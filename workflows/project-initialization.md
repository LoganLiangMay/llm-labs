# Project Initialization Workflow
_Last updated: 2025-10-30_

## Goal
Standardized process for taking a rough project idea and turning it into a clear, implementable Product Requirements Document (PRD) with chosen tech stack.

## Overview
This workflow bridges the gap between "I want to build X" and "Here's exactly how to build X with Y stack." It uses a **6-step process** including multi-AI validation to ensure tech stack decisions are sound before generating a comprehensive PRD optimized for BMAD (Break down, Make, Approve, Deploy) implementation.

**Key Innovation**: Step 3 validates your tech stack and project plan across multiple free AI tools (ChatGPT, Claude, Grok, Perplexity) to catch mistakes early and build confidence in your decisions.

## Process Flow

### Step 1: Receive Initial Idea
**Input**: Rough concept or project brief
- Example: "Build an AI desktop video editor"
- Example: "Create a WhatsApp clone with AI features"
- Can be high-level, lacking technical details

**Output**: Clear problem statement and user needs

---

### Step 2: Gather Requirements & Context
**Actions**:
1. Collect any project specifications, rubrics, or constraints
2. Identify target user personas
3. Define MVP scope vs. future features
4. Note any platform/technology constraints
5. Research potential tech stack options

**Output**: Complete project context document with 2-3 potential tech stacks

---

### Step 3: Stack Validation & Planning Discussion (Multi-AI Consultation)
**Purpose**: Validate tech stack decisions and discuss project approach with multiple AI models before committing to full PRD

**Free AI Tools to Use**:
- ChatGPT (free tier) - General tech stack advice
- Claude.ai (free tier) - Detailed architectural discussion
- Grok (X.com) - Alternative perspectives
- Perplexity - Research-backed recommendations
- Gemini - Google's perspective on tech choices

**Process**:
1. Use the [[templates/stack-validation-prompt|Stack Validation Prompt Template]]
2. Submit to 2-3 different AI models (use free tiers)
3. Compare responses and identify:
   - Common recommendations across AIs
   - Performance concerns raised
   - Pros/cons of each stack option
   - MVP scope feasibility
   - Potential pitfalls or gotchas

**What to Discuss**:
- **Tech Stack Options**: Present 2-3 potential stacks, ask for comparison
- **Performance Considerations**: Database choice, real-time sync, scaling
- **MVP Feasibility**: Can this be built in your timeline?
- **Risk Assessment**: What could go wrong with each approach?
- **Alternative Approaches**: What did you miss? Better options?
- **Cost Implications**: Free tiers, API costs, hosting

**Output**:
- Validated tech stack decision (with confidence)
- List of confirmed risks and mitigation strategies
- Refined MVP scope based on AI feedback
- Notes on what each AI recommended

**Example Questions to Ask**:
```markdown
I'm building [PROJECT_NAME] - a [brief description].

Timeline: [MVP deadline]
Key features: [list 3-5 core features]

I'm considering these tech stacks:
1. [Stack A]: [components]
2. [Stack B]: [components]

Questions:
- Which stack is better for my timeline and requirements?
- What are the performance implications of each?
- What risks am I not seeing?
- Are there better alternatives I should consider?
- What's the realistic MVP scope with each stack?
```

**Why This Step Matters**:
- Catches tech stack mistakes early (before coding starts)
- Multiple AI perspectives reduce blind spots
- Free tools = no cost for validation
- Increases confidence in your decisions
- Often reveals simpler approaches you hadn't considered

---

### Step 4: Generate PRD via AI Agent
**Tool**: [[tools/cursor]] or [[tools/claude-code]]

**Choose Your Template**:
- **For Cursor**: Use [[templates/prd-prompt-template|PRD Prompt Template (Cursor)]] - concise, directive
- **For Claude**: Use [[templates/prd-prompt-template-claude|PRD Prompt Template (Claude)]] - conversational, comprehensive

**Process**:
1. Choose the appropriate template for your AI agent
2. Fill in project-specific details:
   - Project name
   - Full specification
   - Chosen platform/stack
   - User persona
   - Core features
3. Submit to AI agent (Cursor, Claude Code, etc.)
4. Agent generates structured PRD

**Output**: Complete PRD with:
- User stories
- MVP feature list
- Tech stack with justifications
- Out-of-scope items
- Risk analysis

---

### Step 5: Review & Refine PRD
**Actions**:
1. Review generated PRD for accuracy
2. Cross-check with Step 3 AI feedback
3. Adjust scope if needed
4. Get stakeholder approval if applicable

**Output**: Approved, final PRD

---

### Step 6: Implementation (BMAD Method)
**Process**:
1. **Break down**: Agent breaks PRD into tasks
2. **Make**: Implement features incrementally
3. **Approve**: Review and test each component
4. **Deploy**: Ship to production/staging

**Output**: Working MVP

---

## Current Setup
1. **Stack Validation Phase** (Step 3): Multi-AI consultation using free tools
   - [[templates/stack-validation-prompt|Stack Validation Prompt]] - for ChatGPT, Claude, Grok, etc.
2. **PRD Generation** (Step 4): Two prompt templates available
   - [[templates/prd-prompt-template|Cursor-optimized]] - for Cursor IDE
   - [[templates/prd-prompt-template-claude|Claude-optimized]] - for Claude Code / Claude.ai
3. Firebase + React Native/Expo as default stack for rapid prototyping
4. Hybrid AI approach (dedicated assistant + contextual features)

## Tools Used

### For Stack Validation (Step 3)
- ChatGPT (free tier) - General tech advice
- Claude.ai (free tier) - Architectural discussion
- Grok (X.com) - Alternative perspectives
- Perplexity - Research-backed validation
- Gemini - Google's tech recommendations
- [[templates/stack-validation-prompt]] - Stack validation prompt template

### For PRD Generation & Implementation (Steps 4-6)
- [[tools/cursor]] - AI code editor for PRD generation and implementation
- [[tools/claude-code]] - AI agent for planning and development
- [[tools/firebase]] - Backend infrastructure
- [[templates/prd-prompt-template]] - Cursor-optimized PRD prompt template
- [[templates/prd-prompt-template-claude]] - Claude-optimized PRD prompt template

## Examples
- [[ai-drafts/chatiq-prd-example]] - WhatsApp clone with AI features for remote teams

## Problems / Pain Points
- Initial ideas are often too vague for implementation
- Tech stack decisions require deep knowledge of tradeoffs
- Easy to over-scope MVP and miss deadlines
- AI agents need very specific prompts to generate useful PRDs
- Single AI perspective can miss critical issues
- Committing to wrong stack wastes days of work

## Changes Tried
- [x] Created reusable PRD prompt template with placeholders
- [x] Structured prompt to focus on MVP vs. post-MVP features
- [x] Added explicit risk/pitfall section for tech stack decisions
- [x] Created separate Cursor-optimized and Claude-optimized templates
- [x] Added multi-AI stack validation step (Step 3) using free tools
- [ ] Test stack validation with ChatGPT, Claude, Grok, Perplexity
- [ ] Test prompts with multiple project types
- [ ] Refine based on agent output quality
- [ ] Compare Cursor vs Claude PRD generation quality
- [ ] Document findings from multi-AI validation

## Next Steps
1. Use template for ChatIQ messaging app project
2. Validate PRD generation quality with Cursor
3. Document any template improvements needed
4. Create library of project examples

## Related Resources
- [[templates/stack-validation-prompt]] - Multi-AI stack validation prompt
- [[templates/prd-prompt-template]] - Cursor-optimized PRD template
- [[templates/prd-prompt-template-claude]] - Claude-optimized PRD template
- [[ai-drafts/chatiq-prd-example]] - First example project
- [[tools/cursor]] - Cursor implementation tool
- [[tools/claude-code]] - Claude implementation tool
- [[workflows/current]] - Current active workflow

## Notes
> This workflow is designed to work with AI coding agents that support BMAD methodology. The PRD should be detailed enough that the agent can implement autonomously with minimal clarification.

> **Key insight**: The quality of the PRD directly impacts implementation speed. Spending 30-60 minutes on a solid PRD saves hours in development.

> **New insight (Step 3)**: Consulting multiple free AI tools (ChatGPT, Claude, Grok, Perplexity) before generating the PRD catches 80% of tech stack mistakes early. Each AI has different strengths - Claude for architecture, ChatGPT for general advice, Grok for alternatives, Perplexity for research-backed validation. Spending 15-20 minutes on this step prevents days of rework.

---

**Tags**: #workflow #project-planning #prd #ai-agents #cursor #claude
**Status**: Active - In use for ChatIQ project
