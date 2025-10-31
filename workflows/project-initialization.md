# Project Initialization Workflow
_Last updated: 2025-10-30_

## Goal
Standardized process for taking a rough project idea and turning it into a clear, implementable Product Requirements Document (PRD) with chosen tech stack.

## Overview
This workflow bridges the gap between "I want to build X" and "Here's exactly how to build X with Y stack." It uses AI agents (like Cursor) to generate comprehensive PRDs that are optimized for BMAD (Break down, Make, Approve, Deploy) implementation.

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

**Output**: Complete project context document

---

### Step 3: Generate PRD via AI Agent
**Tool**: [[tools/cursor]] or [[tools/claude-code]]

**Process**:
1. Use the [[templates/prd-prompt-template|PRD Prompt Template]]
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

### Step 4: Review & Refine PRD
**Actions**:
1. Review generated PRD for accuracy
2. Validate tech stack choices
3. Adjust scope if needed
4. Get stakeholder approval if applicable

**Output**: Approved, final PRD

---

### Step 5: Implementation (BMAD Method)
**Process**:
1. **Break down**: Agent breaks PRD into tasks
2. **Make**: Implement features incrementally
3. **Approve**: Review and test each component
4. **Deploy**: Ship to production/staging

**Output**: Working MVP

---

## Current Setup
1. Using [[templates/prd-prompt-template|PRD Prompt Template]] for Cursor/AI agents
2. Firebase + React Native/Expo as default stack for rapid prototyping
3. Hybrid AI approach (dedicated assistant + contextual features)

## Tools Used
- [[tools/cursor]] - AI code editor for PRD generation and implementation
- [[tools/claude-code]] - Alternative AI agent for planning
- [[tools/firebase]] - Backend infrastructure
- [[templates/prd-prompt-template]] - Reusable prompt template

## Examples
- [[ai-drafts/chatiq-prd-example]] - WhatsApp clone with AI features for remote teams

## Problems / Pain Points
- Initial ideas are often too vague for implementation
- Tech stack decisions require deep knowledge of tradeoffs
- Easy to over-scope MVP and miss deadlines
- AI agents need very specific prompts to generate useful PRDs

## Changes Tried
- [x] Created reusable PRD prompt template with placeholders
- [x] Structured prompt to focus on MVP vs. post-MVP features
- [x] Added explicit risk/pitfall section for tech stack decisions
- [ ] Test prompt with multiple project types
- [ ] Refine based on agent output quality

## Next Steps
1. Use template for ChatIQ messaging app project
2. Validate PRD generation quality with Cursor
3. Document any template improvements needed
4. Create library of project examples

## Related Resources
- [[templates/prd-prompt-template]] - The core reusable template
- [[ai-drafts/chatiq-prd-example]] - First example project
- [[tools/cursor]] - Primary implementation tool
- [[workflows/current]] - Current active workflow

## Notes
> This workflow is designed to work with AI coding agents that support BMAD methodology. The PRD should be detailed enough that the agent can implement autonomously with minimal clarification.

> Key insight: The quality of the PRD directly impacts implementation speed. Spending 30-60 minutes on a solid PRD saves hours in development.

---

**Tags**: #workflow #project-planning #prd #ai-agents #cursor
**Status**: Active - In use for ChatIQ project
