# systemd-netns
## About
Utilities to create and manage network namespaces with systemd

## Installation

1. Place netns@.service and netns-peer@.service in a systemd service directory (e.g. /etc/systemd/system)
2. Install the helper script somewhere in the root user's path (e.g. /usr/local/sbin)
3. create a configuration file for each namespace you wish to create

## Configuration

Configuration files are stored in /etc/systemd with the name netns-(name).conf in the format:

```
BRIDGE_IF=br0
OPT_ARGS="-m 5a:e9:49:7f:17:da"
```

We just need to know a bridge interface and optionally a mac addresss
