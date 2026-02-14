# Project Minato (The Remote Controller) ⚓

## Overview
**Project Minato** (formerly Sora-Link) is a standalone orchestrator designed to provide remote CLI access and real-time streaming via external channels (Telegram, Discord, Vault, etc.). It acts as the "Harbor" for all remote session data and coordination.

## Goals
- **Channel Autonomy:** Robust handlers for Telegram, Discord, and Filesystem watchers.
- **Universal Communication Bus:** Support existing bot channels to ensure a unified experience across different platforms.
- **Multi-Session Management:** Handle multiple concurrent sessions with efficient context switching.
- **Live Streaming:** Real-time stdout/stderr streaming directly back to the triggering channel.
- **Vault Integration:** Organized session data in Project Kura for persistence and manual inspection.
- **Secure Execution:** Integrated with **Project Aegis** for safety and human-in-the-loop approvals.

## Planned Components
- \`internal/channel\`: Native implementation for Discord/Telegram/Filesystem.
- \`internal/session\`: Lifecycle management for active sessions and metadata.
- \`internal/engine\`: The core loop orchestrating commands and channel routing.
- \`internal/stream\`: Real-time data piping between processes and user channels.

## Status
- [x] Initial Repo Structure Created (Renamed to Minato)
- [x] Architecture Design (Multi-Session & Universal Bus Update)
- [ ] Channel Prototype (Discord/Telegram)
- [ ] Session Context Switching Logic
