# ChatIQ PRD Example
_Date: 2025-10-30_

## Project Context
**Source**: Gauntlet AI - MessageAI Project
**Goal**: Build a production-quality messaging app (WhatsApp clone) with AI features in one week
**Chosen Persona**: Remote Team Professional
**Timeline**: MVP in 24 hours, final in 7 days

## Project Overview
WhatsApp-style messaging app with:
- Real-time messaging, group chat, offline support
- AI features: thread summarization, action item extraction, smart search, priority detection, decision tracking
- Advanced: Multi-step agent for autonomous team offsite planning

## Chosen Tech Stack
- **Platform**: React Native with Expo
- **Backend**: Firebase (Firestore, Auth, FCM, Cloud Functions)
- **AI Integration**: Hybrid (dedicated AI chat + contextual inline features)
- **Deployment**: Expo Go

---

## Filled Prompt (Ready to Use in Cursor)

```markdown
You are an expert full-stack product engineer and technical product manager. Your task is to help me build ChatIQ by first generating a **complete, professional Product Requirements Document (PRD)** focused on **MVP only**.

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
  - Frontend: React Native + Expo
  - Navigation: Expo Router
  - Local DB: Expo SQLite
  - Backend: Firebase Firestore, Auth, Cloud Functions, FCM
  - AI: OpenAI GPT-4 via Cloud Functions + RAG
  - Deployment: Expo Go

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

**Project Specification:**

MessageAI - Building Cross-Platform Messaging Apps with AI Features

Background: WhatsApp transformed how billions communicate by making messaging fast, reliable, and secure. This project challenges you to build both production-quality messaging infrastructure and AI features that enhance the messaging experience using LLMs, agents, and RAG pipelines.

Timeline:
- MVP: Tuesday (24 hours)
- Early Submission: Friday (4 days)
- Final: Sunday (7 days)

MVP Requirements (Hard Gate):
1. One-on-one chat functionality
2. Real-time message delivery between 2+ users
3. Message persistence (survives app restarts)
4. Optimistic UI updates (messages appear instantly before server confirmation)
5. Online/offline status indicators
6. Message timestamps
7. User authentication (users have accounts/profiles)
8. Basic group chat functionality (3+ users in one conversation)
9. Message read receipts
10. Push notifications working (at least in foreground)
11. Deployment: Running on local emulator/simulator with deployed backend

Core Messaging Infrastructure:
- Real-time message delivery
- Offline message queuing and sync
- Handle poor network conditions (3G, packet loss, intermittent)
- Optimistic UI updates
- Message states: sending, sent, delivered, read
- Group chat with 3+ users
- Profile pictures and display names
- Basic media support (images minimum)
- Typing indicators

Testing Scenarios:
- Two devices chatting in real-time
- One device offline → receiving messages → coming back online
- Messages while app backgrounded
- App force-quit and reopened (persistence test)
- Poor network conditions
- Rapid-fire messages (20+ quickly)
- Group chat with 3+ participants

**Chosen Options:**
- **Platform**: React Native with Expo
- **Backend**: Firebase (Firestore for real-time DB, Auth for users, Cloud Functions for AI calls, FCM for push notifications)
- **AI Integration**: Hybrid Approach - Both a dedicated AI assistant AND contextual features
- **User Persona**: Remote Team Professional
  - Pain points: Drowning in threads, missing important messages, context switching, time zone coordination
- **AI Features (Required 5 + 1 Advanced)**:
  1. Thread summarization - Condense long conversation threads
  2. Action item extraction - Pull out tasks and TODOs from messages
  3. Smart search - RAG-powered search over chat history
  4. Priority message detection - Flag urgent/important messages
  5. Decision tracking - Track decisions made in conversations
  **Advanced**: Multi-Step Agent - Plans team offsites, coordinates schedules autonomously (requires function calling, memory, multi-turn conversations)
- **Deployment Target**: Expo Go (local development + shareable QR code), Firebase backend deployed to production

**Tech Stack Justifications:**
- React Native + Expo: Cross-platform (iOS/Android) from single codebase, fastest development
- Expo Router: File-based routing, familiar to web developers
- Expo SQLite: Local message persistence, works offline
- Firebase Firestore: Real-time sync out of the box, handles online/offline seamlessly
- Firebase Auth: Drop-in authentication, social providers ready
- Firebase Cloud Functions: Serverless AI calls, keeps API keys secure
- FCM (Firebase Cloud Messaging): Push notifications to both platforms
- OpenAI GPT-4 + RAG: Industry-standard LLM, excellent function calling support
- Expo Go: No TestFlight/Play Store delays, instant sharing via QR

---

Output the PRD in clean markdown with clear headings, tables where helpful, and concise language.
Do **not** write code yet.
Do **not** mention BMAD, agents, or implementation steps.
Focus only on clarity, completeness, and decision-making support.
```

