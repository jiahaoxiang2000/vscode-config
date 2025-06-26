# GitHub Copilot Customization in VS Code

This workspace supports customizing GitHub Copilot's AI responses in Visual Studio Code using the following methods:

## 1. Custom Instructions

- **Purpose:** Define guidelines or rules for code generation, code review, commit messages, etc.
- **How:**
  - Add a `.github/copilot-instructions.md` file for workspace-wide instructions (applies to all chat requests).
  - Create `.instructions.md` files for task- or file-specific instructions (can use metadata like `applyTo: "**"`).
  - Set instructions in VS Code settings for user or workspace scope (e.g., `github.copilot.chat.codeGeneration.instructions`).
- **Tips:**
  - Keep instructions short and self-contained.
  - Organize by topic or task using multiple files.
  - Avoid conflicting or redundant instructions.

## 2. Prompt Files (Experimental)

- **Purpose:** Define reusable prompts for common tasks (e.g., code generation, code review).
- **How:**
  - Store prompt files as `.prompt.md` in `.github/prompts` (workspace) or user profile (global).
  - Use Markdown formatting and optional metadata (e.g., `mode`, `tools`).
  - Reference other files or variables for context.
- **Usage:**
  - Run via Command Palette, chat input (`/prompt-name`), or editor play button.
  - Prompts can reference instruction files for additional guidelines.

## 3. Chat Modes in Copilot Chat

> Custom chat modes are available as of VS Code release 1.101 and are currently in preview.

- **Purpose:** Chat modes are configurations that tailor Copilot Chat's behavior for specific tasks (e.g., asking questions, editing code, autonomous coding).
- **Custom Chat Modes:**
  - Define your own modes with `.chatmode.md` files (workspace: `.github/chatmodes/`, or user profile).
  - Each file includes a metadata header (description, tools) and body (instructions/guidelines).
  - Reference instruction files and select available tools for each mode.
  - Create and manage modes via Command Palette (e.g., Chat: New Mode File, Chat: Configure Chat Modes).
- **Use Cases:**
  - Tailor chat for planning, research, or any specialized workflow by creating custom modes.

## References

- [Copilot Customization Docs](https://code.visualstudio.com/docs/copilot/copilot-customization)
- [Prompt Files](https://code.visualstudio.com/docs/copilot/copilot-customization#_prompt-files-experimental)
- [Copilot Chat Modes Docs](https://code.visualstudio.com/docs/copilot/chat/chat-modes)

For more details and examples, see the official documentation linked above.
