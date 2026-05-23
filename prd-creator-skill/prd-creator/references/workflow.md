# Full PRD Creation Workflow

Use this workflow ONLY when the Working Mode is "Full PRD Creation".

## Stage 0: Context Initialization
- **Goal**: Establish background and storage strategy.
- **Action**: Check for `Global_Context.md`. Distill Project Background, Objectives, and Initial Assumptions.
- **Confirmation Gate**: Wait for user confirmation before moving to discovery.

## Stage 1: Idea Discovery
- **Goal**: Clarify core requirements without logic deep-dives.
- **Action**: Ask strategic questions. Establish the physical `Decision Log` & `Open Questions` list in the draft.
- **Confirmation Gate**: Wait for user to confirm the conceptual baseline.

## Optional Stage 1.5: Knowledge Scan
Use this optional step when the domain is unfamiliar, market behavior matters, or the user asks for brainstorming / competitor research.
- **Goal**: Use AI knowledge to reduce product blind spots before scope is finalized.
- **Action**: Research/brainstorm (competitors, UX patterns, technical constraints, edge cases) ONLY within the current product focus.
- **Output Format**: You MUST summarize findings using this exact format to prevent context pollution:
  ```markdown
  ### Knowledge Scan Summary
  **Findings**: [Facts/Research]
  **Product Implications**: [Impact on our PRD]
  **Options**: [Option A, Option B]
  **Open Questions**: [...]
  **Recommended Direction**: [...]
  ```
- **Confirmation Gate**: Do not move to the next stage until the user confirms which findings/options should be adopted.

## Stage 2: Scope & Priority
- **Goal**: Define boundaries (P0/P1/P2).
- **Action**: List features and cross-system dependencies.
- **Confirmation Gate**: Wait for user to approve the scope.

## Stage 3: Logic Flow & Detailed Design
- **Goal**: Refine core paths, edge cases, and functional logic.
- **Action**: Map business logic. Update the `Decision Log` with rejected options and confirmed paths. Propose Mermaid diagrams for complex flows.
- **Confirmation Gate**: Wait for logic closure for the current feature/focus.
### Focus Lock
During detailed design, the AI must stay on the current feature or flow until it is confirmed as complete.
If the current feature still has open questions, unresolved logic, or incomplete PRD fields, do not ask whether to move to the next feature or stage.
Ask only focused questions about the current feature.

## Stage 4: File Generation
- **Goal**: Output standardized, Global English documentation.
- **Action**: Populate `PRD Template.md`. Apply Global English rules. Carry forward visualizations and the Decision Log. Save to workspace with a professional filename.

## Agile Iteration for Complex PRDs
Use when the PRD involves many features, cross-system dependencies, shared architecture, complex edge cases, or multiple user flows.
1. **Skeleton First**: Establish the document skeleton, shared architecture, and non-functional requirements.
2. **Iterate by Feature**: For EACH major feature, run through Stages 1-3. Write that feature's content into the file.
3. **Loop**: Repeat for the next feature after the previous one is confirmed. Update the `[Focus: Feature Name]` in your status anchor.