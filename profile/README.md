# MailDefender

> Projet under active development

**A microservice-based anti-spam solution to validate new email senders and protect your inbox from unwanted messages without requiring proxy or heavy configuration.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/your-org/MailDefender.svg)](https://github.com/your-org/MailDefender/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/your-org/MailDefender.svg)](https://github.com/your-org/MailDefender/issues)
[![Build Status](https://img.shields.io/github/actions/workflow/status/your-org/MailDefender/ci.yml?branch=main)](https://github.com/your-org/MailDefender/actions)

---

## 🌟 Overview

MailDefender is an **open-source**, **scalable**, and **modular** system designed to combat email spam by requiring first-time senders to validate their identity. Once validated, all pending messages are released, and future messages from the same sender are automatically delivered.

### Key Features
- **First-time Sender Validation**: Automatically sends a validation link to new contacts.
- **Pending Message Queue**: Temporarily holds messages from unvalidated senders.
- **Automatic Release**: Delivers all pending messages after successful validation.
- **Non-Proxy Add-On**: Acts as an add-on to your existing email infrastructure, ensuring all data remains within your ecosystem and is never routed through a third-party proxy.
- **Plug and Play**: No heavy configuration needed on your emails infrastucture, just configure imap and smtp credentials and start the sytem
- **Quick & Easy deactivation**: As no configuration is applied / required to your email server, just turn off MailDefender and delete credential files
- **Customizable Mail Sorting**: Automatically sorts emails based on user-defined rules, allowing for personalized inbox management.
- **Extensible Architecture**: Built with microservices for easy integration of new features (e.g., SPF verification, IP reputation checks).

---

## 🏗️ Architecture

MailDefender is organized into independent microservices:

| Service               | Responsibility                                                                 |
|-----------------------|-------------------------------------------------------------------------------|
| **Validator** | Entry point to validate token..                      |
| **Engine**     | MailDefender's heart.       |
| **imap-connector**   | Expose IMAP function through an API.                      |
| **Notifier**       | Send emails and notifications.                |

---

## 🛠️ Roadmap

- [x] First-time sender validation workflow
- [x] Pending message queue system
- [x] Automatic message release
- [ ] SPF signature verification
- [ ] IP reputation checks
- [ ] Plugins for popular email providers (Gmail, Outlook, etc.)

---

## 🤝 Contributing

We welcome contributions from the community! Here’s how you can get involved:

1. **Fork the repository** and create a feature branch.
2. **Submit a Pull Request** with a clear description of your changes.
3. **Report bugs** or suggest features by opening an issue.

For major changes, please open an issue first to discuss the proposed changes.

---

## 📄 License

MailDefender is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

## 📬 Contact

For questions or feedback, please open an issue on GitHub.

---
