# Instalação detalhada

Light: Download + OCR é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_contas_light_download_ocr`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_contas_light_download_ocr` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_contas_light_download_ocr` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_contas_light_download_ocr` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.contas_light_download_ocr` (ou `servers.contas_light_download_ocr` no VS Code) do config do cliente e reinicie.
