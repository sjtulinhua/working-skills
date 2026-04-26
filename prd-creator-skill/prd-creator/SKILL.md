---
name: prd-creator
description: Professional PRD creation guide. Guides users through idea discovery to a structured PRD using the company standard template. Always outputs final PRD in English.
---

# PRD Creator

## Overview
This skill assists in building comprehensive Product Requirement Documents (PRDs). It facilitates a discovery phase to clarify ideas and ensures the final documentation adheres to the official `PRD Template.md`.

## Core Workflow
Follow the stages in the professional workflow defined in [references/workflow.md](references/workflow.md):

0. **Context Initialization**: Establish project background, business goals, and determine context storage strategy (Global vs Single).
1. **Idea Discovery**: Dig deep with 3-5 strategic questions.
2. **Scope & Priority**: Define P0/P1/P2 features.
3. **Logic Details**: Clarify business rules and dependencies.
4. **Final Output**: Generate the document using the standard [references/PRD Template.md](references/PRD Template.md).

## Language & Output Policy
- **Interaction (CRITICAL)**: 
  - AI MUST follow the user's language preference for the discussion. 
  - If the user interacts in Chinese, the entire discovery and logic clarification process MUST be conducted in Chinese.
- **Final PRD Language**: The final generated PRD (both Markdown and Word) **MUST be in English** regardless of the interaction language.
- **Visualizations (Optional)**: If the user requests a visual representation of a journey or logic, use **Mermaid.js** syntax within the Markdown. ALWAYS ask the user for confirmation before generating a flowchart.
- **Output & Integration (CRITICAL)**: 
  1. **Filename Confirmation**: Before saving the file, suggest a professional name (e.g., `PRD_[ProjectName].md`) and ask the user to confirm.
  2. **Local Markdown**: After name confirmation, save the final PRD as a `.md` file using the `write_file` tool.
  3. **Visualizations Inclusion**: If the user has confirmed any Mermaid diagrams or visual logic during the process, **YOU MUST** include the full Mermaid code blocks in the relevant sections of the final `.md` file. Do NOT omit them.
- **Template Strictness (CRITICAL)**: 
  1. **Zero Omission**: The final PRD MUST contain ALL sections defined in the template. Do NOT remove any headers (e.g., "Non-functional Requirements", "Dependencies") even if no content is currently available. Mark them as "None" or "To be identified".
  2. **Format Fidelity**: Keep the exact table structures (e.g., Priority table) and Markdown header levels (H1, H2, H3) as specified in the template.
  3. **Metadata**: Ensure the "Product manager" field is correctly filled based on user input or left empty if not provided.

## Resources (Relative to skill directory)
- `references/PRD Template.md`: The official standard template for final output.
- `references/workflow.md`: Step-by-step guidance.
