# bioRxiv MCP Server

🔍 Enable AI assistants to search and access bioRxiv papers through a simple MCP interface.

The bioRxiv MCP Server provides a bridge between AI assistants and bioRxiv's preprint repository through the Model Context Protocol (MCP). It allows AI models to search for biology preprints and access their metadata in a programmatic way.

🤝 Contribute • 📝 Report Bug

## ✨ Core Features
- 🔎 Paper Search: Query bioRxiv papers with keywords or advanced search ✅
- 🚀 Efficient Retrieval: Fast access to paper metadata ✅
- 📊 Metadata Access: Retrieve detailed metadata for specific papers ✅
- 📊 Research Support: Facilitate biological sciences research and analysis ✅
- 📄 Paper Access: Download and read paper content 📝
- 📋 Paper Listing: View all downloaded papers 📝
- 🗃️ Local Storage: Papers are saved locally for faster access 📝
- 📝 Research Prompts: A set of specialized prompts for paper analysis 📝

## 🚀 Quick Start

### Prerequisites

- Python 3.10+
- FastMCP library

### Installation

#### Using uvx (Recommended)

```bash
uvx --from "git+https://github.com/pansapiens/bioRxiv-MCP-Server" biorxiv-mcp-server
```

#### Using with Claude Desktop

Add this configuration to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "biorxiv": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/pansapiens/bioRxiv-MCP-Server",
        "biorxiv-mcp-server"
      ]
    }
  }
}
```

#### Using with Cursor

Add this configuration to your cursor settings:

```json
{
  "mcpServers": {
    "biorxiv": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/pansapiens/bioRxiv-MCP-Server",
        "biorxiv-mcp-server"
      ]
    }
  }
}
```

#### Using with Cline

Add this configuration to your cline settings:

```json
{
  "mcpServers": {
    "biorxiv": {
      "command": "bash",
      "args": [
        "-c",
        "uvx --from \"git+https://github.com/pansapiens/bioRxiv-MCP-Server\" biorxiv-mcp-server"
      ]
    }
  }
}
```

#### Using with Opencode

Add this configuration to your `~/.config/opencode/opencode.json`:

```json
{
  "mcp": {
    "biorxiv": {
      "type": "local",
      "command": [
        "uvx",
        "--from",
        "git+https://github.com/pansapiens/bioRxiv-MCP-Server",
        "biorxiv-mcp-server"
      ],
      "enabled": true
    }
  }
}
```


## 📊 Usage

Start the MCP server:

```bash
uvx --from "git+https://github.com/pansapiens/bioRxiv-MCP-Server" biorxiv-mcp-server
```

## 🛠 MCP Tools

The bioRxiv MCP Server provides the following tools:

1. `search_biorxiv_key_words`: Search for articles on bioRxiv using keywords.
2. `search_biorxiv_advanced`: Perform an advanced search for articles on bioRxiv with multiple parameters.
3. `get_biorxiv_metadata`: Fetch metadata for a bioRxiv article using its DOI.

### Searching Papers

You can ask the AI assistant to search for papers using queries like:
```
Can you search bioRxiv for recent papers about genomics?
```

### Getting Paper Details

Once you have a DOI, you can ask for more details:
```
Can you show me the metadata for the paper with DOI 10.1101/123456?
```

## 📁 Project Structure

- `biorxiv_mcp_server/biorxiv_server.py`: The main MCP server implementation using FastMCP
- `biorxiv_mcp_server/biorxiv_web_search.py`: Contains the web scraping logic for searching bioRxiv

## 🔧 Dependencies

- Python 3.10+
- FastMCP
- asyncio
- logging

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.

## ⚠️ Disclaimer

This tool is for research purposes only. Please respect bioRxiv's terms of service and use this tool responsibly.
