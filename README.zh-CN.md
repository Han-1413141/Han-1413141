# Han

我开发让 AI 编程过程更容易理解和使用的工具，主要关注**费用追踪、指令调试和插件界面**。

[English](README.md) · [全部项目](https://github.com/Han-1413141?tab=repositories) · [开源贡献](https://github.com/pulls?q=is%3Apr+author%3AHan-1413141+-user%3AHan-1413141)

## 主要项目

### [DSH Cost Meter](https://github.com/Han-1413141/dsh-cost-meter)

查看 AI 编程费用花在了哪里。为 DeepSeek Harness 提供会话费用、Token 用量、预算、渠道余额和 Coding Plan 额度展示，支持中英文界面。

- 区分订阅用量与按量付费支出。
- 查看各模型费用与历史用量，支持自定义价格。
- 根据社区问题持续修复，并记录每次变更。

[安装与使用](https://github.com/Han-1413141/dsh-cost-meter/blob/master/README.zh-CN.md) · [更新记录](https://github.com/Han-1413141/dsh-cost-meter/blob/master/CHANGELOG.md)

### [Codex Context Map](https://github.com/Han-1413141/codex-context-map)

查看哪些 `AGENTS.md` 会被发现、哪些文件被同目录的 override 遮蔽，以及字节预算在哪里截断指令。提供命令行工具和可交互的离线报告，无运行时依赖。

```sh
npx codex-context-map . --html context-map.html
```

[![Codex Context Map：目录树、指令链与字节预算](https://raw.githubusercontent.com/Han-1413141/codex-context-map/main/docs/assets/preview.png)](https://han-1413141.github.io/codex-context-map/?lang=zh)

[在线演示](https://han-1413141.github.io/codex-context-map/?lang=zh) · [中文说明](https://github.com/Han-1413141/codex-context-map/blob/main/README.zh-CN.md) · [发现规则与限制](https://github.com/Han-1413141/codex-context-map/blob/main/docs/semantics.md) · [持续集成](https://github.com/Han-1413141/codex-context-map/actions/workflows/ci.yml)

## 其他工具

| 项目 | 解决的问题 |
| --- | --- |
| [DSH UI Hub](https://github.com/Han-1413141/dsh-ui-hub) | 发现插件界面元素，支持逐项显示、隐藏、移动、缩放和排列。 |
| [DSH Sticky Disclosure](https://github.com/Han-1413141/dsh-sticky-disclosure) | 一键或通过自定义快捷键收起展开的思考与工具调用区域。 |

## 开发方向

目前主要使用 JavaScript 和 Node.js 开发浏览器界面与命令行工具，重视可复现的问题、针对修复的回归测试、清楚的安装说明和明确的功能边界。

如果遇到问题或有具体使用需求，欢迎在对应仓库提交 issue。提供最小示例、预期行为和实际结果，便于定位与讨论。中文、英文都可以。
