# Project Minato (The Unified Channel Harbor) ⚓

## Overview
Project Minato is the centralized communication and session management layer for the local ecosystem. It is the only component responsible for interacting with external platforms like Discord, Telegram, and the Web.

## Core Mission
To provide a unified "Channel-as-a-Service" for other local tools (like Hashi and Aegis). Instead of each tool implementing its own Discord bot, they all connect to Minato.

## Key Features
- **Universal Channel Layer:** Native implementations for Discord, Telegram, and Filesystem watchers.
- **Session Harbor:** Manages real-time streaming of stdout/stderr from multiple concurrent sessions.
- **Unified UI:** Provides a local Web UI for managing all connected sessions and channel settings.
- **Persistent Storage:** Integrated with **Project Kura** for long-term session archiving.

## Architecture
Minato provides an internal API (IPC/WebSocket) that other projects use to "speak" to the outside world.

\`\`\`mermaid
graph TD
    Hashi[Hashi Orchestrator] -->|Stream| Minato
    Aegis[Aegis Security] -->|Approval Req| Minato
    Minato -->|Bot API| Discord[Discord]
    Minato -->|Bot API| Telegram[Telegram]
    Minato -->|HTTP| WebUI[Local Web UI]
\`\`\`
