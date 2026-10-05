# Codex Plugins

Damao 的 Codex 插件发布仓库。各插件独立版本，通过同一个 marketplace 安装。

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