---

## Key Decisions Made

### Why Remote Team Professional Persona?
- Aligns with my current workflow (distributed teams)
- AI features are highly practical (not gimmicky)
- Multi-step agent capability is challenging but achievable

### Why Hybrid AI Approach?
- Dedicated chat: Easy to implement, low friction for users
- Contextual features: More powerful UX, feels integrated
- Together: Covers both "ask the AI" and "AI helps me" use cases

### Why Firebase?
- Real-time sync is built-in (critical for messaging)
- Offline support is automatic
- Cloud Functions keep OpenAI API keys secure
- Familiar stack, reduces learning curve

### Why Expo over Native?
- One week timeline is aggressive
- Cross-platform from day 1
- Expo Go deployment is instant (no app store delays)
- Can always eject to bare React Native later if needed

---

## Expected PRD Output Sections

The AI agent should generate:

1. **User Stories** (8-12 stories)
   - Remote worker sending urgent message
   - Team lead reviewing action items from group chat
   - Developer searching for previous technical decision
   - Manager getting summary of 100+ message thread
   - AI assistant autonomously suggesting meeting times

2. **MVP Features** (ruthlessly scoped)
   - Basic messaging infrastructure (real-time, offline, persistence)
   - All 5 core AI features
   - Hybrid AI interface (chat + contextual)
   - NO advanced agent in MVP (post-MVP)
   - NO media beyond images
   - NO voice/video

3. **Tech Stack** (with one-line justifications)
   - Clear reasoning for each choice
   - No alternatives presented (decision already made)

4. **Out of Scope** (explicitly called out)
   - End-to-end encryption
   - Voice messages
   - Video calls
   - Advanced media editing
   - Multi-Step Agent (post-MVP)
   - Custom emoji/stickers

5. **Risks & Mitigations**
   - Firebase costs with heavy usage
   - OpenAI API latency for AI features
   - Expo Go limitations vs. native features
   - Message ordering in group chats under poor network
   - RAG pipeline accuracy with limited context

---

## Next Steps

1. **Submit prompt to Cursor**
2. **Review generated PRD** - Check for completeness, accuracy
3. **Refine** - Adjust scope, clarify risks
4. **Approve** - Lock in the PRD
5. **Implement using BMAD** - Break down → Make → Approve → Deploy

---

## Observations
- The prompt focuses AI on MVP only (critical for tight timeline)
- Explicit tech stack prevents agent from suggesting alternatives
- Risk section helps anticipate problems before coding
- User stories ground features in real user needs

## Related
- [[workflows/project-initialization]] - The workflow this example demonstrates
- [[templates/prd-prompt-template]] - The reusable template used here
- [[tools/cursor]] - Where this prompt will be submitted
- [[tools/firebase]] - Backend infrastructure choice

---

**Tags**: #example #prd #chatiq #messaging-app #ai-features
**Status**: Ready to submit to Cursor
**Project**: ChatIQ (Gauntlet AI MessageAI)
