---
tags:
  - cli
---

# Amazon Q Developer CLI

| Website | GitHub | License |
| --- | --- | --- |
| [aws.amazon.com/q](https://aws.amazon.com/q/) | [aws/amazon-q-developer-cli](https://github.com/aws/amazon-q-developer-cli) | Apache 2.0 |

**Amazon Q Developer CLI (Q CLI) is a command-line interface that brings the capabilities of Amazon Q—AWS’s generative-AI-powered coding assistant—directly into your terminal and local development workflow.**

Q CLI enables conversational coding, code generation, and refactoring without leaving the shell. It complements the Amazon Q IDE plug-ins by offering an editor-agnostic way to interact with the assistant and is especially useful for lightweight environments such as cloud shells, remote servers, or CI tasks.

### Key Features

* **Conversational assistant** – Ask questions in natural language and receive contextual answers based on your repository contents.
* **Code generation & modification** – Generate new files, update existing ones, or apply large-scale refactors; Q CLI writes the changes and shows a git diff for review.
* **Multi-file understanding** – Analyses the entire git repo to provide smarter suggestions and accurate navigation.
* **Run & test commands** – Can execute unit tests or build commands suggested by the AI, shortening the build-and-verify loop.
* **Works everywhere** – Runs on macOS, Linux, and Windows (x86‐64 & Arm) with zero external dependencies apart from git and an AWS account.

### Installation

Amazon distributes pre-built binaries via Homebrew, Chocolatey, and direct download.

#### Homebrew (macOS / Linux)

```bash
brew tap aws/tap
brew install amazon-q-cli
```

#### Scoop / Chocolatey (Windows)

```powershell
choco install amazon-q-cli
# or
scoop bucket add aws https://github.com/aws/scoop-bucket.git
scoop install amazon-q-cli
```

#### Manual download

Grab the latest release archive from the [GitHub releases page](https://github.com/aws/amazon-q-developer-cli/releases) and place the extracted `q` binary somewhere on your `$PATH`.

### Quickstart

1. **Authenticate** – Set up your AWS credentials (via `aws configure`) and run `q init` to complete OAuth sign-in for Amazon Q.
2. **Enter chat mode** – Inside a git repository, type:

   ```bash
   q chat
   ```

   Then ask something like “generate a UnitTest for `handlers/user.go`”.
3. **Review changes** – Q CLI stages edits in git; use `git diff` to inspect and `git commit` (or `q accept`) to apply.

### Links

* **GitHub:** https://github.com/aws/amazon-q-developer-cli
* **Docs:** https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/what-is-qdeveloper.html
* **AWS announcement blog:** https://aws.amazon.com/blogs/aws/meet-amazon-q/

### Tutorials & Resources

* **Getting started with Amazon Q Developer CLI** – AWS YouTube (2024) — https://www.youtube.com/watch?v=qcli_demo
* **Automating refactors with Q CLI** – AWS Dev Blog — https://aws.amazon.com/blogs/developer/q-cli-refactor/

