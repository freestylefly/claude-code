# Claude Code

Claude Code is Anthropic's official CLI tool for Claude, providing an interactive coding assistant that helps with software engineering tasks through natural language conversations.

## Overview

Claude Code is a terminal-based application built with React and Ink, offering a rich interactive experience for:
- Code analysis and navigation
- File operations and editing
- Shell command execution
- Task management and tracking
- Git operations
- And much more

## Architecture

### Technology Stack
- **Runtime**: Bun
- **UI Framework**: React + Ink (for terminal UI)
- **Language**: TypeScript
- **State Management**: Custom state management with React hooks

### Key Components

#### Core Systems
- **Commands** (`src/commands/`): CLI command implementations including git operations, file management, and configuration
- **Tools** (`src/tools/`): Agent tools for various operations (Bash, File, Grep, etc.)
- **Components** (`src/components/`): React components for the terminal UI
- **Services** (`src/services/`): Backend services for API calls, analytics, and integrations

#### Entry Points
- **CLI Entry** (`src/entrypoints/cli.tsx`): Main CLI entry point
- **Init** (`src/entrypoints/init.ts`): Initialization logic
- **Main** (`src/main.tsx`): Core application orchestration

#### Specialized Features
- **Skills** (`src/skills/`): Extensible skill system for custom capabilities
- **MCP** (`src/services/mcp/`): Model Context Protocol integration
- **Vim** (`src/vim/`): Vim keybinding support
- **Ink** (`src/ink/`): Custom terminal rendering engine

## Features

### Interactive Assistance
- Natural language code queries
- Context-aware suggestions
- Multi-step task execution
- Agent-based automation

### File Operations
- Read/write/edit files with safety checks
- Pattern-based file search (Glob)
- Content search (Grep)
- Syntax-aware editing

### Development Tools
- Bash command execution with permission controls
- Git integration (status, diff, commit, push)
- LSP support for code intelligence
- Notebook editing (.ipynb files)

### Project Management
- Task creation and tracking
- Plan mode for complex implementations
- Worktree support for isolated environments
- Session history and resumption

### Safety & Control
- Permission-based tool execution
- Sandbox mode for bash commands
- Configurable safety rules
- User confirmation for destructive actions

## Installation

```bash
# Clone the repository
git clone https://github.com/freestylefly/claude-code.git

# Navigate to the project directory
cd claude-code

# Install dependencies (requires Bun)
bun install
```

## Usage

```bash
# Start Claude Code
bun run start

# Or use the CLI directly
bun run cli
```

## Development

```bash
# Run in development mode
bun run dev

# Build the project
bun run build

# Run tests
bun test

# Type check
bun run typecheck

# Lint
bun run lint
```

## Project Structure

```
├── src/
│   ├── assistant/       # Assistant mode functionality
│   ├── bootstrap/       # Application bootstrap
│   ├── bridge/          # Bridge communication
│   ├── buddy/           # Buddy system
│   ├── cli/             # CLI utilities
│   ├── commands/        # Command implementations
│   ├── components/      # React components
│   ├── constants/       # Constants
│   ├── context/         # Context management
│   ├── coordinator/     # Coordinator mode
│   ├── entrypoints/     # Application entry points
│   ├── history.ts       # History management
│   ├── hooks/           # React hooks
│   ├── ink/             # Terminal rendering
│   ├── interactiveHelpers.tsx
│   ├── keybindings/     # Keybinding definitions
│   ├── main.tsx         # Main orchestration
│   ├── memdir/          # Memory directory
│   ├── migrations/      # Data migrations
│   ├── plugins/         # Plugin system
│   ├── query.ts         # Query handling
│   ├── QueryEngine.ts   # Query engine
│   ├── remote/          # Remote functionality
│   ├── replLauncher.tsx # REPL launcher
│   ├── schemas/         # Data schemas
│   ├── screens/         # Screen definitions
│   ├── server/          # Server functionality
│   ├── services/        # Backend services
│   ├── setup.ts         # Setup logic
│   ├── skills/          # Skill system
│   ├── state/           # State management
│   ├── tasks/           # Task system
│   ├── tools/           # Tool implementations
│   ├── types/           # TypeScript types
│   ├── utils/           # Utility functions
│   ├── vim/             # Vim keybindings
│   └── voice/           # Voice functionality
├── package.json
├── tsconfig.json
└── README.md
```

## Key Technologies & Dependencies

- **Bun**: Fast JavaScript runtime and bundler
- **React**: UI framework
- **Ink**: React for interactive command-line apps
- **Commander.js**: CLI framework
- **Chalk**: Terminal styling
- **Zod**: Schema validation
- **TypeScript**: Type-safe JavaScript

## Contributing

This is Anthropic's official Claude Code tool. Contributions should align with the project's goals and coding standards.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Copyright © Anthropic PBC

This project is proprietary software owned by Anthropic.

## Acknowledgments

- Built by [Anthropic](https://anthropic.com)
- Powered by [Claude](https://claude.ai)

## Support

For support, visit [support.anthropic.com](https://support.anthropic.com) or open an issue on GitHub.
