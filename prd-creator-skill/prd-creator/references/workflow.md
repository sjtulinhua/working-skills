# PRD Creation Workflow

This skill adopts a "progressive disclosure" guided design.

## Stage 0: Context Initialization
- **Goal**: Establish the project background and business objectives before defining features.
- **Action**:
  1. Ask the user for a brief description of the project's background and goals.
  2. **Progressive Q&A**: Ask targeted questions to fill in missing context (e.g., target audience, business metrics, system constraints, user pain points).
  3. **Context Distillation**: Summarize the gathered information into a professional "Project Background" and "Objectives" (including success metrics).
  4. **Storage Strategy**: Ask the user if this is a large, multi-PRD project or a single-PRD project.
     - If large: Suggest saving this context as a standalone `Global_Context.md` for future PRDs.
     - If single: Inform the user it will be included directly in the PRD's Introduction section.

## Stage 1: Idea Discovery
- **Goal**: Understand the user's core requirements.
- **Action**: Ask 3-5 strategic questions based on the user's idea.
- **Confirmation**: Summarize and confirm the background.

## Stage 2: Scope Definition
- **Goal**: Define the product boundaries.
- **Action**: List features and categorize them into P0 (Core), P1 (Important), and P2 (Nice-to-have).
- **Confirmation**: Finalize the feature list and priorities with the user.

## Stage 3: Logic Flow & Visualization
- **Goal**: Refine core paths and dive deep into functional details.
- **Action**: 
  1. Describe basic business processes for P0/P1 features.
  2. **Progressive Deep Dive**: Ask if specific features need detailed **Triggers**, **Pre-conditions**, **Exit Criteria**, or a **User Journey**.
  3. **Visual Confirmation (Optional)**: If a User Journey is defined, ask: "Would you like me to generate a **Mermaid flowchart** to visualize this journey for stakeholders?" Only generate the code block if the user says "Yes".
- **Confirmation**: Ensure logic closure.

## Stage 4: Naming & Final Generation
- **Goal**: Confirm the document name and output the complete files.
- **Action**: 
  1. **Naming Suggestion**: Propose a professional filename based on the project (e.g., `PRD_[ProjectName]_V1.md`). Ask: "I suggest naming the document '[Suggested Name]'. Do you accept this, or would you like to provide a different name?"
  2. **File Generation**: Once the name is confirmed, accurately fill in the `references/PRD Template.md`. Ensure the PRD content is in **English**.
  3. **Local Save (Markdown)**: Use `write_file` to save the content using the confirmed name.
- **Completion**: Present the final file paths to the user.

## Important Notes
- **User Control**: ALWAYS get user confirmation for visualizations and filenames before proceeding.
- **Do not rush**: Wait for user confirmation at the end of each stage.
- **Maintain professionalism**: Provide suggestions for names and logic flows when the user is unsure.