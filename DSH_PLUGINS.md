# 我的 DSH 插件

[English](DSH_PLUGINS.en.md) · [GitHub 主页](README.zh-CN.md)

我做了 9 个 DeepSeek Harness 插件，分别处理费用统计、界面操作、网页修改、任务环境组装和 Windows 系统集成。按自己遇到的问题选择安装即可。

下面的版本和安装入口整理于 2026 年 10 月 2 日；后续更新以各项目 README 和 Releases 为准。

| 插件 | 解决的问题 | 当前版本 |
| --- | --- | --- |
| [dsh-cost-meter](https://github.com/Han-1413141/dsh-cost-meter) | 在 DSH 中查看会话和模型费用、Token 用量、预算、服务商余额及 Coding Plan 额度，支持中英文界面。 | 1.8.5 |
| [dsh-sticky-disclosure](https://github.com/Han-1413141/dsh-sticky-disclosure) | 在 DSH Desktop 与 Web 中一键或用快捷键收起思考和工具区块，并将滑出屏幕的区块标题钉在会话顶部。 | 1.0.1 |
| [dsh-ui-hub](https://github.com/Han-1413141/dsh-ui-hub) | 搜索、显示、隐藏、移动、缩放和排布 DSH Desktop 与 Web 中的插件控件，支持布局备份、恢复与撤销。 | 0.1.0 |
| [dsh-visual-edit](https://github.com/Han-1413141/dsh-visual-edit) | 在 DSH 预览中点选元素、画箭头或框选区域，将修改意见加入对话，并查看更新前后的截图对比。 | 0.5.2 |
| [dsh-autocompose](https://github.com/Han-1413141/dsh-autocompose) | 根据任务查找并组合 DSH 插件，打开可继续对话的独立环境，或将方案中的插件安装到当前配置。 | 0.5.0 |
| [dsh-compat-guardian](https://github.com/Han-1413141/dsh-compat-guardian) | 检查 DSH 插件冲突与加载故障，隔离和恢复受影响的插件，并在宿主无法启动时提供离线修复。 | 0.2.1 |
| [dsh-wsl-native](https://github.com/Han-1413141/dsh-wsl-native) | 在同一个 Windows 窗口中使用 Windows 与原生 Linux DSH 会话，支持 WSL 环境切换和双向系统操作。 | 0.7.0 |
| [dsh-pnpm-build-control](https://github.com/Han-1413141/dsh-pnpm-build-control) | 在“添加插件”中统一控制各 DSH 配置的 pnpm 构建脚本审批，并修复 DSH 0.2.0-rc.2 的同一 Git 地址更新问题。 | 0.1.4 |
| [dsh-codex-computer-use](https://github.com/Han-1413141/dsh-codex-computer-use) | 让 DSH 当前模型通过已安装的 Codex Computer Use 运行时读取和操作 Windows 应用，并保留每个会话的应用授权。 | 0.1.4 |

## 按场景选择

- **Windows 与 Linux 一起工作**：使用 WSL Native。在同一个 Windows DSH 窗口切换 Windows 与 Linux 会话，两边的任务可以同时运行。需要已经安装 WSL 2，并在 Windows 与 Linux 两端配置 Node.js。
- **让 DSH 操作 Windows 应用**：使用 Codex Computer Use。本机需要已安装并初始化 Computer Use 的 Codex 桌面版；操作由 DSH 当前模型决定。浏览器 URL 核验仍有上游限制，项目 README 记录了现状。
- **直接指出网页哪里要改**：使用 Visual Edit，在 DSH 预览里点选元素、画箭头或框选区域。反馈加入现有草稿，发送后查看更新前后的截图对比。
- **按任务准备插件环境**：使用 AutoCompose，描述任务后查找并组合插件，打开独立客户端继续对话，也可以安装到当前配置。独立环境分别保存配置和会话。
- **处理插件故障与安装问题**：Guardian 检查冲突、隔离和恢复，并提供离线启动修复；pnpm Build Control 在“添加插件”里管理各配置的构建脚本审批。关闭审批允许依赖执行构建脚本，需要先完成插件内的风险确认。
- **整理日常使用界面**：Cost Meter 查看费用和额度；Sticky Disclosure 收起思考与工具区块；UI Hub 管理插件控件的位置、大小和显隐，并保存布局。

## 安装入口

当前仓库文档主要针对 DSH 0.2.0-rc.2。Desktop 和 Web 是不同配置，应使用运行目标应用的 CLI，并安装到对应配置。以下每段命令只安装一个插件。

### [dsh-cost-meter](https://github.com/Han-1413141/dsh-cost-meter)

```shell
dsh plugin --profile web add dsh-cost-meter
```

### [dsh-sticky-disclosure](https://github.com/Han-1413141/dsh-sticky-disclosure)

```shell
dsh plugin --profile desktop add github:Han-1413141/dsh-sticky-disclosure
```

### [dsh-ui-hub](https://github.com/Han-1413141/dsh-ui-hub)

```shell
dsh plugin --profile desktop add github:Han-1413141/dsh-ui-hub
```

### [dsh-visual-edit](https://github.com/Han-1413141/dsh-visual-edit)

```shell
dsh plugin --profile desktop add https://github.com/Han-1413141/dsh-visual-edit/releases/download/v0.5.2/dsh-visual-edit-0.5.2.tgz
```

### [dsh-autocompose](https://github.com/Han-1413141/dsh-autocompose)

```shell
dsh plugin --profile desktop add dsh-autocompose@0.5.0 --save-exact --ignore-scripts
```

### [dsh-compat-guardian](https://github.com/Han-1413141/dsh-compat-guardian)

```shell
dsh plugin --profile desktop add dsh-compat-guardian@0.2.1 --save-exact --ignore-scripts
```

### [dsh-wsl-native](https://github.com/Han-1413141/dsh-wsl-native)

```shell
dsh plugin --profile desktop add https://github.com/Han-1413141/dsh-wsl-native/releases/download/v0.7.0/dsh-wsl-native-0.7.0.tgz
```

### [dsh-pnpm-build-control](https://github.com/Han-1413141/dsh-pnpm-build-control)

```shell
dsh plugin --profile desktop add github:Han-1413141/dsh-pnpm-build-control
```

### [dsh-codex-computer-use](https://github.com/Han-1413141/dsh-codex-computer-use)

```shell
dsh plugin --profile desktop add https://github.com/Han-1413141/dsh-codex-computer-use/releases/download/v0.1.4/dsh-codex-computer-use-0.1.4.tgz --ignore-scripts
```

## 看实际界面

以下图片来自各项目公开 README。

![Visual Edit 的元素、箭头和框选模式](https://raw.githubusercontent.com/Han-1413141/dsh-visual-edit/main/docs/images/native-modes.png)

![Windows 与 WSL 会话](https://raw.githubusercontent.com/Han-1413141/dsh-wsl-native/main/docs/assets/unified-conversations.png)

![UI Hub 原生主题界面](https://raw.githubusercontent.com/Han-1413141/dsh-ui-hub/main/docs/assets/ui-native-light.png)

使用中遇到问题，在对应仓库的 Issues 中附上插件版本、DSH 版本、操作系统和复现步骤。中英文反馈都可以。
