# PRD Creator Skill for Gemini CLI

A professional Gemini CLI agent skill designed to help you create, review, and polish high-quality Product Requirement Documents (PRDs) following industry standards.

This skill transforms your Gemini CLI into a **Senior Product Partner**. It doesn't just write text; it asks clarifying questions, points out logical gaps, suggests structure, and enforces a rigorous step-by-step workflow.

## ✨ Key Features
- **Guided 4-Stage Workflow**: Takes you systematically from Idea Discovery -> Scope & Priority -> Logic & Design -> Final Markdown File.
- **Strict Pacing (Passive Execution)**: The agent operates with strict pacing control. It will *never* rush ahead or auto-generate entire documents without your explicit confirmation at each stage.
- **Adaptive Formatting**: Automatically chooses between user-facing feature formats (interaction feedback, triggers) and system-level formats (architecture, data flows).
- **Multilingual Input / Global English Output**: You can discuss and brainstorm in Chinese or any other language, but the final PRD output will always be in clear, professional Global English.
- **Visualizations**: Supports generating Mermaid.js flowcharts and state diagrams for complex logic.

---

## 🚀 Installation

To use this skill, you need the [Gemini CLI](https://github.com/google/gemini-cli) installed on your machine.

### Option 1: Global Installation (Recommended)
Installing globally allows you to use the `prd-creator` skill in *any* project or directory on your computer.

1. Clone or download this repository.
2. Open your terminal in the repository root (where `prd-creator.skill` is located).
3. Run the following command:
   ```bash
   gemini skills install prd-creator.skill
   ```

### Option 2: Workspace Installation
If you only want this skill available within a specific project folder:
```bash
gemini skills install prd-creator.skill --scope workspace
```

---

## 💡 How to Use

### 1. Starting a Session
Simply launch Gemini CLI and state that you want to write a PRD. The skill will automatically activate based on your intent.

**Examples:**
* `"Help me write a PRD for a new dark mode toggle feature."`
* `"我想为我们的后台管理系统写一份权限控制的 PRD。"`
* `"Let's create a system-level PRD for a new payment gateway."`

Alternatively, you can manually activate it inside the CLI:
```bash
/skills activate prd-creator
```

### 2. Understanding the Workflow
The agent will guide you through a structured process:

1. **Stage 1: Idea Discovery**: The agent asks a few high-level questions to understand the background and goals.
2. **Stage 2: Scope & Priority**: Defining what is P0 (Must have) vs P1/P2.
3. **Stage 3: Logic Flow & Detailed Design**: Deep dive into triggers, edge cases, and architectures.
4. **Stage 4: File Generation**: The agent generates a structured `.md` file using a standard template.

### 3. 🛑 IMPORTANT: Navigating Stages (The "Hard Stop" Rule)
This skill uses a **Passive Execution Engine**. This means the agent will ask you questions and then **stop and wait**. 

**It will not move to the next feature or stage automatically.** 

When the agent finishes a thought, it will end its message with a separator (`---`) and a question.
To move forward, you **must explicitly confirm**, for example:
* `"Looks good, move to the next stage."`
* `"确认，下一步。"`
* `"This feature is done, let's discuss the next one."`

---

## 🛠️ Development & Customization

If you want to modify the skill's behavior (e.g., changing the PRD template or adjusting the system prompt):

1. The source files are located in the `prd-creator-skill/prd-creator/` directory.
2. Make your changes to `SKILL.md` or the `references/` files.
3. To test your changes locally without repacking, use the link command:
   ```bash
   gemini skills link ./prd-creator-skill/prd-creator
   ```
4. To repackage the `.skill` file, compress the *contents* of the `prd-creator/` folder into a `.zip` archive and rename it to `.skill`.

## License
MIT
