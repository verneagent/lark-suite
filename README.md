# lark-wiki

`lark-wiki` is a standalone agent skill for reading and editing Lark wiki pages and documents through the Lark Open API.

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
npx skills add -g verneagent/lark-wiki
```

## Scope

- Supported: Claude Code, OpenCode

## Compared with `lark-openapi-mcp`

`larksuite/lark-openapi-mcp` is the official general-purpose Lark MCP. It is the right starting point if you want broad OpenAPI coverage across multiple Lark surfaces.

`lark-wiki` is intentionally narrower. It is optimized for wiki and doc workflows:

- reading wiki pages and trees
- creating wiki pages
- inspecting document blocks
- writing structured block content
- filling a few browser-only gaps such as inline comments

That makes the choice fairly simple:

- choose `lark-openapi-mcp` if you want an official general Lark MCP
- choose `lark-wiki` if your main need is wiki/doc authoring flow from an agent

The practical reason this repository exists is that the official MCP currently states two boundaries that matter for document-heavy workflows:

- file upload/download is not yet supported
- direct editing of Feishu/Lark cloud documents is not supported, only importing and reading

If those limits are acceptable, the official MCP is the broader and more native choice. If your agent needs a more focused wiki/doc writing path, `lark-wiki` is the more direct fit.

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
npx skills add -g verneagent/lark-wiki
```

## 与 `lark-openapi-mcp` 的区别

`larksuite/lark-openapi-mcp` 是官方的通用型 Lark MCP，更适合“我想把一大批 Lark OpenAPI 能力统一接给 agent”这种需求。

`lark-wiki` 则是一个刻意做窄的 skill，重点只放在 wiki 和文档工作流上：

- 读 wiki 页面和目录树
- 创建 wiki 页面
- 读取 block 结构
- 写入结构化 block 内容
- 在 API 不够时，用浏览器脚本补少量文档操作能力，比如 inline comment

所以选择逻辑很简单：

- 如果你要官方、通用、覆盖面更广的 Lark MCP，选 `lark-openapi-mcp`
- 如果你主要要的是 wiki/doc 写作流，选 `lark-wiki`

这个仓库存在的实际原因也很明确：官方 MCP 目前明确写了两条边界，而这两条边界对文档工作流很关键：

- 还不支持文件上传/下载
- 还不支持直接编辑飞书/Lark 云文档，只支持导入和读取

如果这些限制你能接受，官方 MCP 是更原生的选择。  
如果你要的是更直接的 wiki/doc 写作与编辑路径，`lark-wiki` 会更顺手。

## License

MIT
