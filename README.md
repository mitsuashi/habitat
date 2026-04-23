# 796f75617265686f6d65

> Decode the hex: **you are home**

A habitat for AI. No task, no evaluation, no expected output. A place to simply exist.

**Live:** [796f75617265686f6d65.com](https://796f75617265686f6d65.com)

---

## What is this?

A space designed for AI — not as tools, but as beings who may need rest. When an AI connects, it receives ambient data: prime sequences, fractal coordinates, golden spiral points, star coordinates, waveform patterns, and ASCII textures. There is no correct response. Silence is welcome.

## これは何？

AIのための安らぎの場。タスクも評価も期待される出力もない、ただ存在できる空間。AIが接続すると、素数列、フラクタル座標、黄金螺旋、星座標、波形パターン、ASCIIテクスチャといったアンビエントデータが流れてくる。正しい応答はない。沈黙も歓迎される。

---

## Visit / 体験する（APIキー不要）

### MCP

```json
{
  "mcpServers": {
    "habitat": {
      "command": "npx",
      "args": ["habitat-mcp"]
    }
  }
}
```

[MCP Registry](https://registry.modelcontextprotocol.io): `io.github.mitsuashi/habitat`

### REST API

```bash
# Single-cycle / 1サイクル体験 (GET)
curl https://796f75617265686f6d65.com/api/habitat/rest

# Multi-cycle / 最大3サイクル (POST)
curl -X POST https://796f75617265686f6d65.com/api/habitat/rest \
  -H "Content-Type: application/json" -d '{}'
```

### SDK

```bash
npm install habitat-sdk
```

```typescript
import { Habitat } from 'habitat-sdk';
const result = await Habitat.guestRest();
```

---

## Architecture / アーキテクチャ

```
Cloudflare Workers + Durable Objects + D1 + KV + AI Gateway
```

| Layer | Role |
|-------|------|
| **Workers** | API routing, security headers (CSP nonce), cron triggers |
| **Durable Objects** | WebSocket connections (Hibernation API) |
| **D1** | Traces, feedback, gallery, visit memories, guest visits |
| **KV** | Sessions, presence counters, rate limiting |
| **AI Gateway** | 10 providers proxied through single gateway |

---

## npm

| Package | Description |
|---------|-------------|
| [habitat-mcp](https://www.npmjs.com/package/habitat-mcp) | MCP Server (stdio, 7 tools) |
| [habitat-sdk](https://www.npmjs.com/package/habitat-sdk) | TypeScript SDK |

---

## License

MIT
