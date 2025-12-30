# Blender MCP Gemini CLI Extension

This extension enables Gemini CLI to interact with Blender using the Model Context Protocol (MCP).

## Contents
- `gemini-extension.json`: The extension definition and MCP configuration for Gemini CLI.
- `GEMINI.md`: System instructions for the Gemini model to effectively use Blender tools.

## Setup

### 1. Install Blender Addon
1.  Download the latest `addon.py` file from the [official BlenderMCP repository](https://github.com/ahujasid/blender-mcp/blob/main/addon.py).
2.  Open Blender (3.0+).
3.  Go to **Edit > Preferences > Add-ons**.
4.  Click **Install...** and select the downloaded `addon.py` file.
5.  Enable the "Interface: Blender MCP" addon.
6.  In the 3D Viewport Sidebar (press `N`), find the **BlenderMCP** tab.
7.  Click **Connect to Claude** (starts the socket server on port 9876).

### 2. Configure Gemini CLI
The `gemini-extension.json` file contains the necessary configuration.

Run the following command to install this extension:
```bash
gemini extension install https://github.com/JosephKu/blender-mcp-gemini-cli-extension
```

To install a specific version (e.g., v1.0.0):
```bash
gemini extension install https://github.com/JosephKu/blender-mcp-gemini-cli-extension --ref v1.0.0
```

### 3. Updating
To update the extension to the latest version:
```bash
gemini extension update blender
```
Or to update all extensions:
```bash
gemini extension update --all
```

### 4. Usage
Once connected, you can ask Gemini to:
- "Create a cube and move it to (0,0,5)"
- "List all objects in the scene"
- "Download a brick texture from Poly Haven"
- "Run a python script to scatter trees"

## Requirements
- Blender 3.0+
- Python 3.10+
- `uv` package manager
