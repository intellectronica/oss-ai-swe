---
tags:
  - cli
---

# Amazon Q CLI

| Website | GitHub | License |
| --- | --- | --- |
| [aws.amazon.com/q](https://aws.amazon.com/q/) | [aws/amazon-q-developer-cli](https://github.com/aws/amazon-q-developer-cli) | Apache&nbsp;2.0 &amp; MIT |

**Amazon Q CLI (also known simply as `q`) is a command-line companion that brings Amazon Q’s AI-powered chat and autocompletion features to your terminal.**

With `q` you can have a natural-language conversation, translate plain-English requests into shell commands, and receive inline completions for more than 500 popular CLIs such as `git`, `docker`, and `aws`.

### Key Features

* **`q chat` interactive mode:** Ask questions and get answers directly in the terminal.
* **Command generation & translation:** Convert natural-language instructions into executable shell commands.
* **Inline completions:** Context-aware suggestions as you type, based on your shell history and current directory.
* **Git-aware context:** Includes file diffs and project structure to refine answers and code suggestions.
* **Profiles & hooks:** Fine-grained control over what context is shared, with the ability to extend via custom hooks.

## Installation

Below is a condensed overview. See the [official installation guide](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html) for full details.

### macOS (Homebrew)

```bash
brew tap aws/tap
brew install amazon-q-cli
```

Alternatively, download the signed **Amazon Q.dmg** and drag the app to _Applications_. Launch once to enable shell integrations.

### Linux AppImage

```bash
curl -LO https://desktop-release.q.us-east-1.amazonaws.com/latest/amazon-q.appimage
chmod +x amazon-q.appimage
./amazon-q.appimage
```

For headless servers, download the minimal zip that contains only the `q` and `qterm` binaries.

### Ubuntu / Debian package

```bash
wget https://desktop-release.q.us-east-1.amazonaws.com/latest/amazon-q_amd64.deb
sudo apt install ./amazon-q_amd64.deb
```

## Quickstart

1. Authenticate:

   ```bash
   q login
   ```

   Sign in with your **AWS Builder ID** or **IAM Identity Center** credentials.
2. Start a chat session inside your project:

   ```bash
   q chat
   ```
3. For inline completions, ensure the installer added the appropriate hook to your shell (`zsh`, `bash`, or `fish`).

## Links

* **Docs – Using Q on the command line:** <https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line.html>
* **CLI reference:** <https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-reference.html>
* **GitHub:** <https://github.com/aws/amazon-q-developer-cli>
* **Supported environments:** <https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-supported-envs.html>
