# Live Monitoring

Watch player screens in real-time through the dashboard.

## What is Live Monitoring?

Live Monitoring uses WebRTC to stream player screens to your dashboard. You can:

- Watch player screens in real-time
- See exactly what they're doing
- Take screenshots for evidence
- Detect cheaters visually

## Setup

### Server Configuration

Add to your `server.cfg`:
```cfg
setr fivemsecure:enable_streaming "true"
setr fivemsecure:streaming_port "3001"
```

### Firewall

Open UDP port 3001:
```bash
# Linux (UFW)
sudo ufw allow 3001/udp

# Linux (iptables)
sudo iptables -A INPUT -p udp --dport 3001 -j ACCEPT
```

### Restart
```bash
restart fivemsecure
```

## Usage

1. Go to **Dashboard** → **Monitoring**
2. View all connected players
3. Click on a player to start streaming

## Controls

- **Play** - Start watching player
- **Stop** - Stop streaming
- **Screenshot** - Capture current frame

## Performance Settings

Optimize for your connection:

**Good Internet (100+ Mbps)**:
```lua
frameRate = 30
quality = 0.8
width = 1920, height = 1080
```

**Average Internet (50 Mbps)**:
```lua
frameRate = 15
quality = 0.7
width = 1280, height = 720
```

**Limited Internet (< 25 Mbps)**:
```lua
frameRate = 10
quality = 0.5
width = 1280, height = 720
```

## Privacy

> Make sure players are aware they're being monitored. Add to your server rules.

## Troubleshooting

**Black screen**
- Check player has game in focus
- Verify WebGL is enabled
- Restart the stream

**Connection failed**
- Check firewall allows UDP on port 3001
- Verify streaming_port matches in config
- Restart FiveMSecure resource

**Laggy stream**
- Lower frameRate in config
- Reduce quality setting
- Use smaller resolution