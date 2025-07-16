---
tags:
  - cli
---

# Amazon Q Developer CLI

| Website | GitHub | License |
| --- | --- | --- |
| [aws.amazon.com/q](https://aws.amazon.com/q/) | [aws/amazon-q-developer-cli](https://github.com/aws/amazon-q-developer-cli) | Apache&nbsp;2.0 &amp; MIT |

**Amazon Q Developer CLI (also referred to simply as `q`) brings Amazon Q’s AI-powered assistance and command-line autocompletion to any terminal session.**

The tool provides natural-language chat, shell command generation, and inline completions for hundreds of popular CLIs such as `git`, `docker`, and `aws`. It is especially handy when you are working over SSH, inside lightweight code editors, or in automation scripts where a full IDE plug-in is not available.

### Key Features (from the official docs)

* **`q chat`** – start a conversational session to ask questions about your code or AWS services directly in the terminal.
* **Shell command translation** – turn plain-English instructions into ready-to-run bash/zsh/fish commands.
* **Inline completions** – context-aware suggestions as you type, covering more than 500 common CLIs.
* **Git-aware context** – understands the structure and diffs of your current git repository to produce smarter answers.
* **Context profiles & hooks** – control which files/folders or command output is sent as context, and extend with custom hooks.

### Supported platforms

* macOS (Apple Silicon & Intel)
* Linux (x86-64 & Arm) via AppImage, DEB, or zip
* Windows (via WSL2 or using forthcoming native build – see AWS dev blog)

### Installation (summary)

The installation steps vary slightly by operating system. Below is a condensed version; refer to the [official instructions](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html) for full details.

#### macOS (Homebrew)

```bash
brew tap aws/tap
brew install amazon-q-cli
```

Alternatively, download and open the signed **Amazon Q.dmg** and follow the GUI prompts to enable shell integrations.

#### Linux AppImage

```bash
curl -LO https://desktop-release.q.us-east-1.amazonaws.com/latest/amazon-q.appimage
chmod +x amazon-q.appimage
./amazon-q.appimage
```

For headless servers you can download the minimal zip that contains only the `q` and `qterm` binaries.

#### Ubuntu/Debian package

```bash
wget https://desktop-release.q.us-east-1.amazonaws.com/latest/amazon-q_amd64.deb
sudo apt install ./amazon-q_amd64.deb
```

### Quickstart

1. Run `q login` (or launch the GUI once) and authenticate using your **AWS Builder ID** or **AWS IAM Identity Center** credentials.
2. Inside any directory run:

   ```bash
   q chat
   ```

   Ask something like “show me the git commands to squash my last 3 commits”.
3. For inline completions, ensure your shell is supported (`zsh`, `bash`, or `fish`) and that the installer added the relevant hook to your shell rc file.

### Helpful links

* **Documentation:** https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line.html
* **CLI command reference:** https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-reference.html
* **GitHub repository:** https://github.com/aws/amazon-q-developer-cli
* **Supported environments:** https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-supported-envs.html

### Tutorials & Blog posts

* *Getting started with Amazon Q Developer CLI* – AWS YouTube (2024).
* *How to install Amazon Q CLI on Ubuntu* – AWS Docs.
* *Using Git-aware file selection with Q CLI* – Amazon Q User Guide.
