# Instalação rápida

Pedágios: Pedágio Digital é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_pedagios_pedagio_digital`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Pedágios: Pedágio Digital` / `https://api.mcp.ai/p_pedagios_pedagio_digital`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "pedagios_pedagio_digital": { "type": "http", "url": "https://api.mcp.ai/p_pedagios_pedagio_digital" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pedagios_pedagio_digital&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wZWRhZ2lvc19wZWRhZ2lvX2RpZ2l0YWwifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "pedagios_pedagio_digital": { "url": "https://api.mcp.ai/p_pedagios_pedagio_digital" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=pedagios_pedagio_digital&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pedagios_pedagio_digital%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "pedagios_pedagio_digital": { "type": "http", "url": "https://api.mcp.ai/p_pedagios_pedagio_digital" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_pedagios_pedagio_digital
```

Dúvidas? [pedagios_pedagio_digital@mcp.ai](mailto:pedagios_pedagio_digital@mcp.ai)
