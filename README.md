# Project Setup & Troubleshooting Log

## 🛠 Tools Installed
- **Node.js (LTS)**: JavaScript runtime and npm package manager.
- **Git for Windows**: Provides Git-Bash and essential Unix tools for Windows.
- **Claude Code**: Anthropic's CLI agent for terminal-based coding.
- **Cursor**: AI-powered code editor (IDE).
- **OpenAI Codex**: Agentic AI extension within Cursor.

## 🚀 Steps Completed
1. Installed Node.js and verified installation with `node -v` and `npm -v`.
2. Installed `@anthropic-ai/claude-code` globally via npm.
3. Configured Windows Environment Variables for Git-Bash integration.
4. Authenticated Claude Code via the Anthropic Console (Pay-as-you-go).
5. Connected Cursor to GitHub and cloned the project repository.
6. Successfully pushed documentation to GitHub.

## ⚠️ Issues Encountered & Solutions

### 1. 'npm' is not recognized
- **Problem:** PowerShell didn't know what `npm` was.
- **Solution:** Installed Node.js from the official website and **restarted the terminal** to refresh the System PATH.

### 2. PowerShell Execution Policy Error
- **Problem:** Windows blocked the `npm.ps1` script from running for security reasons.
- **Solution:** Ran `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser` in an Administrator PowerShell window.

### 3. Claude Code requires Git-Bash
- **Problem:** Claude Code couldn't find Unix-style commands (like `ls` or `grep`) on Windows.
- **Solution:** Installed Git for Windows and created a new Environment Variable `CLAUDE_CODE_GIT_BASH_PATH` pointing to `C:\Program Files\Git\bin\bash.exe`.

### 4. Git 'fatal: pathspec' Error
- **Problem:** Tried to `git add` the README while the terminal was in the wrong folder.
- **Solution:** Used `ls` to verify the file location and `cd` to navigate into the correct project subdirectory.

### 5. Blank File on GitHub
- **Problem:** Pushed the file before hitting "Save" in Cursor, resulting in an empty file online.
- **Solution:** Pressed **`Ctrl + S`** to save the file to disk, then re-ran `git add`, `commit`, and `push`.