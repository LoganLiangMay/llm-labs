# PRD Prompt Template
_Last updated: 2025-10-30_

## Purpose
Reusable prompt template for generating Product Requirements Documents (PRDs) via AI coding agents (Cursor, Claude Code, etc.). Optimized for BMAD methodology implementation.

## When to Use
- Starting a new project with clear requirements
- Converting project specifications into actionable PRDs
- Before beginning implementation in AI coding agents
- When you need a structured planning document for stakeholder review

---

## The Prompt Template

```markdown
You are an expert full-stack product engineer and technical product manager. Your task is to help me build [PROJECT_NAME] by first generating a **complete, professional Product Requirements Document (PRD)** focused on **MVP only**.

Use the provided project specification below to create the PRD. Structure it clearly with the following sections:

---

### 1. User Stories
- Write 8–12 concise, prioritized user stories in the format:
  `As a [user type], I want [action/feature] so that [benefit].`
- Cover all core user types (e.g., sender, receiver, group member, AI user).
- Mark each as **[MVP]** or **[Post-MVP]**.

### 2. Key MVP Features
- Bullet list of **only what must ship in the MVP** (24-hour deadline).
- Include functional and non-functional requirements (e.g., real-time sync, offline persistence, optimistic UI).
- Prioritize reliability over polish.

### 3. Tech Stack (Chosen)
- List the exact stack we **are using** (no alternatives in this section).
- One-line justification per component.
- Include:
  - Frontend: [e.g., React Native + Expo]
  - Navigation: [e.g., Expo Router]
  - Local DB: [e.g., Expo SQLite]
  - Backend: [e.g., Firebase Firestore, Auth, Cloud Functions, FCM]
  - AI: [e.g., OpenAI GPT-4 via Cloud Functions + RAG]
  - Deployment: [e.g., Expo Go]

### 4. Non-MVP Scope (Out of Scope)
- Explicitly list what we are **not building** in MVP.
- Be ruthless: no nice-to-haves.

### 5. Risks, Pitfalls & Recommendations
- Highlight 3–5 technical or UX risks (e.g., "Firebase listener memory leaks on rapid messages").
- For each:
  - Risk description
  - Impact (High/Med/Low)
  - Mitigation strategy or idea

---

After the PRD, **pause and wait for my approval**.
Once approved, we will edit the PRD together if needed, then proceed to implementation.

---

**Project Specification (Paste or Summarize Here):**
[PROJECT_SPEC_DOC]

**Chosen Options (Fill These In):**
- **Platform**: [e.g., React Native with Expo]
- **Backend**: [e.g., Firebase (Firestore, Auth, FCM, Cloud Functions)]
- **AI Integration**: [e.g., Hybrid: Dedicated AI chat + contextual inline features]
- **User Persona**: [e.g., Remote Team Professional]
- **AI Features (Required 5 + 1 Advanced)**:
  1. [e.g., Thread summarization]
  2. [e.g., Action item extraction]
  3. [e.g., Smart search over chat history]
  4. [e.g., Priority message detection]
  5. [e.g., Decision tracking]
  **Advanced**: [e.g., Multi-Step Agent: Plans team offsites autonomously]
- **Deployment Target**: [e.g., Expo Go (local + shared QR), Firebase backend live]

---

Output the PRD in clean markdown with clear headings, tables where helpful, and concise language.
Do **not** write code yet.
Do **not** mention BMAD, agents, or implementation steps.
Focus only on clarity, completeness, and decision-making support.
```

---

## How to Use This Template

### Step 1: Copy the Prompt
Copy everything between the triple backticks above.

### Step 2: Fill in Placeholders
Replace all `[...]` placeholders with your project specifics:

| Placeholder | What to Fill In | Example |
|------------|-----------------|---------|
| `[PROJECT_NAME]` | Your project name | ChatIQ, VideoEditor Pro, etc. |
| `[PROJECT_SPEC_DOC]` | Full project requirements/rubric | Paste entire spec document |
| **Platform** | Your chosen frontend framework | React Native with Expo, Swift/SwiftUI, Kotlin/Compose |
| **Backend** | Backend services | Firebase, Supabase, AWS, custom Node.js |
| **AI Integration** | How AI is integrated | Dedicated chat, contextual features, or hybrid |
| **User Persona** | Target user type | Remote Team Professional, Busy Parent, etc. |
| **AI Features** | Specific AI capabilities | List 5 required + 1 advanced |
| **Deployment Target** | Where it will be deployed | Expo Go, TestFlight, APK, web |

### Step 3: Submit to AI Agent
Paste the completed prompt into:
- **Cursor** (Chat mode)
- **Claude Code** (terminal or web)
- **GitHub Copilot Chat**
- Any other AI coding assistant

### Step 4: Review & Iterate
- Review the generated PRD
- Ask follow-up questions
- Refine tech stack choices
- Adjust scope as needed

### Step 5: Approve & Implement
Once satisfied:
1. Save the PRD in `/ai-drafts/[project-name]-prd.md`
2. Begin implementation using BMAD methodology
3. Reference PRD throughout development

---

## Tips for Best Results

### Be Specific with Project Specs
- Paste the **full** project specification document
- Include rubrics, requirements, constraints
- Don't assume the AI knows context

### Choose Your Stack First
- Research options before filling in the template
- Have a reason for each choice
- Consider team expertise and timeline

### Focus on MVP
- Be ruthless about what's in vs. out of scope
- MVP should be shippable in 24-48 hours
- Save nice-to-haves for post-MVP

### Use the Risk Section
- The AI will flag potential issues
- Pay attention to these warnings
- Adjust stack/scope based on risks

---

## Related
- [[workflows/project-initialization]] - Full workflow using this template
- [[ai-drafts/chatiq-prd-example]] - Example of template in use
- [[tools/cursor]] - Primary tool for using this prompt

---

**Tags**: #template #prd #product-planning #ai-agents #reusable
**Type**: Prompt Template
**Use Case**: Project initialization and planning
