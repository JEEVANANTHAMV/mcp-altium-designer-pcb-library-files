# Altium Designer (PCB Library Files)

> Reads and edits Altium circuit-board library files (component and schematic libraries) directly. You don't need Altium open to use it — only to view the results afterwards.

The bundle zip (**3.3 MB**) is stored in this repository at **`a47c875e-3ca1-498f-a075-4ed801c76b5e.zip`**.

This repository is part of the **Forjinn-Desk** MCP bundle collection. An MCP bundle is a self-contained server that a host application launches and communicates with over the MCP (Model Context Protocol) protocol.

## Repo metadata

| Field | Value |
| --- | --- |
| Registry ID | `a47c875e-3ca1-498f-a075-4ed801c76b5e` |
| Status in registry | active |
| Bundle size | 3.3 MB |
| Distribution | committed to this repo |

## Environment variables

| Variable | Value / note |
| --- | --- |
| `RUST_LOG` | `info` |

## MCP launch configuration

The host replaces `__INSTALL_DIR__` (install dir) and `__PYTHON__` (bundled Python) at runtime.

```json
{
  "command": "__INSTALL_DIR__\\altium-designer-mcp.exe",
  "args": [
    "__INSTALL_DIR__\\mcp-config.json"
  ],
  "env": {
    "RUST_LOG": "info"
  }
}
```


## Install / usage

1. Get the bundle:
   - download `a47c875e-3ca1-498f-a075-4ed801c76b5e.zip` from this repo (Code → Download ZIP, or `git clone`).
2. Extract to your target installation directory (config paths expect contents at the install-dir root).
3. Set the environment variables listed above.
4. Launch using the MCP config JSON (or let a host client manage it automatically).

> Bundles may include vendored runtimes (bundled Python, Node, or native executables). Builds are Windows x64.
