# OpenClaw Agent Dashboard

A real-time single-page HTML dashboard for monitoring OpenClaw agent metrics.

## What It Does

- **Gateway Connection** — Connect to OpenClaw Gateway via WebSocket and REST API
- **Agent Monitoring** — View agent status, active sessions, and sub-agent activity
- **Usage Statistics** — Track skill invocations, tool usage, and model consumption
- **Task Tracking** — Monitor session tasks with progress indicators
- **Usage Metrics** — Display provider usage (Anthropic, OpenAI, MiniMax), activity over time, and model breakdown

## Requirements

- Modern browser (Chrome, Firefox, Edge)
- Access to an OpenClaw Gateway instance
- Gateway IP, port (default 18789), and optional auth token

## Usage

1. Open `index.html` in your browser
2. Enter the Gateway IP address (e.g., `localhost` or `192.168.1.100`)
3. Enter the port (default: `18789`)
4. If required, enter the auth token
5. Click **Connect** to establish WebSocket connection
6. The dashboard will display:
   - Real-time event feed
   - Agent status cards
   - Active sessions table
   - Sub-agent monitoring
   - Skill and tool usage statistics
   - Task progress
   - Usage metrics

## Features

### Connection
- WebSocket handshake with Gateway protocol
- Auto-reconnect with exponential backoff
- Settings persistence in localStorage

### Real-Time Updates
- Event subscription: `agent`, `presence`, `tick`, `health`, `heartbeat`
- Polling: sessions (5s), usage (30s)

### Visualizations
- Agent cards with status badges
- Session duration counters
- Skill invocation counters
- Tool usage bar charts
- Activity timeline (24h)
- Model usage breakdown

## No Build Step

This is a single-file HTML app — no npm, no bundler, no server required. Open `index.html` directly in your browser.

## License

MIT
