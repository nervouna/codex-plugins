# Contributing

Codex Plugins is a personal project, but bug reports and fixes are welcome.

## Issues

- **Bugs:** use the bug report form. Give the plugin version, the Codex version, your operating system, what happened and what you expected. Do not paste raw session logs, credentials or private conversations.
- **Security problems:** report them privately, see [SECURITY.md](SECURITY.md).
- **Feature ideas and new plugins:** open an issue to discuss it first. The project stays small on purpose, so not every idea will fit.

## How the project is developed

Each plugin lives in `plugins/<name>/` with its own `.codex-plugin/plugin.json`, `README.md`, `CHANGELOG.md` and license, and is listed in `.agents/plugins/marketplace.json`. A release bumps the version in `plugin.json`, adds a `CHANGELOG.md` entry, and is tagged `<plugin>-v<version>`.

Session Stats is standard-library Python 3.12. The program does all collection and calculation; the skill in `skills/session-stats/SKILL.md` only tells the model to run it and show the result. Keep it that way: no network access, no writes outside the output directory, and no session text in its output or error messages.

## Pull requests

Describe the problem, what you changed, and how you checked it (the Codex version and the commands you ran). Keep one change per pull request.
