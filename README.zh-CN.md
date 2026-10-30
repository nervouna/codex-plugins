# Codex Plugins

[English](README.md) | 简体中文

Damao 的 Codex 插件发布仓库。各插件独立版本，通过同一个 marketplace 安装。

## 状态

这是个人项目：作者为自己使用 Codex App 而写的插件，公开出来供他人安装。Session Stats 0.1.2 是首个公开版本，已在 macOS 和 Codex CLI 0.159.0 上验证。需要 Codex App、支持插件的 Codex CLI，以及可通过 `python3` 调用的 Python 3.12 或更高版本。除 Codex 本身外，不需要 API key 或其他账号。插件界面（指标名称、范围按钮）为中文。

各插件独立发布：每个版本有一个 tag 和一个 GitHub release（例如 `session-stats-v0.1.2`），变更记录在插件的 `CHANGELOG.md` 中。Codex 通过 marketplace 从本仓库安装和更新插件。报告问题或提交修复见 [CONTRIBUTING.md](CONTRIBUTING.md)，安全问题见 [SECURITY.md](SECURITY.md)。

## 安装

先添加插件源：

```sh
codex plugin marketplace add nervouna/codex-plugins
```

然后安装需要的插件：

```sh
codex plugin add session-stats@codex-plugins
```

重启 Codex App，在新会话中使用插件。

## 插件

| 插件 | 用途 | 环境要求 |
| --- | --- | --- |
| [Session Stats](plugins/session-stats/README.md) | 在对话中展示本机会话统计快照 | Codex App、支持插件的 Codex CLI、Python 3.12+ |

## 更新

```sh
codex plugin marketplace upgrade codex-plugins
codex plugin add session-stats@codex-plugins
```

更新后重启 Codex App。

## 反馈

请通过本仓库 Issues 报告问题，附上插件版本、Codex 版本和操作系统。不要上传会话原始记录、凭证或私人对话内容。

## 许可证

[MIT](LICENSE)。
