# Agentic Coding Platform

A monorepo containing various AI-powered development tools and Model Context Protocol (MCP) servers for enhanced coding workflows.

## Project Structure

```
mcp/
├── gpt5-mcp/                    # GPT-5 MCP Server
│   ├── servers/gpt5-server/     # TypeScript MCP server implementation
│   ├── docker-compose.yml      # Docker setup
│   └── docs/                   # Project documentation
└── email-orchestrator-mcp/     # Email orchestration MCP server
    └── email-orchestrator-mcp.py
```

## Projects

### 🤖 GPT-5 MCP Server
**Standalone repo:** [gpt5-mcp](https://github.com/makdas/gpt5-mcp)

A TypeScript-based MCP server that provides GPT-5 integration capabilities for Claude Code and other MCP clients.

**Features:**
- Docker containerized deployment
- TypeScript implementation with proper typing
- Integration with Claude Code via MCP protocol

### 📧 Email Orchestrator MCP
**Standalone repo:** [email-orchestrator-mcp](https://github.com/makdas/email-orchestrator-mcp)

A Python MCP server for email automation and orchestration tasks.

## Getting Started

### Prerequisites
- Node.js 18+ (for TypeScript projects)
- Python 3.8+ (for Python projects)
- Docker and Docker Compose
- Git

### Setup

1. **Clone the monorepo:**
   ```bash
   git clone https://github.com/makdas/agentic_coding.git
   cd agentic_coding
   ```

2. **Individual project setup:**
   - See individual project READMEs in their respective directories
   - Each project can be run independently

3. **Docker setup (GPT-5 MCP):**
   ```bash
   cd mcp/gpt5-mcp
   docker-compose up -d
   ```

## Development Workflow

### Monorepo Structure
This repository uses **git subtrees** to maintain both a unified monorepo and standalone project repositories.

### Making Changes

1. **Work in the monorepo:**
   ```bash
   # Make changes in mcp/gpt5-mcp/ or mcp/email-orchestrator-mcp/
   git add .
   git commit -m "Your changes"
   git push origin main
   ```

2. **Sync to standalone repos:**
   ```bash
   # Update GPT-5 MCP standalone repo
   git subtree push --prefix=mcp/gpt5-mcp origin-gpt5mcp main
   
   # Update Email Orchestrator standalone repo
   git subtree push --prefix=mcp/email-orchestrator-mcp origin-email-orchestrator main
   ```

### For Contributors

If you want to contribute to a specific project:

**Option 1: Work with standalone repos**
```bash
git clone https://github.com/makdas/gpt5-mcp.git
# Make your changes and submit PR
```

**Option 2: Work with the monorepo**
```bash
git clone https://github.com/makdas/agentic_coding.git
# Make changes in the appropriate mcp/ subdirectory
```

### Cloning Individual Projects

You can clone individual projects without the full monorepo:

```bash
# Clone only GPT-5 MCP
git clone https://github.com/makdas/gpt5-mcp.git

# Clone only Email Orchestrator
git clone https://github.com/makdas/email-orchestrator-mcp.git
```

## Repository Links

- **Main Monorepo:** https://github.com/makdas/agentic_coding
- **GPT-5 MCP:** https://github.com/makdas/gpt5-mcp
- **Email Orchestrator MCP:** https://github.com/makdas/email-orchestrator-mcp

## Technology Stack

- **Languages:** TypeScript, Python
- **Runtime:** Node.js, Python
- **Containerization:** Docker, Docker Compose
- **Protocol:** Model Context Protocol (MCP)
- **Integration:** Claude Code, MCP clients

## License

This project is open source. See individual project directories for specific license information.

## Contributing

1. Fork the repository (monorepo or individual project)
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

For major changes, please open an issue first to discuss what you would like to change.

---

**Built with ❤️ for the agentic coding community**