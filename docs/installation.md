---
title: Installation Guide
description: "Follow this tutorial to easily install and use Claude Code on your computer."
---

# Claude Code Installation Guide

Follow this tutorial to easily install and use Claude Code on your computer.

## 📍 Choose Your Operating System

- **Windows**: Windows 10/11
- **macOS**: Intel & Apple Silicon
- **Linux/WSL2**: Ubuntu, CentOS, Arch...

---

## 🪟 Windows Installation Tutorial

### 1. Install Node.js Environment
Claude Code requires a Node.js environment to run.

**Method 1: Official Download (Recommended)**
1. Visit [Node.js Official Website](https://nodejs.org/)
2. Click "LTS" version to download
3. Double-click the `.msi` file and follow the installation wizard
4. Verify installation:
   ```bash
   node --version && npm --version
   ```

**Method 2: Using Package Manager**
```powershell
# Using Chocolatey
choco install nodejs

# Using Scoop
scoop install nodejs
```

### 2. Install Claude Code
**Method 1: PowerShell One-Click Installation (Recommended)**
```powershell
# Run PowerShell as administrator
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
irm https://claude.ai/install.ps1 | iex
```

**Method 2: npm Installation**
```powershell
npm install -g @anthropic-ai/claude-code
```

### 3. Set Environment Variables
Configure Claude Code environment variables to connect to your proxy service.

**Method 1: Temporary Setting (Current Session)**
```powershell
$env:ANTHROPIC_BASE_URL = "your-url"
$env:ANTHROPIC_AUTH_TOKEN = "your-API-key"
```

**Method 2: Permanent Setting (User-level)**
```powershell
# Set user-level environment variables (permanent)
[System.Environment]::SetEnvironmentVariable("ANTHROPIC_BASE_URL", "your-url", [System.EnvironmentVariableTarget]::User)
[System.Environment]::SetEnvironmentVariable("ANTHROPIC_AUTH_TOKEN", "your-API-key", [System.EnvironmentVariableTarget]::User)
```
*Note: Restart PowerShell for settings to take effect.*

---

## 🍎 macOS Installation Tutorial

### 1. Install Node.js Environment
**Method 1: Using Homebrew (Recommended)**
```bash
brew update
brew install node
```

**Method 2: Official Website Download**
1. Visit [nodejs.org](https://nodejs.org/)
2. Download the LTS version for macOS
3. Open the `.pkg` file and follow instructions.

### 2. Install Claude Code
```bash
npm install -g @anthropic-ai/claude-code
```

### 3. Set Environment Variables
**Permanent Setting (zsh default):**
```bash
echo 'export ANTHROPIC_BASE_URL="your-url"' >> ~/.zshrc
echo 'export ANTHROPIC_AUTH_TOKEN="your-API-key"' >> ~/.zshrc
source ~/.zshrc
```

---

## 🐧 Linux/WSL2 Installation Tutorial

### 1. Install Node.js Environment
```bash
# Using NodeSource (Recommended)
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs
```

### 2. Install Claude Code
```bash
sudo npm install -g @anthropic-ai/claude-code
```

### 3. Set Environment Variables
```bash
echo 'export ANTHROPIC_BASE_URL="your-url"' >> ~/.bashrc
echo 'export ANTHROPIC_AUTH_TOKEN="your-API-key"' >> ~/.bashrc
source ~/.bashrc
```

---

## 🚀 Start Using Claude Code

**Launch Claude Code:**
```bash
claude
```

**Use in Specific Project:**
```bash
cd /path/to/your/project
claude
```
