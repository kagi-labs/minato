# Project Minato (The Agent Orchestrator) ⚓

## Overview
Project Minato is the central **Orchestration and Communication Hub** for the Kagi Labs ecosystem. It acts as the "Command Deck" where the user provides orders and Minato orchestrates how those orders are routed to various delegation engines.

## Core Mission
To provide a unified orchestration layer that coordinates agents and sessions. It manages the human-in-the-loop experience through multiple channels (Discord, Telegram, Web) and ensures that delegated tasks are tracked from start to finish.

## Key Features
- **Central Orchestration:** Routes user orders to the appropriate worker (e.g., Hashi).
- **Universal Channel Layer:** Only component responsible for external messaging.
- **Session Coordination:** Manages real-time data streaming and multi-agent collaboration.
- **Persistent Storage:** Integrated with **Project Kura** for global state.

## Architecture
Minato sits at the top of the hierarchy, giving orders to Hashi and receiving security feedback from Aegis.

\`\`\`mermaid
graph TD
    User[User / Discord / Telegram] -->|Orders| Minato
    Minato -->|Delegate Task| Hashi[Hashi Delegation Engine]
    Hashi -->|Tool Call| Aegis[Aegis Security]
    Aegis -->|Approval Req| Minato
    Minato -->|UI Prompt| User
\`\`\`
