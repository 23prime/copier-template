# copier-template

## About

Copier template for general projects.

### Features

- **[mise](https://mise.jdx.dev) as the dev tool manager** — Tool installation, task running (`mise check`, `mise fix`), and git hooks ([lefthook](https://github.com/evilmartians/lefthook)) are all managed through mise.
- **AI agent support** — `AGENTS.md` and `CLAUDE.md` provide project-level instructions for AI coding agents (Claude Code, GitHub Copilot, etc.).
- **GitHub Actions CI/CD** — Workflows for markdown linting and auto-fix are included out of the box.
- **Markdown linting** — [markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2) with a pre-configured ruleset and VS Code integration.
- **GitHub best practices** — `CODEOWNERS`, pull request template, Dependabot configuration, and contributing guide.
- **EditorConfig** — Consistent coding style (charset, indentation, line endings) across editors.

### File structure

```txt
{{project_name}}
├── .editorconfig
├── .github
│   ├── CODEOWNERS
│   ├── PULL_REQUEST_TEMPLATE.md
│   ├── copilot-instructions.md
│   ├── dependabot.yml
│   └── workflows
│       ├── check-empty.yml
│       └── check-markdown.yml
├── .gitignore
├── .markdownlint-cli2.jsonc
├── .vscode
│   ├── extensions.json
│   └── settings.json
├── AGENTS.md
├── CLAUDE.md
├── README.md
├── docs
│   └── CONTRIBUTING.md
├── lefthook.yml
└── mise.toml
```

## Usage

### Prerequisites

- [Copier](https://copier.readthedocs.io/)

### Generate a new project

```sh
copier copy https://github.com/23prime/copier-template path/to/destination
```

You will be prompted to enter:

| Question | Description | Default |
| --- | --- | --- |
| `project_name` | Project name | — |
| `license` | License type (`MIT`, `Apache-2.0`, `GPL-3.0`) | `MIT` |

### Update an existing project

```sh
copier update
```
