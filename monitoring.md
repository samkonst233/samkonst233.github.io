# Live Monitoring

Watch player screens in real-time through the web dashboard.

## Overview

Live Monitoring uses WebRTC technology to stream player screens directly to your browser, allowing you to:

- View player screens in real-time
- Detect cheaters through visual inspection
- Capture screenshots for evidence
- Monitor multiple players simultaneously

## Setup

### Server Configuration

Add these settings to your `server.cfg`:
```cfg
setr fivemsecure:enable_streaming "true"
setr fivemsecure:streaming_port "3001"
```

### Firewall Configuration

Open UDP port 3001 on your server:

**Linux (UFW)**
```bash
sudo ufw allow 3001/udp
```

**Linux (iptables)**
```bash
sudo iptables -A INPUT -p udp --dport 3001 -j ACCEPT
sudo iptables-save > /etc/iptables/rules.v4
```

**Windows Firewall**
```powershell
New-NetFirewallRule -DisplayName "FiveMSecure Streaming" -Direction Inbound -Protocol UDP -LocalPort 3001 -Action Allow
```

### Restart Resource
```bash
restart fivemsecure
```

## Using Live Monitoring

### Access Monitoring

1. Open dashboard at [fivemsecure.com/dashboard](https://fivemsecure.com/dashboard)
2. Navigate to **Monitoring** section
3. View list of connected players

### Start Streaming

Click on any player to begin streaming their screen. The stream will appear in your browser.

### Controls

- **Play** - Start watching player
- **Stop** - End stream
- **Screenshot** - Capture current frame

### Multi-Stream Viewing

Watch up to 4 players simultaneously by clicking multiple players. Streams appear in a grid layout.

## Performance Optimization

### Stream Quality Settings

Configure in `config.lua`:
```lua
Config.Streaming = {
    enabled = true,
    frameRate = 15,      -- Frames per second
    quality = 0.7,       -- 0.1 to 1.0
    width = 1280,
    height = 720
}
```

### Recommended Settings by Connection Speed

**High-Speed (100+ Mbps)**
```lua
frameRate = 30
quality = 0.8
width = 1920
height = 1080
```

**Medium-Speed (50 Mbps)**
```lua
frameRate = 15
quality = 0.7
width = 1280
height = 720
```

**Low-Speed (< 25 Mbps)**
```lua
frameRate = 10
quality = 0.5
width = 1280
height = 720
```

## Privacy Considerations

> Players should be notified that monitoring is active on your server.

Add to your server rules:
- "This server uses anti-cheat monitoring"
- "Player screens may be viewed by administrators"
- "By playing here, you consent to monitoring"

Check local laws regarding monitoring and recording.

## Common Issues

### Black Screen

**Cause**: Player doesn't have game window focused or WebGL disabled

**Solution**:
1. Ask player to focus game window
2. Verify resource config has WebGL enabled
3. Restart the stream

### Connection Failed

**Cause**: Firewall blocking UDP or incorrect port configuration

**Solution**:
1. Verify firewall allows UDP on port 3001
2. Check `streaming_port` in server.cfg matches config
3. Restart FiveMSecure resource

### Laggy or Choppy Stream

**Cause**: Bandwidth limitations or high frameRate setting

**Solution**:
1. Lower `frameRate` to 10-15
2. Reduce `quality` to 0.5-0.6
3. Use smaller resolution (1280x720)

### No Players Visible

**Cause**: Resource not loaded or WebSocket disconnected

**Solution**:
1. Check FiveMSecure is started (`resources` command)
2. Verify license key is correct
3. Check server console for errors
4. Restart resource

## Advanced Usage

### Screenshot Capture

Screenshots are automatically uploaded and can be viewed in the dashboard under the player's activity log.

### Recording (Coming Soon)

Full stream recording functionality will be available in a future update.