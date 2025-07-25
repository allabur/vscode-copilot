# VS Code Copilot Instructions Template Repository

This repository provides comprehensive templates and configurations for customizing GitHub Copilot in VS Code. Understanding the architecture and conventions will help you effectively contribute and maintain this system.

## Architecture Overview

The repository follows a modular template system with three main components:

- **`instructions/`** - Scoped instruction files that auto-apply based on file patterns (`applyTo` frontmatter)
- **`prompts/`** - Reusable AI workflows with variable substitution and tool specifications
- **`settings-template.json`** - VS Code configuration that wires everything together

## Key Patterns & Conventions

### Instruction File Structure
All instruction files follow this pattern:
```markdown
---
description: "Brief description of the instruction scope"
applyTo: "**/*.{file,extensions}"
---
# Title
Content with specific, actionable guidelines
```

**Critical**: The `applyTo` pattern determines when instructions are automatically included. Use precise glob patterns to avoid conflicts.

### Settings Configuration Architecture
The `settings-template.json` uses three distinct instruction categories:
- `github.copilot.chat.codeGeneration.instructions` - For general coding
- `github.copilot.chat.testGeneration.instructions` - For test-specific guidance  
- `github.copilot.chat.reviewSelection.instructions` - For code review workflows

### Prompt File Variables
Prompts support dynamic content through variable substitution:
- `${input:variableName:placeholder}` - User input prompts
- `#githubRepo owner/repo` - External repository references
- Tool specifications via frontmatter (`tools: ["githubRepo", "codebase"]`)

## Development Workflows

### Adding New Instructions
1. Create `.instructions.md` file in `instructions/` directory
2. Add frontmatter with `description` and precise `applyTo` pattern
3. Update `settings-template.json` to reference the new file
4. Test with target file types to verify scoping

### Creating Reusable Prompts
1. Define prompt in `prompts/` with `.prompt.md` extension
2. Specify `mode: "agent"` and required `tools` in frontmatter
3. Use descriptive variable names with placeholder text
4. Reference existing instruction files for consistency

### Path Management
**Windows-specific**: All paths in `settings-template.json` use double backslashes (`\\`) for proper escaping. When customizing for other environments, update the absolute paths in:
- `chat.instructionsFilesLocations`
- `chat.promptFilesLocations` 
- Individual instruction file references

## Technology-Specific Conventions

### Python Files (`**/*.py`)
- Use NumPy docstring format consistently
- Enforce modern type hints (Python 3.9+ syntax: `str | None` vs `Optional[str]`)
- Apply `python-coding.instructions.md` for PEP 8 and performance patterns

### JavaScript/TypeScript (`**/*.{js,ts,jsx,tsx}`)
- Prefer modern ES6+ syntax and TypeScript strict mode
- Follow React patterns documented in `frontend.instructions.md`
- Use conventional commit format for all changes

### Documentation (`**/*.md`)
- Follow Microsoft documentation style guide patterns
- Use consistent formatting as defined in `docs-writing.instructions.md`
- Include proper frontmatter for instruction files

## Integration Points

### VS Code Settings Integration
The template integrates with VS Code through:
- `github.copilot.enable` - Controls Copilot activation per file type
- `chat.instructionsFilesLocations` - Auto-discovery of instruction files
- File nesting patterns for organized project explorer

### Git Integration
- Conventional Commits enforced through `commit-messages.instructions.md`
- PR templates defined in `pull-request.instructions.md`
- Branch naming conventions documented in `docs/AGENTS.md`

## Testing & Validation

### Instruction File Testing
- Test each instruction file against its target file patterns
- Verify `applyTo` patterns don't overlap unintentionally
- Validate frontmatter YAML syntax

### Settings Validation
- Use absolute paths for cross-platform compatibility
- Test instruction file auto-loading in VS Code
- Verify prompt file discovery and execution

## Maintenance Notes

### Version Compatibility
- Requires VS Code 1.85+ with GitHub Copilot extension
- Settings template updated for latest Copilot features
- Instruction file patterns follow VS Code customization spec

### Path Customization
When adapting for new environments, update ALL absolute paths in `settings-template.json` to match your directory structure. The current paths are Windows-specific examples.
