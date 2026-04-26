# PRD Creator Skill for Gemini CLI

A professional agent skill to facilitate the creation of high-quality Product Requirement Documents (PRDs) following industry and company standards.

## Features
- **Guided Discovery**: 4-stage guided process from idea to final PRD.
- **Progressive Deep Dive**: Dynamically asks for Triggers, Pre-conditions, and User Journeys when needed.
- **Multilingual Support**: Discuss in Chinese or English; output always in professional English.
- **Visualizations**: Optional Mermaid.js flowchart generation.
- **Markdown Export**: Generates structured `.md` files locally with standard templates.

## Installation

### Prerequisites
- [Gemini CLI](https://github.com/google/gemini-cli) installed and configured.

### Option 1: Global Installation (Recommended)
To use this skill across all your projects:
1. Download the `prd-creator.skill` file.
2. Run the installation command:
   ```bash
   gemini skills install prd-creator.skill
   ```

### Option 2: Workspace Installation
To limit this skill to the current project directory only:
```bash
gemini skills install prd-creator.skill --scope workspace
```

### Option 3: Developer Mode (Link from Source)
If you are developing or customizing the skill, link directly to the source folder:
```bash
gemini skills link ./prd-creator-skill/prd-creator
```

## How to Use

Simply trigger the skill by mentioning "PRD" or "Product Requirement" in your prompt, or activate it manually:
```bash
/skills activate prd-creator
```

**Example Prompts:**
- "Help me write a PRD for a new smart watch sync feature."
- "我想为一个 AI 聊天机器人写一份 PRD。"
- "Create a system-level PRD for our new billing service."

### The Workflow
1. **Idea Discovery**: AI asks 3-5 questions to clarify your vision.
2. **Scope**: Define feature priorities (P0/P1/P2).
3. **Deep Dive**: Define logic, triggers, and optional Mermaid flowcharts.
4. **Finalization**: Confirm the document name and generate files.

## Contributing
The source files are located in the `prd-creator/` directory. Feel free to submit PRs for template improvements or workflow optimizations.

## License
MIT
