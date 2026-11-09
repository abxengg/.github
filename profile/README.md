# ABX Engineering

Developer tools that run on your own machine: code review for Java services, and an editor theme for people who live in the terminal.

## Codist

**[Codist](https://github.com/abxengg/codist)** reviews a Java and Spring Boot repository locally. It watches the repository, checks every new commit with deterministic rules and a local AI model (via Ollama), and shows the results in your browser. Each model claim is checked against the code before it is shown. Nothing leaves your machine, and it never changes your code unless you approve a fix.

```sh
# macOS / Linux
curl -fsSL https://raw.githubusercontent.com/abxengg/codist/remaster/install.sh | sh

# Docker (includes git, Java 21 and Maven)
docker run --rm -p 8080:8080 -v "$PWD:/repo" -v codist-data:/data \
  --add-host=host.docker.internal:host-gateway ghcr.io/abxengg/codist

# Go
go install github.com/abxengg/codist@latest
```

Windows: `irm https://raw.githubusercontent.com/abxengg/codist/remaster/install.ps1 | iex`

| Module | What it does |
|---|---|
| [codist](https://github.com/abxengg/codist) | The app: one program that watches the repository and serves the interface |
| [codist-review](https://github.com/abxengg/codist-review) | Reviews a commit and keeps track of its issues |
| [codist-fix](https://github.com/abxengg/codist-fix) | Prepares fixes, builds and tests them in a separate copy, commits only after approval |
| [codist-behaviour](https://github.com/abxengg/codist-behaviour) | Runs changed methods before and after a commit and shows what behaves differently |
| [codist-java](https://github.com/abxengg/codist-java) | Java parser, code checks, class graph and call graph |
| [codist-git](https://github.com/abxengg/codist-git) | Reads a git repository; builds test repositories |
| [codist-model](https://github.com/abxengg/codist-model) | Model server client and production log parsing |
| [codist-ui](https://github.com/abxengg/codist-ui) | The Svelte interface, embedded already built |
| [codist-eval](https://github.com/abxengg/codist-eval) | Measures what Codist catches on real Java bugs |

## Hell Pine

**[Hell Pine](https://github.com/abxengg/hell-pine)** is a darker, higher-contrast take on Rosé Pine for VS Code, born inside tmux.

[Install from the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=ABX.hell-pine), or run `ext install ABX.hell-pine` from the VS Code Quick Open bar.

---

[theabx.in](https://theabx.in) · [abinash@theabx.in](mailto:abinash@theabx.in)
