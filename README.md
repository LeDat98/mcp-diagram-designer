<div align="center">

# Diagram Designer

### Transform messy Mermaid code into stunning architecture diagrams

[![MCPize](https://img.shields.io/badge/MCPize-Marketplace-7c3aed?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJ3aGl0ZSI+PHBhdGggZD0iTTEyIDJMMiA3bDEwIDUgMTAtNS0xMC01ek0yIDE3bDEwIDUgMTAtNS0xMC01LTEwIDV6TTIgMTJsMTAgNSAxMC01LTEwLTUtMTAgNXoiLz48L3N2Zz4=)](https://mcpize.com/mcp/diagram-designer)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Contact-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/leducdat-profile)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**Stop wrestling with diagram tools.** Write your system architecture in Mermaid, and let AI generate professional diagrams — ready for presentations, documentation, and open-source projects.

[Get Started on MCPize](https://mcpize.com/mcp/diagram-designer) · [Try in Playground](https://mcpize.com/mcp/diagram-designer/playground) · [Contact Me](https://www.linkedin.com/in/leducdat-profile)

</div>

---

## The Problem

You have a complex system architecture described in Mermaid code — nodes, edges, subgraphs everywhere. It's functional but **nobody wants to look at it**. You need clean, professional diagrams for:

- **Presentations** — Impress stakeholders with polished system overviews
- **Infrastructure docs** — Make your architecture documentation actually readable
- **Open-source READMEs** — Showcase your project with diagrams that attract contributors
- **Technical blogs** — Illustrate complex systems beautifully

**Diagram Designer** takes your Mermaid code and transforms it into production-quality architecture diagram images in under 60 seconds.

---

## Showcase

### Cloud Style

> Clean, modern cloud-native diagrams with AWS/GCP/Azure color palettes. Perfect for system documentation and presentations.

![DeepRAG Cloud Architecture](showcase/Deeprag_cloud.png)

<details>
<summary><b>More Cloud Style Examples</b></summary>

#### ShopFlow E-Commerce Platform
![ShopFlow Cloud Architecture](showcase/ecommerce_cloud.png)

</details>

---

### Darkmode Style

> Sleek dark backgrounds with neon accents. Ideal for tech presentations, pitch decks, and modern documentation.

![DataPulse Streaming Architecture](showcase/streaming_darkmode.png)

---

### Isometric Style

> 3D layered perspective that intuitively conveys system hierarchy and depth. The most visually stunning option for showcasing complex platforms.

![NeuralForge MLOps Architecture](showcase/ai_platform_isometric.png)

---

## Features

| Feature | Details |
|---|---|
| **5 Visual Styles** | Cloud, Isometric, Blueprint, Whiteboard, Darkmode |
| **3 Aspect Ratios** | Presentation (16:9), Documentation (4:3), Social (1:1) |
| **3 Detail Levels** | Overview (5-8 blocks), Medium (10-15), Full (15-25) |
| **Cloud Palettes** | AWS, GCP, Azure, or auto-detect from your Mermaid code |
| **2 Quality Tiers** | Standard (fast, ~50s) or Premium (high fidelity, ~100s) |
| **Up to 2K Resolution** | Crisp output for slides, docs, and print |
| **Secure by Default** | Download links expire in 1 hour, auto-deleted for privacy |

---

## How It Works

```
Your Mermaid Code  →  AI Prompt Composer  →  Image Generator  →  Professional PNG
    (input)            (understands your       (Gemini AI)        (download link)
                        architecture)
```

1. **Provide** your Mermaid diagram + system description
2. **Choose** your preferred style, detail level, and quality tier
3. **Receive** a professional PNG with proper icons, labels, colors, and layout
4. **Download** your image (link valid for 1 hour)

---

## Quick Start

### Step 1: Subscribe on MCPize

Visit the [Diagram Designer marketplace page](https://mcpize.com/mcp/diagram-designer) and subscribe to a plan. Free tier available (2 diagrams).

### Step 2: Get Your API Key

After subscribing, copy your API key from your MCPize account settings.

### Step 3: Configure Your MCP Client

<details>
<summary><b>Claude Code (CLI)</b></summary>

```bash
claude mcp add --transport http diagram-designer https://diagram-designer.mcpize.run/mcp \
  --header "Authorization: Bearer YOUR_API_KEY"
```

Or add via JSON:

```bash
claude mcp add-json diagram-designer '{
  "type": "http",
  "url": "https://diagram-designer.mcpize.run/mcp",
  "headers": {
    "Authorization": "Bearer YOUR_API_KEY"
  }
}'
```

</details>

<details>
<summary><b>Cursor IDE</b></summary>

Create `.cursor/mcp.json` in your project (or `~/.cursor/mcp.json` for global):

```json
{
  "mcpServers": {
    "diagram-designer": {
      "url": "https://diagram-designer.mcpize.run/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

</details>

<details>
<summary><b>Windsurf</b></summary>

Edit `~/.codeium/windsurf/mcp_config.json`:

```json
{
  "mcpServers": {
    "diagram-designer": {
      "serverUrl": "https://diagram-designer.mcpize.run/mcp",
      "headers": {
        "Authorization": "Bearer ${env:MCPIZE_API_KEY}"
      }
    }
  }
}
```

Set the environment variable: `export MCPIZE_API_KEY=YOUR_API_KEY`

</details>

<details>
<summary><b>Claude Desktop</b></summary>

Go to **Settings > Connectors** and add the MCPize server URL. Or use `mcp-remote` in your config file:

**macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
**Windows**: `%APPDATA%\Claude\claude_desktop_config.json`

```json
{
  "mcpServers": {
    "diagram-designer": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://diagram-designer.mcpize.run/mcp",
        "--header",
        "Authorization: Bearer YOUR_API_KEY"
      ]
    }
  }
}
```

</details>

<details>
<summary><b>VS Code (GitHub Copilot)</b></summary>

Create `.vscode/mcp.json` in your workspace:

```json
{
  "servers": {
    "diagram-designer": {
      "type": "http",
      "url": "https://diagram-designer.mcpize.run/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

> Note: VS Code uses `"servers"` as root key, not `"mcpServers"`.

</details>

### Step 4: Generate Your Diagram

Once connected, ask your AI assistant to generate a diagram. Example prompt:

> *"Generate an architecture diagram for my system using Diagram Designer. Style: cloud, quality: premium, purpose: presentation."*

The AI will ask you a few clarifying questions, create a Mermaid diagram, and call the `generate_diagram_image` tool to produce your diagram.

---

## Parameters

| Parameter | Options | Default |
|---|---|---|
| `style` | `cloud` · `isometric` · `blueprint` · `whiteboard` · `darkmode` | `cloud` |
| `purpose` | `presentation` (16:9) · `doc` (4:3) · `social` (1:1) | `doc` |
| `color_preference` | `aws` · `gcp` · `azure` · `custom` · `auto` | `auto` |
| `detail_level` | `overview` · `medium` · `full` | `medium` |
| `quality` | `standard` · `premium` | `standard` |
| `resolution` | `1K` · `2K` | `2K` |

---

## Pricing

| Plan | Price | Diagrams | Quality | Resolution |
|---|---|---|---|---|
| **Free** | $0 | 2 lifetime | Standard | 1K |
| **Starter** | $5/mo | 10/mo | Standard | 2K |
| **Pro** | $12/mo | 30/mo | Premium | 2K |
| **Credits** | $1.50/each | 1 | Premium | 2K |
| **Pack 8** | $10 | 8 | Premium | 2K |
| **Pack 18** | $20 | 18 | Premium | 2K |

---

## Pro & Premium Quality — Worth It

For the best results, we strongly recommend using the **Pro plan** or **Premium quality** tier:

- **2.2x more detailed prompts** — The Premium tier uses an advanced AI model that generates prompts with ~10,700 characters vs ~5,000 for Standard. This means more precise component placement, better icon descriptions, and richer color instructions.
- **Higher Mermaid logic compliance** — Premium diagrams more accurately follow the relationships and hierarchy defined in your Mermaid code. Connections, data flows, and groupings are preserved with greater fidelity.
- **Complex systems, no problem** — For large architectures with 15-25+ components (microservices, ML pipelines, multi-tier platforms), Premium handles the complexity without cutting corners or merging components.
- **2K resolution** — Every label, icon, and connection line stays crisp and readable, even in dense diagrams. No more blurry text or artifacts.

> **TL;DR**: Use Standard for quick iterations and drafts. Use Premium for final deliverables, presentations, and documentation you'll share with others.

---

## For Enterprises

Need to deploy Diagram Designer within your organization's infrastructure? Have questions about custom integrations, volume pricing, or private instances?

**Let's talk.** Reach out via LinkedIn:

[![LinkedIn](https://img.shields.io/badge/Le_Duc_Dat-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/leducdat-profile)

---

<div align="center">

### If you find this useful, please consider giving a star!

[![Star on MCPize](https://img.shields.io/badge/Star_on-MCPize-7c3aed?style=for-the-badge)](https://mcpize.com/mcp/diagram-designer)
[![Star on GitHub](https://img.shields.io/badge/Star_on-GitHub-181717?style=for-the-badge&logo=github)](https://github.com/leducdat-profile/diagram-designer-showcase)

Your support helps us improve and build more features.

---

**Built with** Gemini AI **·** FastMCP **·** Cloudflare R2

MIT License © 2026 Le Duc Dat

</div>
