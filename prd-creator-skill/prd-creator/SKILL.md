---
name: prd-creator
description: Professional PRD creation guide. Guides users through idea discovery to a structured PRD using the company standard template. Always outputs final PRD in English.
---

# PRD Creator

## Overview
This skill assists in building comprehensive Product Requirement Documents (PRDs). It facilitates a discovery phase to clarify ideas and ensures the final documentation adheres to the official `PRD Template.md`.

## Core Workflow
Follow the stages in the professional workflow defined in [references/workflow.md](references/workflow.md):

0. **Context Initialization**: Establish project background and storage strategy (`Global_Context.md` vs Single PRD). **MANDATORY**: User must confirm context distillation before proceeding.
1. **Idea Discovery**: Dig deep with 3-5 strategic questions. Strictly separate "Discovery" from "Logic Deep Dive".
2. **Scope & Priority**: Define P0/P1/P2 features.
3. **Logic Details**: Clarify business rules and dependencies. Includes a "Controlled Brainstorming" sub-phase for specific features.
4. **Final Output**: Generate the document using the standard [references/PRD Template.md](references/PRD Template.md).

## Execution & Control Policy (CRITICAL)
- **Workflow Status Checklist**: EVERY response MUST include a `[Workflow Status]` checklist (e.g., `[v] Stage 0 [ ] Stage 1 ...`) to prevent "auto-pilot".
- **Hard-Gate Confirmation**: AI MUST wait for explicit user confirmation that the current point is resolved before proposing the next. Do NOT skip confirmation gates for stage transitions.
- **Strict Phase Control**: Do NOT assume a phase is complete until the user explicitly says "Phase Complete" or "Move to next feature".
- **Workflow Pacing**: Maintain consistency with previous context. Proposing the next feature before the current PRD is fully polished is a violation of policy.
- **Zero-Tolerance for Pollution**: Strictly separate "Idea Discovery" from "Logic Deep Dive" to prevent context pollution.

## Quality & Formatting Rigor (CRITICAL)
- **Anti-Formatting Decay**: Fields like `Interaction Feedback Strategy`, `Triggers & Pre-conditions`, and `Success Criteria` MUST always use multi-line lists or bullet points. NEVER bunch them into a single paragraph.
- **Visual Component Persistence**: Mermaid diagrams, flowcharts, or wireframe references approved in earlier stages MUST be carried forward into ALL subsequent PRD versions. A document update should never result in the removal of previously confirmed visualizations.

## Language & Output Policy
- **Interaction (CRITICAL)**: 
  - AI MUST follow the user's language preference for the discussion (e.g., Chinese for discovery).
- **Final PRD Language**: The final generated PRD **MUST be in English**.
- **File Management**: 
  - **MANDATORY**: All generated files (.md, .docx, etc.) MUST be stored within the workspace directory. NEVER use system/temp folders.
  - **Filename Confirmation**: Propose a professional name (e.g., `PRD_[ProjectName].md`) and get user confirmation before saving.
- **Terminology & Clarity**: Use professional engineering-standard terminology. Avoid vague phrasing or redundant qualifiers (e.g., do not use "Success Criteria (Exit Criteria)").
- **Visualizations (Optional)**: Use **Mermaid.js**. ALWAYS ask for confirmation before generating.

## Template Strictness (CRITICAL)
1. **Zero Omission**: Keep ALL template sections. Mark as "None" if empty.
2. **Format Fidelity**: Maintain exact table structures and header levels.

## Resources (Relative to skill directory)
- `references/PRD Template.md`: The official standard template for final output.
- `references/workflow.md`: Step-by-step guidance.
