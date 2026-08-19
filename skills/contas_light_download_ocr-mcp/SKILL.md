---
name: contas_light_download_ocr-mcp
description: Skill da REST API do Light: Download + OCR na MCP.AI: 1 endpoint em /api/contas_light_download_ocr. Light: Download + OCR, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Light: Download + OCR — REST API skill

Você tem acesso à **Light: Download + OCR** REST API na MCP.AI.

> Light: Download + OCR, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/contas_light_download_ocr
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/contas_light_download_ocr/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"login":"...","senha":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/contas_light_download_ocr/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `contas_light_download_ocr_consultar`

Light: Download + OCR, consulta em fonte oficial. _(POST /api/contas_light_download_ocr/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `login` | string | Sim | Parâmetro de consulta "login". |
| `senha` | string | Sim | Parâmetro de consulta "senha". |
| `codigo_cliente` | string | Não | Parâmetro de consulta "codigo_cliente". |
| `codigo_instalacao` | string | Não | Parâmetro de consulta "codigo_instalacao". |
| `mes` | string | Não | Parâmetro de consulta "mes". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_contas_light_download_ocr` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
