# My DSH plugins

[简体中文](DSH_PLUGINS.md) · [Profile](README.md)

I maintain nine DeepSeek Harness plugins for cost tracking, interface controls, visual feedback, task-based plugin composition and Windows integrations. Each plugin installs independently.

Versions and install links below were collected on 2 October 2026. Each repository README and Releases page carries subsequent updates.

| Plugin | What it does | Version |
| --- | --- | --- |
| [dsh-cost-meter](https://github.com/Han-1413141/dsh-cost-meter) | Track session and model costs, token usage, budgets, provider balances and coding-plan quotas in a bilingual DSH interface. | 1.8.5 |
| [dsh-sticky-disclosure](https://github.com/Han-1413141/dsh-sticky-disclosure) | Collapse expanded thinking and tool sections with one click or a custom hotkey, and pin off-screen section titles in DSH Desktop and Web. | 1.0.1 |
| [dsh-ui-hub](https://github.com/Han-1413141/dsh-ui-hub) | Search, show, hide, move, resize and arrange plugin controls in DSH Desktop and Web, with layout backup, restore and undo. | 0.1.0 |
| [dsh-visual-edit](https://github.com/Han-1413141/dsh-visual-edit) | Select elements, draw arrows or frame areas in DSH previews, send visual feedback to chat and compare before-and-after snapshots. | 0.5.2 |
| [dsh-autocompose](https://github.com/Han-1413141/dsh-autocompose) | Find and compose DSH plugins from a task description, then open an independent chat environment or install the plan into the current profile. | 0.5.0 |
| [dsh-compat-guardian](https://github.com/Han-1413141/dsh-compat-guardian) | Detect DSH plugin conflicts and loading failures, quarantine affected bundles and recover them, with offline startup rescue. | 0.2.1 |
| [dsh-wsl-native](https://github.com/Han-1413141/dsh-wsl-native) | Use Windows and native Linux DSH sessions in one Windows window, with WSL environment switching and bidirectional system tools. | 0.7.0 |
| [dsh-pnpm-build-control](https://github.com/Han-1413141/dsh-pnpm-build-control) | Control pnpm build-script approval across DSH profiles from Add Plugin, and repair same-Git-URL updates on DSH 0.2.0-rc.2. | 0.1.4 |
| [dsh-codex-computer-use](https://github.com/Han-1413141/dsh-codex-computer-use) | Let a DSH model inspect and operate Windows applications through an installed Codex Computer Use runtime, with per-session app approval. | 0.1.4 |

## Choose by task

- **Work across Windows and Linux**: WSL Native keeps Windows and native Linux DSH sessions in one window. Requires WSL 2 and Node.js on both systems.
- **Operate Windows applications**: Codex Computer Use uses an installed, initialized Codex Desktop runtime with DSH's selected model. The README documents the upstream browser URL-verification limitation.
- **Point out webpage changes**: Visual Edit adds element selections, arrows or framed areas to your chat draft and compares snapshots after the page updates.
- **Prepare task-specific plugins**: AutoCompose searches and combines plugins, opens an independent chat client, or installs the plan into your current profile.
- **Recover and maintain plugins**: Guardian handles conflicts, quarantine, recovery and offline startup rescue. pnpm Build Control manages build-script approval across profiles; disabling approval allows dependency build scripts and requires its risk confirmation.
- **Organize daily work**: Cost Meter shows costs and quotas; Sticky Disclosure collapses expanded thinking and tool sections; UI Hub arranges plugin controls and saves layouts.

## Install

Current repository documentation primarily targets DSH 0.2.0-rc.2. Desktop and Web are separate profiles. Use the CLI belonging to your DSH application and the intended profile. Each command below installs one plugin.

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

## Screenshots

Images below are from the projects' public READMEs.

![Visual Edit element, arrow and rectangle modes](https://raw.githubusercontent.com/Han-1413141/dsh-visual-edit/main/docs/images/native-modes.png)

![Windows and WSL sessions](https://raw.githubusercontent.com/Han-1413141/dsh-wsl-native/main/docs/assets/unified-conversations.png)

![UI Hub native theme](https://raw.githubusercontent.com/Han-1413141/dsh-ui-hub/main/docs/assets/ui-native-light.png)

For a problem or concrete use case, open an issue in the relevant repository with the plugin version, DSH version, operating system and reproduction steps. English and Chinese feedback are welcome.
