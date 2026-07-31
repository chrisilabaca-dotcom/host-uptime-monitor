# host-uptime-monitor

Dead-man's switch. A machine publishes a UTC timestamp to a public gist on a
schedule. This repo runs a scheduled GitHub Action that reads that timestamp and
alerts if it goes stale, which means the machine (or the service on it) stopped
reporting.

The alarm deliberately lives here rather than on the machine: nothing running on
a host can alert you that the host is down.

Contains no credentials. The bot token and chat id are encrypted repository
secrets. The gist holds a bare timestamp and nothing else.
