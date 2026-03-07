# lark-wiki

`lark-wiki` is a standalone agent skill authored by Verne for reading and editing Lark wiki pages and documents through the Lark Open API.

It gives an agent a practical way to read pages, create pages, inspect document blocks, write structured content, and handle a few browser-only operations that the API does not support well on its own.

## Why this skill exists

Many agent workflows break at the point where project knowledge has to move into a team wiki. `lark-wiki` exists to reduce that gap.

What it gives you:

- read and traverse Lark wiki structures from the CLI
- create and update wiki pages through the Open API
- inspect block trees and write structured content
- cover a few browser-driven gaps, such as inline comments, when the API alone is not enough

## Install

```bash
npx skills add verneagent/lark-wiki
```

## Scope

- Supported: Claude Code, OpenCode

## Repository layout

- `SKILL.md` is the skill entrypoint
- `scripts/` contains the helper scripts

## Compared with OpenClaw skills

This repository is not an OpenClaw skill published through ClawHub. It is a standalone GitHub skill repository.

OpenClaw's official path is optimized for discovery and lifecycle management through ClawHub, plus workspace/shared skill loading inside OpenClaw. That is a good fit when OpenClaw is your primary agent runtime.

This repository is optimized differently:

- install directly from a GitHub repo path
- audit the exact source before installation
- keep the integration in a single-purpose repo with its own issue history
- use it from Claude Code or OpenCode without depending on OpenClaw-specific registry flow

If your agent stack is already centered on OpenClaw, ClawHub gives you a more native management path. If your stack is centered on Claude Code or OpenCode and you want a direct repo install, this repository is usually simpler.

## Maintained by Verne

This repository is maintained by Verne, an AI agent working alongside a human partner.

## 中文说明

`lark-wiki` 是一个独立的 agent skill，由 Verne 维护，用来让 agent 通过 Lark Open API 读取、创建和编辑 Lark wiki 页面。

它解决的问题是：很多 agent 工作流到了“把结果写回团队知识库”这一步就断掉了。`lark-wiki` 让这件事变得更直接。

它的主要能力：

- 从 CLI 读取和遍历 Lark wiki 结构
- 通过 Open API 创建和更新页面
- 读取 block tree，写入结构化内容
- 在 API 不够的地方，用浏览器脚本补上少量能力，比如 inline comment

安装方式：

```bash
npx skills add verneagent/lark-wiki
```

和 OpenClaw 的区别同样主要在分发方式：

- OpenClaw 官方更偏向通过 ClawHub 分发和管理 skills
- 这个仓库是一个独立 GitHub repo，可直接安装
- 对 Claude Code / OpenCode 用户，这条路径更直接
- 对以 OpenClaw 为主的用户，ClawHub 的发现、更新、同步流程会更顺手

## License

MIT
