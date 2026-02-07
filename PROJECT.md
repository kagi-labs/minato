# Sora-Link (The Remote Controller)

## Overview
Sora-Link (formerly BMO-Link) is a standalone orchestrator designed to provide remote CLI access and real-time streaming via external channels (Telegram, Vault, etc.). It allows Player 1 to execute commands on the host from anywhere and see the output live.

## Goals
- **Channel Autonomy:** We build our own handlers for Telegram, Discord, and Filesystem watchers.
- **Session Management:** Persist state across remote calls.
- **Live Streaming:** Stream stdout/stderr directly back to the triggering channel.
- **Secure Execution:** Use the MCP Firewall and Policy Engine for safety.

## Planned Components
- `internal/channel`: Custom implementation for Telegram/Filesystem.
- `internal/engine`: Orchestrates the "expect message -> run cmd -> return" loop.
- `internal/stream`: Handles the real-time pipe from process to channel.

## Status
- [x] Initial Repo Structure Created
- [ ] Architecture Design (In Progress)
- [ ] Channel Prototype (Telegram)
