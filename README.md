# ocopy

This repository contains the `opencode` skill definition used to guide code generation and editing tasks.

## How to use

- Open `SKILL.md` to review the skill description, usage guidelines, and examples.
- Ask the assistant to use the `opencode` skill for implementation, refactoring, or test creation tasks.
- Example prompts:
  - "Add a new command to list templates in the CLI."
  - "Refactor the parser module to improve validation and error handling."
  - "Generate unit tests for the input sanitization logic."

## Add this skill to opencode

### 1. Local opencode CLI

If you are using the opencode CLI locally:

1. Place `SKILL.md` at the repository root or inside the configured skills directory.
2. Confirm your opencode config points to the skill file or directory. For example:

```yaml
skills:
  - ./SKILL.md
```

3. Restart or reload the opencode CLI so it discovers the new skill.

#### Linux

```bash
cd /path/to/your/repo
cp SKILL.md /path/to/opencode/skills/  # or move to repo root
```

#### macOS

```bash
cd /path/to/your/repo
cp SKILL.md /path/to/opencode/skills/  # or move to repo root
```

#### Windows

Using PowerShell:

```powershell
Set-Location C:\path\to\your\repo
Copy-Item SKILL.md C:\path\to\opencode\skills\
```

Or using Command Prompt:

```cmd
cd C:\path\to\your\repo
copy SKILL.md C:\path\to\opencode\skills\
```

### 2. VS Code / GitHub Copilot with opencode compatibility

If you use opencode through VS Code or a Copilot integration:

1. Ensure the workspace contains `SKILL.md`.
2. If the integration reads skill metadata, verify the file includes:

```yaml
name: saas-landing-page
compatibility: opencode
```

3. Reload the workspace or extension to refresh skill discovery.

### 3. Skill manifest or config-based setups

If your installation uses a manifest or centralized config:

1. Add a reference to `SKILL.md` in the manifest entries.
2. Example manifest entry:

```yaml
- name: saas-landing-page
  path: ./SKILL.md
  compatibility: opencode
```

3. Reload the service or configuration so the skill becomes active.

## Notes

- Keep requests focused and specific to get the best results.
- The skill is designed to produce practical, maintainable code changes.

