# Code Sandbox MCP

MCP (Model Context Protocol) server for E2B code sandbox. This server provides tools to create, manage, and execute code in secure E2B sandboxes.

## Features

- **Create Sandbox**: Create new E2B sandboxes with customizable timeout and template
- **Kill Sandbox**: Terminate existing sandboxes by ID
- **Run Code**: Execute Python code in sandboxes using Jupyter Notebook syntax
- **Run Command**: Execute shell commands in sandboxes

## Installation

```bash
pip install code-sandbox-mcp
```

Or using uv:

```bash
uv pip install code-sandbox-mcp
```

## Usage

### Configuration

Add the following configuration to your MCP client settings JSON file (e.g., `~/.config/claude_desktop/claude_desktop_config.json` for Claude Desktop, or `.cursor/mcp.json` for Cursor):

```json
{
  "mcpServers": {
    "code-sandbox-mcp": {
      "command": "uv",
      "args": ["run", "code-sandbox-mcp"],
      "env": {
        "E2B_API_KEY": "your_api_key_here",
        "E2B_DOMAIN": "your_domain_here"
      }
    }
  }
}
```

Replace `your_api_key_here` and `your_domain_here` with your actual E2B credentials.

Restart your MCP client to load the configuration. The tools will be available in your MCP-enabled application!

## License

MIT
