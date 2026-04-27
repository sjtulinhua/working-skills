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
  5. **HARD GATE**: AI MUST wait for explicit user confirmation (e.g., "Phase Complete") before proceeding to features.

## Stage 1: Idea Discovery
- **Goal**: Understand core requirements while strictly avoiding logic deep-dives.
- **Action**: Ask 3-5 strategic questions. Keep this phase at the "Discovery" level to prevent context pollution.
- **Confirmation**: Finalize the conceptual background. Wait for explicit "Phase Complete" from user.

## Stage 2: Scope & Priority
- **Goal**: Define product boundaries and engineering priorities.
- **Action**: List features categorized by P0 (Must-have), P1 (Should-have), and P2 (Nice-to-have).
- **Confirmation**: Finalize the feature list and priorities. Wait for explicit "Phase Complete" from user.

## Stage 3: Logic Flow & Detailed Design
- **Goal**: Refine core paths and functional logic with professional terminology.
- **Action**: 
  1. **Logic Mapping**: Describe business processes using engineering-standard terms.
  2. **Sensible Baselines**: When proposing technical latencies, use sensible industry baselines (e.g., UI response < 100ms, Agent initiation 3~4s). Think critically instead of using unrealistic values.
  3. **Controlled Brainstorming (Sub-phase)**: For P0/P1 features, offer a deep dive into **Triggers**, **Multi-modal Details**, and **Edge Cases**. Focus ONLY on the current feature to maintain context purity.
  4. **Visual Confirmation**: Propose Mermaid diagrams for complex journeys.
- **Confirmation**: Ensure logic closure. Wait for explicit "Phase Complete" for the entire detailed design phase.

## Stage 4: Naming & Final Generation
- **Goal**: Confirm metadata and output standardized documentation.
- **Action**: 
  1. **Naming Suggestion**: Propose a professional filename (e.g., `PRD_[ProjectName]_V1.md`). 
  2. **File Generation**: Populated the official `PRD Template.md` in **English**. **MANDATORY**: Carry forward all previously approved Mermaid diagrams.
  3. **Local Save**: Save ONLY to the workspace directory.
- **Completion**: Provide local file paths.

## Execution Rules
- **[Workflow Status] Checklist**: Every response must include a status update (e.g., `[v] Stage 0 [>] Stage 1 [ ] Stage 2`).
- **Zero-Tolerance for Auto-Pilot**: Never move to the next stage or propose next steps until the current phase is explicitly confirmed as "Phase Complete" by the user.
- **Visual Component Persistence**: Ensure all approved Mermaid diagrams are included in the final output and all subsequent revisions.
- **Terminology**: Use professional, clear, engineering-standard terminology at all times.
