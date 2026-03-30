---
title: FAQ
description: "Frequently asked questions about Claude Code installation, features, and troubleshooting."
---

# Claude Code FAQ

## 💻 Installation and Environment

**Q: Which operating systems does Claude Code support?**
- **Windows**: Windows 10/11 (recommended)
- **macOS**: macOS 10.14 and above
- **Linux**: Ubuntu 18.04+, CentOS 7+, and other mainstream distributions.

**Q: What should I do if Claude Code won't start after installation?**
- Check if system requirements are met.
- Run as administrator (Windows).
- Check firewall and antivirus settings.
- Reinstall the latest version.

---

## 🔧 Features and Usage

**Q: Which programming languages are supported?**
Claude Code supports almost all mainstream programming languages, including Web (JS/TS), Backend (Python, Java, Go, C#), Mobile (Swift, Kotlin), and Systems (C, C++, Rust).

**Q: Can it generate test code?**
Yes! Claude Code supports generating unit tests (Jest, PyTest), integration tests, and E2E tests (Playwright, Cypress).

**Q: How to make generated code better match project style?**
- Create a `.claude-code.json` configuration file in the project root.
- Specify a code style guide (e.g., Airbnb, Standard).
- Provide existing project code as a reference in your prompts.

---

## 🛠️ Troubleshooting

**Q: What to do if Claude Code responds slowly?**
- Check your network connection quality.
- Try using a proxy server.
- Clear the cache: `claude-code cache clear`.

**Q: Getting "API quota exceeded" error?**
- Check current usage: `claude-code usage show`.
- Wait for the quota reset (usually 1 hour).
- Optimize the frequency of your requests.

---

## 🔐 Security and Privacy

**Q: Will my code be saved?**
- Claude Code does not permanently store user code.
- Temporary data is cleaned after request processing.
- For sensitive projects, private deployment is recommended.

**Q: How to protect sensitive information?**
- Use environment variables to store keys instead of hardcoding them.
- Set up sensitive information filtering rules.
- Avoid writing secrets in code comments.
