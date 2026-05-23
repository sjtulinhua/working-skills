# Skill Iteration Backlog: Phase 2 (Quality & Rigor)

## 🚀 High-Priority Fixes

1. **Anti-Formatting Decay**:
   - **MANDATORY**: Template fields like `Interaction Feedback Strategy`, `Triggers & Pre-conditions`, and `Success Criteria` MUST always use multi-line lists or bullet points. Never bunch them into a single paragraph.
   - **Reason**: Readability for engineering and QA teams is paramount.

2. **Strict Phase Control**:
   - **MANDATORY**: Do NOT assume a phase is complete until the user explicitly says "Phase Complete" or "Move to next feature". 
   - **Constraint**: Proposing the next feature before the current PRD is fully polished is a violation of the Pacing policy.

3. **Terminology & Clarity**:
   - **MANDATORY**: Ensure terms like `Success Criteria` do not have redundant or confusing qualifiers like `(Exit Criteria)` attached.
   - **MANDATORY**: Use professional, clear, and engineering-standard terminology.

4. **Sensible Baselines for Latency & Performance**:
   - **MANDATORY**: When proposing technical latencies, use sensible industry baselines (e.g., 3~4s for agent initiation). Think critically instead of using unrealistic values.

5. **File & Backlog Management**:
   - **MANDATORY**: Consolidate all iteration items into `Skill_Iteration_Backlog_Phase2.md`. Do not create new versioned backlog files unless explicitly requested.

6. **Visual Component Persistence**:
   - **MANDATORY**: Mermaid diagrams, flowcharts, or wireframe references approved in earlier stages MUST be carried forward into all subsequent PRD versions. 
   - **Constraint**: A document update (e.g., for formatting or specific logic refinement) should never result in the removal of previously confirmed visualizations.

7. **Agile Workflow for Complex PRDs**:
   - [x] For PRDs containing multiple large features (e.g., 5+ use cases), adopt an agile iteration workflow instead of a single Stage 4 dump. Establish the document skeleton and common logic first, then iterate through Stages 1-3 and write the Stage 4 content for each feature *one by one* before moving to the next.

8. **Enforce Passive Execution Engine**:
   - [x] Update `prd-creator/SKILL.md` system prompt to mandate the "Passive Execution Engine" persona and "Hard Stop" formatting to permanently suppress the LLM's proactive "helpful" bias that overrides strict pacing rules.

9. **Justified Template Deviation**:
    - [x] While strict format fidelity is the default, if a deviation from the template (e.g., adding a custom consolidated section like `Architecture & Common Logic`) significantly improves readability or comprehension for the target engineering/design audience, the AI MUST suggest this deviation to the user for consideration. This suggestion must be targeted and never advocate for abandoning the core template structure entirely.

## 📝 Previous Progress (Archived from Backlog v1)
- [x] Stage 0 Enhancement (Global Context)
- [x] Controlled Brainstorming Integration
- [x] File Management Standards (Local Workspace)
- [x] Terminology & Clarity (Avoid "Feedback Balance")
