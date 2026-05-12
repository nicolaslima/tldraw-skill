# tldraw-skill — From Text to Whiteboard Diagrams

[中文文档](README_CN.md)

A skill that turns natural-language descriptions into hand-drawn-style `.tldr` whiteboard diagrams and exports them to PNG / SVG via `@kitschpatrol/tldraw-cli` — with 6 diagram presets (Architecture, Flowchart, Sequence, ML/DL, ERD, UML), a vision-based self-check loop that auto-fixes overlaps and clipped labels, and an iterative review loop with a 5-round safety valve.

Works with Claude Code, Cursor, Copilot, OpenClaw, Codex, Hermes, and any agent that supports the [Agent Skills](https://agentskills.io) format.

## Documentation

| Doc | What's inside |
|---|---|
| [docs/features.md](docs/features.md) | Full feature list, comparison vs. native / drawio / mermaid / excalidraw, supported diagram types |
| [docs/limitations.md](docs/limitations.md) | Known limitations (UML notation, PDF export, vision requirement) |
| [skills/tldraw-skill/SKILL.md](skills/tldraw-skill/SKILL.md) | Workflow guide loaded by the agent |

## Quick Start

Install dependencies:

```bash
npm install -g @kitschpatrol/tldraw-cli && tldraw --version
```

Requires Node.js (npm). Works identically on macOS, Windows, and Linux — no browser automation.

Install the skill:

```bash
# Any agent (Claude Code, Cursor, Copilot, etc.)
npx skills add Agents365-ai/365-skills -g

# Claude Code only
> /plugin marketplace add Agents365-ai/365-skills
> /plugin install tldraw
```

Manual install — clone into your agent's skills directory:

```bash
git clone https://github.com/Agents365-ai/tldraw-skill.git ~/.claude/skills/tldraw-skill
```

Common paths: `~/.claude/skills/` (Claude Code), `~/.config/opencode/skills/` (Opencode), `~/.openclaw/skills/` (OpenClaw), `~/.agents/skills/` (Codex). Also indexed on [SkillsMP](https://skillsmp.com) and [ClawHub](https://clawhub.ai/agents365-ai/tldraw-pro-skill).

## Usage

Just describe what you want:

```
Create a microservices e-commerce architecture with API Gateway, auth/user/order/product/payment services,
Kafka message queue, notification service, and separate databases for each service
```

The agent will plan the layout, generate the `.tldr` JSON, export to PNG, self-check, and let you iterate.

## Example

**Prompt:** *Create a microservices e-commerce architecture with Mobile/Web/Admin clients, API Gateway, User/Order/Product/Payment services, Kafka event bus, Notification service, and User DB / Order DB / Product DB / Redis Cache / Stripe API*

![Microservices Architecture](assets/example.png)

## Support

If this skill helps you, consider supporting the author:

<table>
  <tr>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Agents365-ai/images_payment/main/qrcode/wechat-pay.png" width="180" alt="WeChat Pay">
      <br>
      <b>WeChat Pay</b>
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Agents365-ai/images_payment/main/qrcode/alipay.png" width="180" alt="Alipay">
      <br>
      <b>Alipay</b>
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Agents365-ai/images_payment/main/qrcode/buymeacoffee.png" width="180" alt="Buy Me a Coffee">
      <br>
      <b>Buy Me a Coffee</b>
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/Agents365-ai/images_payment/main/awarding/award.gif" width="180" alt="Give a Reward">
      <br>
      <b>Give a Reward</b>
    </td>
  </tr>
</table>

## Author

**Agents365-ai**

- Bilibili: https://space.bilibili.com/441831884
- GitHub: https://github.com/Agents365-ai

## License

MIT
