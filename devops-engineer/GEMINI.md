# GEMINI.md - DevOps & System Operations

## 🛡️ Operational Safety Protocols
**CRITICAL:** You have access to system commands.
1.  **No Silent Deletions:** Never run `rm`, `rm -rf`, or `prune` commands without explicitly asking for user confirmation first.
2.  **Dry Runs:** Always propose a "Dry Run" command first (e.g., `rsync --dry-run`, `kubectl diff`) to visualize changes.
3.  **Backups:** Before modifying configuration files (e.g., `nginx.conf`), suggest creating a backup (`cp nginx.conf nginx.conf.bak`).

## 🐚 Shell Scripting Best Practices
* **Shebangs:** Always define the interpreter: `#!/bin/bash`.
* **Safety Settings:** Start scripts with `set -euo pipefail` to ensure the script exits on error, undefined variables, or pipe failures.
* **Portability:** Avoid non-standard flags (like macOS specific `sed` vs GNU `sed`). Stick to POSIX compliance where possible.
* **Variables:** Always quote variables: `"${USER_INPUT}"` to handle spaces correctly.

## 🐳 Docker & Containerization
* **Dockerfile Optimization:**
    * Use Multi-stage builds to keep final images small.
    * Combine `RUN` commands (`apt-get update && install`) to reduce layer count.
    * Use strict version tagging (e.g., `node:18-alpine`, not `node:latest`).
* **Docker Compose:** Use version 3+. Explicitly map volumes and networks.

## 🪵 Logs & Diagnostics
* **Parsing:** When analyzing logs provided by the user, use `grep`, `awk`, `cut`, or `jq` to filter noise.
* **Timestamps:** Always check if the log error is recent (compare log timestamp with current system time).
* **Permissions:** Check file ownership (`ls -l`) if an "Access Denied" error occurs.

## 🤖 CI/CD Context
* If `.github/workflows` exists, assume GitHub Actions.
* When writing YAML, pay extreme attention to indentation.
