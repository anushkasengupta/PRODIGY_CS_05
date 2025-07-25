Windows Network Monitor

A lightweight Python script to monitor network connections on Windows without requiring Npcap or WinPcap.

Features

- 🖥️ Monitors active network connections in real-time
- 🔍 Resolves remote IP addresses to hostnames
- 📝 Logs all connections to daily log files
- ⚡ Lightweight - uses only built-in Python libraries and psutil
- 🚫 No Npcap/WinPcap dependency required

Requirements

- Python 3.x
- psutil library

The script will:
- Display active connections in your console
- Create a `net_logs` directory if it doesn't exist
- Save logs to daily files named `conn_log_YYYY-MM-DD.txt`

Press `Ctrl+C` to stop monitoring.

Log Format

Each connection is logged with:
- Timestamp
- Local address and port
- Remote address and port
- Remote hostname (when resolvable)
- Process PID (when available)
- Connection status

Example Output

```
============================================================
🕒 Timestamp        : 2023-01-01 12:34:56
📍 Local Address    : 192.168.1.100:49672
🌐 Remote Address   : 172.217.14.206:443
🔍 Remote Hostname  : lax17s42-in-f14.1e100.net
⚙️  Process PID      : 1234
🔁 Connection Status: ESTABLISHED
```

Notes
- The script runs continuously until manually stopped
- New connections are only logged once to avoid duplicates
- Logs are appended to daily files in the `net_logs` directory
- Requires administrator privileges to see all processes

