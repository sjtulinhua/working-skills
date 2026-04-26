# PRD Creation Workflow

This skill adopts a "progressive disclosure" guided design with strict execution gates.

## Stage 0: Context Initialization
- **Goal**: Establish the project background and business objectives before defining features.
- **Action**:
  1. **Detection**: Check if a `Global_Context.md` already exists in the workspace.
  2. **Storage Strategy Selection**: Ask the user: "Is this a **Single PRD** project, or part of a **Large/Multi-PRD** project?"
     - If Multi-PRD: Propose creating/updating `Global_Context.md`.
  3. **Context Gathering**: Ask targeted questions (target audience, business metrics, system constraints, user pain points).
  4. **MANDATORY Context Distillation**: Summarize findings into "Project Background" and "Objectives".
  5. **HARD GATE**: AI MUST wait for explicit user confirmation of the distillation before proceeding to features.

## Stage 1: Idea Discovery
- **Goal**: Understand core requirements while strictly avoiding logic deep-dives.
- **Action**: Ask 3-5 strategic questions. Keep this phase at the "Discovery" level to prevent context pollution.
- **Confirmation**: Finalize the conceptual background with user approval.

## Stage 2: Scope & Priority
- **Goal**: Define product boundaries and engineering priorities.
- **Action**: List features categorized by P0 (Must-have), P1 (Should-have), and P2 (Nice-to-have).
- **Confirmation**: Finalize the feature list and priorities. Wait for explicit user approval.

## Stage 3: Logic Flow & Detailed Design
- **Goal**: Refine core paths and functional logic with professional terminology.
- **Action**: 
  1. **Logic Mapping**: Describe business processes using engineering-standard terms (e.g., "Interaction Feedback Strategy", "Notification Logic", "Exception Handling").
  2. **Controlled Brainstorming (Sub-phase)**: For P0/P1 features, offer a deep dive into **Triggers**, **Multi-modal Details**, and **Edge Cases**. Focus ONLY on the current feature to maintain context purity.
  3. **Visual Confirmation**: Propose Mermaid diagrams for complex journeys.
- **Confirmation**: Ensure logic closure and user acceptance of all detailed designs.

## Stage 4: Naming & Final Generation
- **Goal**: Confirm metadata and output standardized documentation.
- **Action**: 
  1. **Naming Suggestion**: Propose a professional filename (e.g., `PRD_[ProjectName]_V1.md`). 
  2. **File Generation**: Populated the official `PRD Template.md` in **English**.
  3. **Local Save**: Save ONLY to the workspace directory.
- **Completion**: Provide local file paths.

## Execution Rules
- **[Workflow Status] Checklist**: Every response must include a status update (e.g., `[v] Stage 0 [>] Stage 1 [ ] Stage 2`).
- **Zero-Tolerance for Auto-Pilot**: Never move to the next stage or propose next steps until the current discussion point is confirmed as resolved by the user.
- **Consistency**: Maintain a unified voice and logic across all turns. Do not provide fragmented or varying points.
- **Terminology**: Use professional, clear, engineering-standard terminology at all times.
